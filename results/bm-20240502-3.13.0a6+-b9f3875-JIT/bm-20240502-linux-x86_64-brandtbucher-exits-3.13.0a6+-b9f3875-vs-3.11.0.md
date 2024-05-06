# Results vs. 3.11.0

- fork: brandtbucher
- ref: exits
- machine: linux-x86_64
- commit hash: b9f3875
- commit date: 2024-05-02
- overall geometric mean: 1.06x faster
- HPT reliability: 95.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                          |
| chameleon      | 6.70 ms                                                | 7.05 ms: 1.05x slower                                         |
| docutils       | 2.66 sec                                               | 2.93 sec: 1.10x slower                                        |
| html5lib       | 64.8 ms                                                | 66.6 ms: 1.03x slower                                         |
| tornado_http   | 98.1 ms                                                | 96.2 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                          |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                          |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 956 ms: 1.35x faster                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                          |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.0 ms: 1.20x faster                                         |
| float          | 78.9 ms                                                | 73.5 ms: 1.07x faster                                         |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                          |
| regex_effbot   | 3.51 ms                                                | 3.60 ms: 1.03x slower                                         |
| regex_v8       | 22.9 ms                                                | 24.1 ms: 1.05x slower                                         |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                          |
| Geometric mean | (ref)                                                  | 1.04x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.28x faster                                         |
| tomli_loads          | 2.30 sec                                               | 1.92 sec: 1.20x faster                                        |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                          |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                          |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                         |
| pickle_pure_python   | 320 us                                                 | 307 us: 1.04x faster                                          |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                         |
| unpickle_list        | 5.21 us                                                | 5.30 us: 1.02x slower                                         |
| xml_etree_process    | 56.9 ms                                                | 59.3 ms: 1.04x slower                                         |
| xml_etree_generate   | 81.1 ms                                                | 86.6 ms: 1.07x slower                                         |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                         |
| pickle_list          | 4.59 us                                                | 4.99 us: 1.09x slower                                         |
| unpickle             | 13.8 us                                                | 16.1 us: 1.16x slower                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.60 ms: 1.26x slower                                         |
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.29x slower                                         |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.69 ms: 1.10x faster                                         |
| django_template | 33.5 ms                                                | 36.9 ms: 1.10x slower                                         |
| genshi_xml      | 53.4 ms                                                | 59.3 ms: 1.11x slower                                         |
| genshi_text     | 22.5 ms                                                | 25.4 ms: 1.13x slower                                         |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.98x faster                                          |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                        |
| asyncio_tcp                | 875 ms                                                 | 532 ms: 1.65x faster                                          |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                          |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                          |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                         |
| async_tree_io              | 1.29 sec                                               | 935 ms: 1.38x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 956 ms: 1.35x faster                                          |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                          |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.28x faster                                         |
| richards_super             | 61.9 ms                                                | 49.0 ms: 1.26x faster                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                          |
| nbody                      | 96.0 ms                                                | 80.0 ms: 1.20x faster                                         |
| tomli_loads                | 2.30 sec                                               | 1.92 sec: 1.20x faster                                        |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                         |
| chaos                      | 71.9 ms                                                | 60.8 ms: 1.18x faster                                         |
| richards                   | 49.8 ms                                                | 42.3 ms: 1.18x faster                                         |
| fannkuch                   | 405 ms                                                 | 349 ms: 1.16x faster                                          |
| spectral_norm              | 108 ms                                                 | 94.8 ms: 1.14x faster                                         |
| raytrace                   | 309 ms                                                 | 275 ms: 1.12x faster                                          |
| logging_silent             | 111 ns                                                 | 99.1 ns: 1.12x faster                                         |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.55 ms: 1.10x faster                                         |
| mako                       | 10.7 ms                                                | 9.69 ms: 1.10x faster                                         |
| scimark_fft                | 345 ms                                                 | 314 ms: 1.10x faster                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 64.6 ms: 1.09x faster                                         |
| crypto_pyaes               | 76.7 ms                                                | 70.1 ms: 1.09x faster                                         |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                         |
| float                      | 78.9 ms                                                | 73.5 ms: 1.07x faster                                         |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                          |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                        |
| logging_simple             | 6.22 us                                                | 5.81 us: 1.07x faster                                         |
| logging_format             | 6.81 us                                                | 6.37 us: 1.07x faster                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                         |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                         |
| gc_traversal               | 4.01 ms                                                | 3.81 ms: 1.05x faster                                         |
| deltablue                  | 3.92 ms                                                | 3.76 ms: 1.04x faster                                         |
| pickle_pure_python         | 320 us                                                 | 307 us: 1.04x faster                                          |
| hexiom                     | 6.89 ms                                                | 6.62 ms: 1.04x faster                                         |
| djangocms                  | 33.5 us                                                | 32.3 us: 1.04x faster                                         |
| pathlib                    | 18.5 ms                                                | 18.0 ms: 1.03x faster                                         |
| json                       | 5.24 ms                                                | 5.09 ms: 1.03x faster                                         |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                          |
| pprint_safe_repr           | 747 ms                                                 | 731 ms: 1.02x faster                                          |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                          |
| tornado_http               | 98.1 ms                                                | 96.2 ms: 1.02x faster                                         |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                        |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                          |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                         |
| deepcopy                   | 365 us                                                 | 368 us: 1.01x slower                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                         |
| nqueens                    | 87.9 ms                                                | 89.0 ms: 1.01x slower                                         |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                          |
| unpickle_list              | 5.21 us                                                | 5.30 us: 1.02x slower                                         |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                          |
| html5lib                   | 64.8 ms                                                | 66.6 ms: 1.03x slower                                         |
| regex_effbot               | 3.51 ms                                                | 3.60 ms: 1.03x slower                                         |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                          |
| dask                       | 365 ms                                                 | 378 ms: 1.03x slower                                          |
| sqlglot_optimize           | 55.3 ms                                                | 57.3 ms: 1.04x slower                                         |
| bench_thread_pool          | 834 us                                                 | 864 us: 1.04x slower                                          |
| go                         | 149 ms                                                 | 154 ms: 1.04x slower                                          |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                          |
| sympy_integrate            | 21.5 ms                                                | 22.3 ms: 1.04x slower                                         |
| xml_etree_process          | 56.9 ms                                                | 59.3 ms: 1.04x slower                                         |
| pyflate                    | 434 ms                                                 | 453 ms: 1.04x slower                                          |
| sympy_expand               | 484 ms                                                 | 507 ms: 1.05x slower                                          |
| chameleon                  | 6.70 ms                                                | 7.05 ms: 1.05x slower                                         |
| regex_v8                   | 22.9 ms                                                | 24.1 ms: 1.05x slower                                         |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                          |
| xml_etree_generate         | 81.1 ms                                                | 86.6 ms: 1.07x slower                                         |
| dulwich_log                | 64.6 ms                                                | 69.2 ms: 1.07x slower                                         |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                         |
| pickle_list                | 4.59 us                                                | 4.99 us: 1.09x slower                                         |
| scimark_lu                 | 116 ms                                                 | 127 ms: 1.09x slower                                          |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                          |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                         |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.10x slower                                         |
| docutils                   | 2.66 sec                                               | 2.93 sec: 1.10x slower                                        |
| django_template            | 33.5 ms                                                | 36.9 ms: 1.10x slower                                         |
| genshi_xml                 | 53.4 ms                                                | 59.3 ms: 1.11x slower                                         |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                         |
| genshi_text                | 22.5 ms                                                | 25.4 ms: 1.13x slower                                         |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.13x slower                                          |
| unpickle                   | 13.8 us                                                | 16.1 us: 1.16x slower                                         |
| coverage                   | 78.8 ms                                                | 93.2 ms: 1.18x slower                                         |
| mypy2                      | 686 ms                                                 | 818 ms: 1.19x slower                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                         |
| async_generators           | 374 ms                                                 | 466 ms: 1.25x slower                                          |
| telco                      | 6.86 ms                                                | 8.55 ms: 1.25x slower                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.60 ms: 1.26x slower                                         |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.29x slower                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                  |

Benchmark hidden because not significant (4): pycparser, deepcopy_memo, sympy_str, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.20% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x