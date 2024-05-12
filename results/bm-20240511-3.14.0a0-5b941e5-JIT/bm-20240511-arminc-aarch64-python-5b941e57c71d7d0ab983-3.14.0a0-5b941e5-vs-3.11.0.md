# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: linux-aarch64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.06x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 364 ms: 1.21x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.32 ms: 1.12x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.56 sec: 1.22x slower                                                  |
| html5lib       | 65.3 ms                                                               | 70.7 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 499 ms: 1.41x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 617 ms: 1.34x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 656 ms: 1.33x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 476 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.24 sec: 1.29x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 801 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 811 ms: 1.14x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                                    |
| nbody          | 113 ms                                                                | 114 ms: 1.01x slower                                                    |
| float          | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                   |
| regex_dna      | 239 ms                                                                | 255 ms: 1.07x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.95 ms: 1.16x slower                                                   |
| regex_compile  | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps         | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| xml_etree_parse    | 209 ms                                                                | 193 ms: 1.08x faster                                                    |
| unpickle_list      | 6.86 us                                                               | 6.35 us: 1.08x faster                                                   |
| pickle_pure_python | 374 us                                                                | 394 us: 1.05x slower                                                    |
| pickle_list        | 5.01 us                                                               | 5.28 us: 1.05x slower                                                   |
| xml_etree_process  | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                   |
| json_loads         | 30.3 us                                                               | 32.3 us: 1.06x slower                                                   |
| xml_etree_generate | 104 ms                                                                | 113 ms: 1.08x slower                                                    |
| pickle             | 12.8 us                                                               | 14.1 us: 1.10x slower                                                   |
| unpickle           | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (4): unpickle_pure_python, xml_etree_iterparse, tomli_loads, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.8 ms: 1.46x slower                                                   |
| python_startup_no_site | 7.35 ms                                                               | 10.8 ms: 1.48x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.47x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.1 ms: 1.01x faster                                                   |
| django_template | 41.8 ms                                                               | 49.8 ms: 1.19x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 34.4 ms: 1.22x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 81.9 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 207 us: 3.16x faster                                                    |
| generators                 | 64.2 ms                                                               | 38.7 ms: 1.66x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 605 ms: 1.52x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.26 sec: 1.41x faster                                                  |
| async_tree_none            | 701 ms                                                                | 499 ms: 1.41x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 617 ms: 1.34x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 656 ms: 1.33x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 476 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.24 sec: 1.29x faster                                                  |
| comprehensions             | 29.0 us                                                               | 22.9 us: 1.26x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 801 ms: 1.19x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                   |
| richards_super             | 70.2 ms                                                               | 61.3 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 811 ms: 1.14x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 193 ms: 1.08x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.35 us: 1.08x faster                                                   |
| raytrace                   | 351 ms                                                                | 325 ms: 1.08x faster                                                    |
| richards                   | 58.1 ms                                                               | 54.1 ms: 1.07x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 23.2 ms: 1.07x faster                                                   |
| deltablue                  | 4.75 ms                                                               | 4.56 ms: 1.04x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.92 us: 1.04x faster                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.60 ms: 1.03x faster                                                   |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                   |
| mako                       | 13.3 ms                                                               | 13.1 ms: 1.01x faster                                                   |
| nbody                      | 113 ms                                                                | 114 ms: 1.01x slower                                                    |
| float                      | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                                   |
| asyncio_websockets         | 656 ms                                                                | 665 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.04 ms: 1.02x slower                                                   |
| deepcopy_memo              | 49.0 us                                                               | 50.1 us: 1.02x slower                                                   |
| meteor_contest             | 115 ms                                                                | 119 ms: 1.03x slower                                                    |
| json                       | 5.52 ms                                                               | 5.69 ms: 1.03x slower                                                   |
| dask                       | 385 ms                                                                | 397 ms: 1.03x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.48 sec: 1.04x slower                                                  |
| logging_silent             | 133 ns                                                                | 139 ns: 1.05x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 87.4 ms: 1.05x slower                                                   |
| fannkuch                   | 451 ms                                                                | 475 ms: 1.05x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 394 us: 1.05x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.28 us: 1.05x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                   |
| thrift                     | 910 us                                                                | 966 us: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.06x slower                                                   |
| regex_dna                  | 239 ms                                                                | 255 ms: 1.07x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.80 us: 1.07x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 70.7 ms: 1.08x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.08x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 144 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.84 ms: 1.09x slower                                                   |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                  |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                    |
| pickle                     | 12.8 us                                                               | 14.1 us: 1.10x slower                                                   |
| sqlglot_optimize           | 63.4 ms                                                               | 69.9 ms: 1.10x slower                                                   |
| sympy_str                  | 295 ms                                                                | 326 ms: 1.11x slower                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 8.24 ms: 1.11x slower                                                   |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.11x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 189 ms: 1.12x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 9.32 ms: 1.12x slower                                                   |
| chaos                      | 78.8 ms                                                               | 88.7 ms: 1.12x slower                                                   |
| scimark_fft                | 402 ms                                                                | 455 ms: 1.13x slower                                                    |
| deepcopy                   | 435 us                                                                | 495 us: 1.14x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 71.8 ms: 1.14x slower                                                   |
| sympy_integrate            | 23.2 ms                                                               | 26.4 ms: 1.14x slower                                                   |
| sympy_expand               | 482 ms                                                                | 554 ms: 1.15x slower                                                    |
| nqueens                    | 102 ms                                                                | 118 ms: 1.15x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.95 ms: 1.16x slower                                                   |
| hexiom                     | 7.57 ms                                                               | 8.99 ms: 1.19x slower                                                   |
| django_template            | 41.8 ms                                                               | 49.8 ms: 1.19x slower                                                   |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                    |
| pyflate                    | 516 ms                                                                | 619 ms: 1.20x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.67 us: 1.20x slower                                                   |
| scimark_sor                | 145 ms                                                                | 176 ms: 1.21x slower                                                    |
| 2to3                       | 300 ms                                                                | 364 ms: 1.21x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.56 sec: 1.22x slower                                                  |
| flaskblogging              | 4.19 ms                                                               | 5.12 ms: 1.22x slower                                                   |
| genshi_text                | 28.2 ms                                                               | 34.4 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.11 sec: 1.23x slower                                                  |
| pprint_pformat             | 1.85 sec                                                              | 2.29 sec: 1.23x slower                                                  |
| gc_traversal               | 4.33 ms                                                               | 5.35 ms: 1.24x slower                                                   |
| regex_compile              | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 182 ms: 1.30x slower                                                    |
| genshi_xml                 | 62.2 ms                                                               | 81.9 ms: 1.31x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.49 ms: 1.33x slower                                                   |
| async_generators           | 378 ms                                                                | 513 ms: 1.36x slower                                                    |
| python_startup             | 10.2 ms                                                               | 14.8 ms: 1.46x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 10.8 ms: 1.48x slower                                                   |
| telco                      | 7.80 ms                                                               | 166 ms: 21.22x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.06x slower                                                            |

Benchmark hidden because not significant (8): logging_simple, unpickle_pure_python, xml_etree_iterparse, tomli_loads, pickle_dict, crypto_pyaes, tornado_http, pylint
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x