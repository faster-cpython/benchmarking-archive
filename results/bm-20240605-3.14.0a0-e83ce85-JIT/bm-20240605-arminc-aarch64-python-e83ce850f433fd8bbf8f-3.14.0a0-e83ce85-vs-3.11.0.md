# Results vs. 3.11.0

- fork: python
- ref: e83ce850f433fd8bbf8f
- machine: linux-aarch64
- commit hash: e83ce85
- commit date: 2024-06-05
- overall geometric mean: 1.02x slower
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 356 ms: 1.19x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.50 sec: 1.20x slower                                                  |
| html5lib       | 65.3 ms                                                               | 72.2 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 504 ms: 1.39x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 607 ms: 1.36x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 663 ms: 1.32x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 478 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.28x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 771 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 811 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                    |
| float          | 89.6 ms                                                               | 90.4 ms: 1.01x slower                                                   |
| nbody          | 113 ms                                                                | 115 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.1 ms: 1.03x slower                                                   |
| regex_dna      | 239 ms                                                                | 250 ms: 1.05x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.87 ms: 1.15x slower                                                   |
| regex_compile  | 137 ms                                                                | 175 ms: 1.28x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 15.4 ms                                                               | 13.1 ms: 1.17x faster                                                   |
| xml_etree_parse     | 209 ms                                                                | 189 ms: 1.11x faster                                                    |
| unpickle_list       | 6.86 us                                                               | 6.63 us: 1.04x faster                                                   |
| xml_etree_iterparse | 152 ms                                                                | 149 ms: 1.02x faster                                                    |
| tomli_loads         | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                                  |
| xml_etree_process   | 76.1 ms                                                               | 79.7 ms: 1.05x slower                                                   |
| pickle_list         | 5.01 us                                                               | 5.27 us: 1.05x slower                                                   |
| json_loads          | 30.3 us                                                               | 32.1 us: 1.06x slower                                                   |
| pickle              | 12.8 us                                                               | 13.7 us: 1.07x slower                                                   |
| pickle_pure_python  | 374 us                                                                | 413 us: 1.10x slower                                                    |
| xml_etree_generate  | 104 ms                                                                | 115 ms: 1.11x slower                                                    |
| unpickle            | 16.9 us                                                               | 19.4 us: 1.15x slower                                                   |
| Geometric mean      | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 15.2 ms: 1.49x slower                                                   |
| python_startup_no_site | 7.35 ms                                                               | 11.0 ms: 1.50x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.49x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                                   |
| genshi_text     | 28.2 ms                                                               | 33.8 ms: 1.20x slower                                                   |
| django_template | 41.8 ms                                                               | 51.2 ms: 1.23x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 83.0 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 207 us: 3.16x faster                                                    |
| generators                 | 64.2 ms                                                               | 38.6 ms: 1.67x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 614 ms: 1.50x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.23 sec: 1.43x faster                                                  |
| async_tree_none            | 701 ms                                                                | 504 ms: 1.39x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 607 ms: 1.36x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 663 ms: 1.32x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 478 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.28x faster                                                  |
| comprehensions             | 29.0 us                                                               | 23.4 us: 1.24x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 771 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 811 ms: 1.18x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.17x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 21.9 ms: 1.13x faster                                                   |
| richards_super             | 70.2 ms                                                               | 62.4 ms: 1.12x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 189 ms: 1.11x faster                                                    |
| raytrace                   | 351 ms                                                                | 326 ms: 1.07x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.59 ms: 1.04x faster                                                   |
| unpickle_list              | 6.86 us                                                               | 6.63 us: 1.04x faster                                                   |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                    |
| deltablue                  | 4.75 ms                                                               | 4.60 ms: 1.03x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.38 us: 1.03x faster                                                   |
| richards                   | 58.1 ms                                                               | 56.7 ms: 1.02x faster                                                   |
| mako                       | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.34 ms: 1.01x faster                                                   |
| tomli_loads                | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                                  |
| asyncio_websockets         | 656 ms                                                                | 661 ms: 1.01x slower                                                    |
| float                      | 89.6 ms                                                               | 90.4 ms: 1.01x slower                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 2.02 ms: 1.01x slower                                                   |
| meteor_contest             | 115 ms                                                                | 117 ms: 1.01x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 49.9 us: 1.02x slower                                                   |
| mdp                        | 3.35 sec                                                              | 3.41 sec: 1.02x slower                                                  |
| nbody                      | 113 ms                                                                | 115 ms: 1.02x slower                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 89.1 ms: 1.03x slower                                                   |
| dask                       | 385 ms                                                                | 397 ms: 1.03x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.1 ms: 1.03x slower                                                   |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                                   |
| fannkuch                   | 451 ms                                                                | 468 ms: 1.04x slower                                                    |
| logging_silent             | 133 ns                                                                | 138 ns: 1.04x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 79.7 ms: 1.05x slower                                                   |
| regex_dna                  | 239 ms                                                                | 250 ms: 1.05x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.27 us: 1.05x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                                   |
| thrift                     | 910 us                                                                | 964 us: 1.06x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.7 us: 1.07x slower                                                   |
| sqlglot_normalize          | 132 ms                                                                | 144 ms: 1.09x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                  |
| sympy_str                  | 295 ms                                                                | 322 ms: 1.09x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.90 us: 1.09x slower                                                   |
| scimark_monte_carlo        | 83.2 ms                                                               | 91.3 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.90 ms: 1.10x slower                                                   |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 413 us: 1.10x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 70.0 ms: 1.11x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 72.2 ms: 1.11x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.23 ms: 1.11x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 115 ms: 1.11x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 187 ms: 1.11x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 25.8 ms: 1.11x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 71.2 ms: 1.13x slower                                                   |
| sympy_expand               | 482 ms                                                                | 546 ms: 1.13x slower                                                    |
| deepcopy                   | 435 us                                                                | 494 us: 1.14x slower                                                    |
| spectral_norm              | 131 ms                                                                | 149 ms: 1.14x slower                                                    |
| scimark_fft                | 402 ms                                                                | 459 ms: 1.14x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.87 ms: 1.15x slower                                                   |
| chaos                      | 78.8 ms                                                               | 90.4 ms: 1.15x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.4 us: 1.15x slower                                                   |
| nqueens                    | 102 ms                                                                | 118 ms: 1.16x slower                                                    |
| pyflate                    | 516 ms                                                                | 603 ms: 1.17x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.07 ms: 1.17x slower                                                   |
| deepcopy_reduce            | 3.89 us                                                               | 4.61 us: 1.19x slower                                                   |
| 2to3                       | 300 ms                                                                | 356 ms: 1.19x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 8.99 ms: 1.19x slower                                                   |
| coverage                   | 84.1 ms                                                               | 100 ms: 1.19x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 33.8 ms: 1.20x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.50 sec: 1.20x slower                                                  |
| scimark_sor                | 145 ms                                                                | 175 ms: 1.20x slower                                                    |
| django_template            | 41.8 ms                                                               | 51.2 ms: 1.23x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.12 sec: 1.24x slower                                                  |
| pprint_pformat             | 1.85 sec                                                              | 2.32 sec: 1.25x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 2.35 ms: 1.26x slower                                                   |
| regex_compile              | 137 ms                                                                | 175 ms: 1.28x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 184 ms: 1.31x slower                                                    |
| telco                      | 7.80 ms                                                               | 10.4 ms: 1.33x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 83.0 ms: 1.33x slower                                                   |
| async_generators           | 378 ms                                                                | 516 ms: 1.37x slower                                                    |
| python_startup             | 10.2 ms                                                               | 15.2 ms: 1.49x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 11.0 ms: 1.50x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (5): logging_format, tornado_http, unpickle_pure_python, pickle_dict, pylint
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.62% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x