# Results vs. 3.11.0

- fork: mdboom
- ref: aa_test2
- machine: linux-aarch64
- commit hash: fa824fe
- commit date: 2024-05-03
- overall geometric mean: 1.05x faster
- HPT reliability: 99.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 302 ms: 1.01x slower                                         |
| chameleon      | 8.29 ms                                                               | 9.17 ms: 1.11x slower                                        |
| docutils       | 2.92 sec                                                              | 3.10 sec: 1.06x slower                                       |
| tornado_http   | 140 ms                                                                | 128 ms: 1.09x faster                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 494 ms: 1.42x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 650 ms: 1.34x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 620 ms: 1.34x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.30x faster                                       |
| async_tree_io_tg           | 1.54 sec                                                              | 1.21 sec: 1.26x faster                                       |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 785 ms: 1.17x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                         |
| nbody          | 113 ms                                                                | 111 ms: 1.01x faster                                         |
| float          | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| regex_dna      | 239 ms                                                                | 249 ms: 1.04x slower                                         |
| regex_v8       | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                        |
| regex_effbot   | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                        |
| unpickle_pure_python | 278 us                                                                | 248 us: 1.12x faster                                         |
| xml_etree_parse      | 209 ms                                                                | 188 ms: 1.11x faster                                         |
| unpickle_list        | 6.86 us                                                               | 6.32 us: 1.09x faster                                        |
| tomli_loads          | 2.62 sec                                                              | 2.53 sec: 1.03x faster                                       |
| pickle_pure_python   | 374 us                                                                | 363 us: 1.03x faster                                         |
| xml_etree_iterparse  | 152 ms                                                                | 148 ms: 1.03x faster                                         |
| pickle_dict          | 37.6 us                                                               | 37.6 us: 1.00x slower                                        |
| pickle               | 12.8 us                                                               | 13.5 us: 1.05x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 80.5 ms: 1.06x slower                                        |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.36 us: 1.07x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| unpickle             | 16.9 us                                                               | 19.9 us: 1.18x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.35 ms: 1.14x slower                                        |
| python_startup         | 10.2 ms                                                               | 12.5 ms: 1.22x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.18x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                        |
| genshi_text    | 28.2 ms                                                               | 27.8 ms: 1.01x faster                                        |
| mako           | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 193 us: 3.39x faster                                         |
| generators                 | 64.2 ms                                                               | 37.7 ms: 1.70x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 561 ms: 1.64x faster                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.21 sec: 1.44x faster                                       |
| async_tree_none            | 701 ms                                                                | 494 ms: 1.42x faster                                         |
| comprehensions             | 29.0 us                                                               | 20.5 us: 1.42x faster                                        |
| async_tree_memoization     | 872 ms                                                                | 650 ms: 1.34x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 620 ms: 1.34x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.30x faster                                       |
| async_tree_io_tg           | 1.54 sec                                                              | 1.21 sec: 1.26x faster                                       |
| deltablue                  | 4.75 ms                                                               | 3.88 ms: 1.22x faster                                        |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.38 ms: 1.19x faster                                        |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                         |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 785 ms: 1.17x faster                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.71 ms: 1.17x faster                                        |
| sympy_sum                  | 168 ms                                                                | 145 ms: 1.16x faster                                         |
| pylint                     | 397 ms                                                                | 342 ms: 1.16x faster                                         |
| chaos                      | 78.8 ms                                                               | 68.1 ms: 1.16x faster                                        |
| richards_super             | 70.2 ms                                                               | 61.0 ms: 1.15x faster                                        |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                        |
| unpickle_pure_python       | 278 us                                                                | 248 us: 1.12x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 188 ms: 1.11x faster                                         |
| sympy_str                  | 295 ms                                                                | 265 ms: 1.11x faster                                         |
| dulwich_log                | 63.2 ms                                                               | 57.1 ms: 1.11x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 21.1 ms: 1.10x faster                                        |
| tornado_http               | 140 ms                                                                | 128 ms: 1.09x faster                                         |
| pathlib                    | 24.8 ms                                                               | 22.7 ms: 1.09x faster                                        |
| unpickle_list              | 6.86 us                                                               | 6.32 us: 1.09x faster                                        |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.07x faster                                        |
| crypto_pyaes               | 86.5 ms                                                               | 80.7 ms: 1.07x faster                                        |
| hexiom                     | 7.57 ms                                                               | 7.07 ms: 1.07x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.09 us: 1.07x faster                                        |
| regex_compile              | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| sympy_expand               | 482 ms                                                                | 455 ms: 1.06x faster                                         |
| logging_format             | 8.22 us                                                               | 7.76 us: 1.06x faster                                        |
| richards                   | 58.1 ms                                                               | 55.5 ms: 1.05x faster                                        |
| dask                       | 385 ms                                                                | 369 ms: 1.04x faster                                         |
| nqueens                    | 102 ms                                                                | 98.3 ms: 1.04x faster                                        |
| bench_mp_pool              | 7.44 ms                                                               | 7.14 ms: 1.04x faster                                        |
| sqlglot_normalize          | 132 ms                                                                | 127 ms: 1.04x faster                                         |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                         |
| tomli_loads                | 2.62 sec                                                              | 2.53 sec: 1.03x faster                                       |
| scimark_lu                 | 140 ms                                                                | 136 ms: 1.03x faster                                         |
| pickle_pure_python         | 374 us                                                                | 363 us: 1.03x faster                                         |
| xml_etree_iterparse        | 152 ms                                                                | 148 ms: 1.03x faster                                         |
| genshi_xml                 | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 61.9 ms: 1.02x faster                                        |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                         |
| pycparser                  | 1.25 sec                                                              | 1.22 sec: 1.02x faster                                       |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                         |
| genshi_text                | 28.2 ms                                                               | 27.8 ms: 1.01x faster                                        |
| mdp                        | 3.35 sec                                                              | 3.31 sec: 1.01x faster                                       |
| nbody                      | 113 ms                                                                | 111 ms: 1.01x faster                                         |
| scimark_monte_carlo        | 83.2 ms                                                               | 82.5 ms: 1.01x faster                                        |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| pickle_dict                | 37.6 us                                                               | 37.6 us: 1.00x slower                                        |
| asyncio_websockets         | 656 ms                                                                | 658 ms: 1.00x slower                                         |
| deepcopy_memo              | 49.0 us                                                               | 49.4 us: 1.01x slower                                        |
| 2to3                       | 300 ms                                                                | 302 ms: 1.01x slower                                         |
| fannkuch                   | 451 ms                                                                | 456 ms: 1.01x slower                                         |
| logging_silent             | 133 ns                                                                | 134 ns: 1.01x slower                                         |
| float                      | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                        |
| gunicorn                   | 1.19 ms                                                               | 1.21 ms: 1.02x slower                                        |
| deepcopy                   | 435 us                                                                | 445 us: 1.02x slower                                         |
| aiohttp                    | 1.13 ms                                                               | 1.17 ms: 1.03x slower                                        |
| thrift                     | 910 us                                                                | 942 us: 1.04x slower                                         |
| json                       | 5.52 ms                                                               | 5.72 ms: 1.04x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.52 ms: 1.04x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 1.93 sec: 1.04x slower                                       |
| pprint_safe_repr           | 903 ms                                                                | 939 ms: 1.04x slower                                         |
| regex_dna                  | 239 ms                                                                | 249 ms: 1.04x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 4.08 us: 1.05x slower                                        |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.05x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 80.5 ms: 1.06x slower                                        |
| docutils                   | 2.92 sec                                                              | 3.10 sec: 1.06x slower                                       |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.36 us: 1.07x slower                                        |
| regex_v8                   | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                        |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.07x slower                                         |
| pyflate                    | 516 ms                                                                | 558 ms: 1.08x slower                                         |
| sqlite_synth               | 3.56 us                                                               | 3.88 us: 1.09x slower                                        |
| scimark_sor                | 145 ms                                                                | 159 ms: 1.09x slower                                         |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| scimark_fft                | 402 ms                                                                | 445 ms: 1.11x slower                                         |
| chameleon                  | 8.29 ms                                                               | 9.17 ms: 1.11x slower                                        |
| flaskblogging              | 4.19 ms                                                               | 4.73 ms: 1.13x slower                                        |
| python_startup_no_site     | 7.35 ms                                                               | 8.35 ms: 1.14x slower                                        |
| regex_effbot               | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 5.01 ms: 1.16x slower                                        |
| coverage                   | 84.1 ms                                                               | 99.0 ms: 1.18x slower                                        |
| unpickle                   | 16.9 us                                                               | 19.9 us: 1.18x slower                                        |
| create_gc_cycles           | 1.87 ms                                                               | 2.27 ms: 1.21x slower                                        |
| python_startup             | 10.2 ms                                                               | 12.5 ms: 1.22x slower                                        |
| async_generators           | 378 ms                                                                | 484 ms: 1.28x slower                                         |
| telco                      | 7.80 ms                                                               | 10.1 ms: 1.29x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (2): django_template, html5lib
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.44% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x