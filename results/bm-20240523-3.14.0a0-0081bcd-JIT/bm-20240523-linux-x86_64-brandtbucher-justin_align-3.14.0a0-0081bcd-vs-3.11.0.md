# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.07x faster
- HPT reliability: 98.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                |
| chameleon      | 6.70 ms                                                | 7.07 ms: 1.06x slower                                               |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                              |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                               |
| tornado_http   | 98.1 ms                                                | 96.8 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 954 ms: 1.36x faster                                                |
| async_tree_io              | 1.29 sec                                               | 959 ms: 1.34x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                                |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.3 ms: 1.20x faster                                               |
| float          | 78.9 ms                                                | 72.3 ms: 1.09x faster                                               |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                  | 1.10x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                |
| regex_effbot   | 3.51 ms                                                | 3.94 ms: 1.12x slower                                               |
| regex_v8       | 22.9 ms                                                | 25.7 ms: 1.12x slower                                               |
| regex_dna      | 205 ms                                                 | 230 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                  | 1.08x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                               |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                              |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.09x faster                                                |
| pickle_pure_python   | 320 us                                                 | 297 us: 1.08x faster                                                |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                               |
| unpickle_list        | 5.21 us                                                | 5.28 us: 1.01x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 82.8 ms: 1.02x slower                                               |
| xml_etree_process    | 56.9 ms                                                | 58.6 ms: 1.03x slower                                               |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                               |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                               |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                               |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.61 ms: 1.27x slower                                               |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.28x slower                                               |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.00 ms: 1.07x faster                                              |
| genshi_xml      | 53.4 ms                                                | 58.2 ms: 1.09x slower                                               |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                               |
| django_template | 33.5 ms                                                | 36.9 ms: 1.10x slower                                               |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 169 us: 3.08x faster                                                |
| generators                 | 74.9 ms                                                | 30.9 ms: 2.42x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 522 ms: 1.68x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                               |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                |
| async_tree_none            | 528 ms                                                 | 386 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 954 ms: 1.36x faster                                                |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                |
| async_tree_io              | 1.29 sec                                               | 959 ms: 1.34x faster                                                |
| richards_super             | 61.9 ms                                                | 47.3 ms: 1.31x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                               |
| chaos                      | 71.9 ms                                                | 59.3 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 619 ms: 1.21x faster                                                |
| richards                   | 49.8 ms                                                | 41.6 ms: 1.20x faster                                               |
| nbody                      | 96.0 ms                                                | 80.3 ms: 1.20x faster                                               |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                              |
| coroutines                 | 27.0 ms                                                | 23.0 ms: 1.18x faster                                               |
| fannkuch                   | 405 ms                                                 | 350 ms: 1.16x faster                                                |
| scimark_monte_carlo        | 70.7 ms                                                | 62.1 ms: 1.14x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 67.5 ms: 1.14x faster                                               |
| raytrace                   | 309 ms                                                 | 276 ms: 1.12x faster                                                |
| pathlib                    | 18.5 ms                                                | 16.7 ms: 1.11x faster                                               |
| logging_simple             | 6.22 us                                                | 5.62 us: 1.11x faster                                               |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                               |
| scimark_fft                | 345 ms                                                 | 314 ms: 1.10x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.59 ms: 1.09x faster                                               |
| float                      | 78.9 ms                                                | 72.3 ms: 1.09x faster                                               |
| logging_format             | 6.81 us                                                | 6.26 us: 1.09x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.09x faster                                                |
| spectral_norm              | 108 ms                                                 | 99.5 ms: 1.09x faster                                               |
| pickle_pure_python         | 320 us                                                 | 297 us: 1.08x faster                                                |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                              |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                               |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                              |
| mako                       | 10.7 ms                                                | 10.00 ms: 1.07x faster                                              |
| deltablue                  | 3.92 ms                                                | 3.73 ms: 1.05x faster                                               |
| pprint_safe_repr           | 747 ms                                                 | 711 ms: 1.05x faster                                                |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                               |
| hexiom                     | 6.89 ms                                                | 6.58 ms: 1.05x faster                                               |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                |
| gc_traversal               | 4.01 ms                                                | 3.86 ms: 1.04x faster                                               |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                |
| nqueens                    | 87.9 ms                                                | 85.4 ms: 1.03x faster                                               |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                               |
| tornado_http               | 98.1 ms                                                | 96.8 ms: 1.01x faster                                               |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                |
| pyflate                    | 434 ms                                                 | 437 ms: 1.01x slower                                                |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                              |
| unpickle_list              | 5.21 us                                                | 5.28 us: 1.01x slower                                               |
| deepcopy                   | 365 us                                                 | 372 us: 1.02x slower                                                |
| sqlglot_optimize           | 55.3 ms                                                | 56.4 ms: 1.02x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 82.8 ms: 1.02x slower                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                               |
| xml_etree_process          | 56.9 ms                                                | 58.6 ms: 1.03x slower                                               |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                                |
| bench_thread_pool          | 834 us                                                 | 864 us: 1.04x slower                                                |
| sympy_integrate            | 21.5 ms                                                | 22.4 ms: 1.05x slower                                               |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                               |
| thrift                     | 784 us                                                 | 824 us: 1.05x slower                                                |
| sympy_expand               | 484 ms                                                 | 509 ms: 1.05x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.07 ms: 1.06x slower                                               |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.07x slower                                                |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                               |
| dulwich_log                | 64.6 ms                                                | 69.1 ms: 1.07x slower                                               |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.08x slower                                                |
| genshi_xml                 | 53.4 ms                                                | 58.2 ms: 1.09x slower                                               |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                               |
| django_template            | 33.5 ms                                                | 36.9 ms: 1.10x slower                                               |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                               |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                              |
| regex_effbot               | 3.51 ms                                                | 3.94 ms: 1.12x slower                                               |
| regex_v8                   | 22.9 ms                                                | 25.7 ms: 1.12x slower                                               |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.13x slower                                                |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                               |
| coverage                   | 78.8 ms                                                | 92.7 ms: 1.18x slower                                               |
| telco                      | 6.86 ms                                                | 8.16 ms: 1.19x slower                                               |
| async_generators           | 374 ms                                                 | 463 ms: 1.24x slower                                                |
| flaskblogging              | 7.28 ms                                                | 9.21 ms: 1.26x slower                                               |
| python_startup_no_site     | 6.01 ms                                                | 7.61 ms: 1.27x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                               |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.28x slower                                               |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                        |

Benchmark hidden because not significant (4): json, sqlglot_normalize, pickle_dict, bench_mp_pool
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x