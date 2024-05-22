# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_mcmodel
- machine: linux-x86_64
- commit hash: c3cb6dd
- commit date: 2024-05-22
- overall geometric mean: 1.07x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.14 ms: 1.07x slower                                                 |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                |
| html5lib       | 64.8 ms                                                | 66.3 ms: 1.02x slower                                                 |
| tornado_http   | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                  |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 934 ms: 1.38x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 79.3 ms: 1.21x faster                                                 |
| float          | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                 |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                  |
| regex_v8       | 22.9 ms                                                | 23.7 ms: 1.03x slower                                                 |
| regex_effbot   | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                 |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 2.01 sec: 1.15x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 227 us: 1.07x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                  |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                 |
| unpickle_list        | 5.21 us                                                | 5.10 us: 1.02x faster                                                 |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                                 |
| xml_etree_generate   | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 58.3 ms: 1.03x slower                                                 |
| unpickle             | 13.8 us                                                | 15.0 us: 1.09x slower                                                 |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.10 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.58 ms: 1.26x slower                                                 |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                 |
| genshi_xml      | 53.4 ms                                                | 54.3 ms: 1.02x slower                                                 |
| genshi_text     | 22.5 ms                                                | 24.0 ms: 1.06x slower                                                 |
| django_template | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-linux-x86_64-brandtbucher-justin_mcmodel-3.14.0a0-c3cb6dd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 170 us: 3.05x faster                                                  |
| generators                 | 74.9 ms                                                | 30.2 ms: 2.48x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                  |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 934 ms: 1.38x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                  |
| pylint                     | 476 ms                                                 | 351 ms: 1.36x faster                                                  |
| richards_super             | 61.9 ms                                                | 46.8 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                 |
| richards                   | 49.8 ms                                                | 40.2 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                  |
| nbody                      | 96.0 ms                                                | 79.3 ms: 1.21x faster                                                 |
| chaos                      | 71.9 ms                                                | 59.4 ms: 1.21x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 2.01 sec: 1.15x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.13x faster                                                 |
| coroutines                 | 27.0 ms                                                | 24.0 ms: 1.13x faster                                                 |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 68.2 ms: 1.12x faster                                                 |
| raytrace                   | 309 ms                                                 | 274 ms: 1.12x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 63.1 ms: 1.12x faster                                                 |
| fannkuch                   | 405 ms                                                 | 363 ms: 1.12x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                 |
| float                      | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.09x faster                                                  |
| scimark_fft                | 345 ms                                                 | 319 ms: 1.08x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.74 us: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.66 ms: 1.08x faster                                                 |
| pprint_pformat             | 1.55 sec                                               | 1.44 sec: 1.08x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.2 us                                                | 37.5 us: 1.07x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.75 ms: 1.07x faster                                                 |
| unpickle_pure_python       | 242 us                                                 | 227 us: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 703 ms: 1.06x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.52 ms: 1.06x faster                                                 |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                 |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                                 |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                  |
| deltablue                  | 3.92 ms                                                | 3.77 ms: 1.04x faster                                                 |
| nqueens                    | 87.9 ms                                                | 85.1 ms: 1.03x faster                                                 |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                                  |
| spectral_norm              | 108 ms                                                 | 105 ms: 1.03x faster                                                  |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                 |
| unpickle_list              | 5.21 us                                                | 5.10 us: 1.02x faster                                                 |
| logging_silent             | 111 ns                                                 | 109 ns: 1.02x faster                                                  |
| json                       | 5.24 ms                                                | 5.16 ms: 1.02x faster                                                 |
| tornado_http               | 98.1 ms                                                | 96.7 ms: 1.01x faster                                                 |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                  |
| mdp                        | 2.77 sec                                               | 2.76 sec: 1.00x faster                                                |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                                 |
| sqlglot_optimize           | 55.3 ms                                                | 55.8 ms: 1.01x slower                                                 |
| pyflate                    | 434 ms                                                 | 439 ms: 1.01x slower                                                  |
| genshi_xml                 | 53.4 ms                                                | 54.3 ms: 1.02x slower                                                 |
| xml_etree_generate         | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.22 us                                                | 3.29 us: 1.02x slower                                                 |
| html5lib                   | 64.8 ms                                                | 66.3 ms: 1.02x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 58.3 ms: 1.03x slower                                                 |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                  |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 859 us: 1.03x slower                                                  |
| thrift                     | 784 us                                                 | 808 us: 1.03x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.2 ms: 1.03x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 23.7 ms: 1.03x slower                                                 |
| sympy_expand               | 484 ms                                                 | 503 ms: 1.04x slower                                                  |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.68 ms: 1.05x slower                                                 |
| genshi_text                | 22.5 ms                                                | 24.0 ms: 1.06x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.14 ms: 1.07x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 68.9 ms: 1.07x slower                                                 |
| django_template            | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                 |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.09x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                |
| scimark_lu                 | 116 ms                                                 | 127 ms: 1.09x slower                                                  |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                  |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.10 us: 1.11x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                 |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                  |
| coverage                   | 78.8 ms                                                | 93.3 ms: 1.18x slower                                                 |
| telco                      | 6.86 ms                                                | 8.13 ms: 1.19x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                 |
| async_generators           | 374 ms                                                 | 471 ms: 1.26x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.58 ms: 1.26x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 9.24 ms: 1.27x slower                                                 |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.27x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (4): sqlglot_normalize, sympy_str, bench_mp_pool, deepcopy
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x