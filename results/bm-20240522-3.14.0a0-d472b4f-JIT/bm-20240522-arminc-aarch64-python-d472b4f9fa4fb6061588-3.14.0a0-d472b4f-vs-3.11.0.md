# Results vs. 3.11.0

- fork: python
- ref: d472b4f9fa4fb6061588
- machine: linux-aarch64
- commit hash: d472b4f
- commit date: 2024-05-22
- overall geometric mean: 1.03x slower
- HPT reliability: 99.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 361 ms: 1.20x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.28 ms: 1.12x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.56 sec: 1.22x slower                                                  |
| html5lib       | 65.3 ms                                                               | 71.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 517 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 633 ms: 1.31x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 684 ms: 1.28x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 489 ms: 1.27x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 825 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 801 ms: 1.15x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| float          | 89.6 ms                                                               | 91.4 ms: 1.02x slower                                                   |
| nbody          | 113 ms                                                                | 116 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.5 ms: 1.05x slower                                                   |
| regex_dna      | 239 ms                                                                | 254 ms: 1.06x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.91 ms: 1.15x slower                                                   |
| regex_compile  | 137 ms                                                                | 172 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps         | 15.4 ms                                                               | 13.2 ms: 1.16x faster                                                   |
| xml_etree_parse    | 209 ms                                                                | 189 ms: 1.11x faster                                                    |
| unpickle_list      | 6.86 us                                                               | 6.41 us: 1.07x faster                                                   |
| tomli_loads        | 2.62 sec                                                              | 2.63 sec: 1.01x slower                                                  |
| pickle_list        | 5.01 us                                                               | 5.21 us: 1.04x slower                                                   |
| xml_etree_process  | 76.1 ms                                                               | 80.4 ms: 1.06x slower                                                   |
| pickle_pure_python | 374 us                                                                | 398 us: 1.06x slower                                                    |
| json_loads         | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| pickle             | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| xml_etree_generate | 104 ms                                                                | 113 ms: 1.09x slower                                                    |
| unpickle           | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.8 ms: 1.46x slower                                                   |
| python_startup_no_site | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                   |
| django_template | 41.8 ms                                                               | 51.5 ms: 1.23x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 35.3 ms: 1.25x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 83.8 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240522-arminc-aarch64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 208 us: 3.13x faster                                                    |
| generators                 | 64.2 ms                                                               | 38.6 ms: 1.66x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 617 ms: 1.49x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.26 sec: 1.41x faster                                                  |
| async_tree_none            | 701 ms                                                                | 517 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 633 ms: 1.31x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 684 ms: 1.28x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 489 ms: 1.27x faster                                                    |
| comprehensions             | 29.0 us                                                               | 23.1 us: 1.25x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                  |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 825 ms: 1.16x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 801 ms: 1.15x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 21.6 ms: 1.15x faster                                                   |
| richards_super             | 70.2 ms                                                               | 61.4 ms: 1.14x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 189 ms: 1.11x faster                                                    |
| raytrace                   | 351 ms                                                                | 324 ms: 1.08x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.41 us: 1.07x faster                                                   |
| richards                   | 58.1 ms                                                               | 54.7 ms: 1.06x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.32 us: 1.03x faster                                                   |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.60 ms: 1.03x faster                                                   |
| deltablue                  | 4.75 ms                                                               | 4.62 ms: 1.03x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.99 us: 1.03x faster                                                   |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                   |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 2.01 ms: 1.00x slower                                                   |
| tomli_loads                | 2.62 sec                                                              | 2.63 sec: 1.01x slower                                                  |
| meteor_contest             | 115 ms                                                                | 117 ms: 1.01x slower                                                    |
| asyncio_websockets         | 656 ms                                                                | 664 ms: 1.01x slower                                                    |
| fannkuch                   | 451 ms                                                                | 460 ms: 1.02x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 50.0 us: 1.02x slower                                                   |
| float                      | 89.6 ms                                                               | 91.4 ms: 1.02x slower                                                   |
| nbody                      | 113 ms                                                                | 116 ms: 1.03x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.46 sec: 1.03x slower                                                  |
| json                       | 5.52 ms                                                               | 5.72 ms: 1.04x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.21 us: 1.04x slower                                                   |
| crypto_pyaes               | 86.5 ms                                                               | 90.7 ms: 1.05x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.5 ms: 1.05x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 80.4 ms: 1.06x slower                                                   |
| logging_silent             | 133 ns                                                                | 140 ns: 1.06x slower                                                    |
| regex_dna                  | 239 ms                                                                | 254 ms: 1.06x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 398 us: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| thrift                     | 910 us                                                                | 972 us: 1.07x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.86 us: 1.08x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                  |
| sqlglot_normalize          | 132 ms                                                                | 144 ms: 1.09x slower                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 8.11 ms: 1.09x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 71.4 ms: 1.09x slower                                                   |
| sympy_str                  | 295 ms                                                                | 323 ms: 1.10x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 184 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.91 ms: 1.10x slower                                                   |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 70.3 ms: 1.11x slower                                                   |
| scimark_monte_carlo        | 83.2 ms                                                               | 92.8 ms: 1.12x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 9.28 ms: 1.12x slower                                                   |
| spectral_norm              | 131 ms                                                                | 147 ms: 1.12x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.0 ms: 1.12x slower                                                   |
| sympy_expand               | 482 ms                                                                | 541 ms: 1.12x slower                                                    |
| chaos                      | 78.8 ms                                                               | 88.8 ms: 1.13x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 71.9 ms: 1.14x slower                                                   |
| scimark_fft                | 402 ms                                                                | 461 ms: 1.15x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.91 ms: 1.15x slower                                                   |
| deepcopy                   | 435 us                                                                | 503 us: 1.16x slower                                                    |
| nqueens                    | 102 ms                                                                | 119 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.10 ms: 1.18x slower                                                   |
| coverage                   | 84.1 ms                                                               | 99.6 ms: 1.19x slower                                                   |
| hexiom                     | 7.57 ms                                                               | 9.07 ms: 1.20x slower                                                   |
| 2to3                       | 300 ms                                                                | 361 ms: 1.20x slower                                                    |
| scimark_sor                | 145 ms                                                                | 175 ms: 1.20x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.72 us: 1.22x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.56 sec: 1.22x slower                                                  |
| flaskblogging              | 4.19 ms                                                               | 5.12 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.10 sec: 1.22x slower                                                  |
| pyflate                    | 516 ms                                                                | 633 ms: 1.23x slower                                                    |
| django_template            | 41.8 ms                                                               | 51.5 ms: 1.23x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.30 sec: 1.24x slower                                                  |
| genshi_text                | 28.2 ms                                                               | 35.3 ms: 1.25x slower                                                   |
| regex_compile              | 137 ms                                                                | 172 ms: 1.26x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.42 ms: 1.29x slower                                                   |
| scimark_lu                 | 140 ms                                                                | 183 ms: 1.30x slower                                                    |
| telco                      | 7.80 ms                                                               | 10.3 ms: 1.31x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 83.8 ms: 1.35x slower                                                   |
| async_generators           | 378 ms                                                                | 511 ms: 1.35x slower                                                    |
| python_startup             | 10.2 ms                                                               | 14.8 ms: 1.46x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.03x slower                                                            |

Benchmark hidden because not significant (6): tornado_http, unpickle_pure_python, xml_etree_iterparse, pickle_dict, dask, pylint
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.77% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x