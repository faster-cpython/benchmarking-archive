# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-aarch64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.11x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 353 ms: 1.17x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.93 ms: 1.20x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.51 sec: 1.20x slower                                                  |
| html5lib       | 65.3 ms                                                               | 73.7 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 665 ms: 1.31x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.28x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 646 ms: 1.28x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 814 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 816 ms: 1.13x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| nbody          | 113 ms                                                                | 137 ms: 1.22x slower                                                    |
| float          | 89.6 ms                                                               | 113 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 249 ms: 1.04x slower                                                    |
| regex_v8       | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                   |
| regex_effbot   | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                                   |
| regex_compile  | 137 ms                                                                | 166 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.9 ms: 1.11x faster                                                   |
| xml_etree_parse      | 209 ms                                                                | 195 ms: 1.07x faster                                                    |
| pickle_list          | 5.01 us                                                               | 5.28 us: 1.05x slower                                                   |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| pickle               | 12.8 us                                                               | 14.0 us: 1.09x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 87.2 ms: 1.15x slower                                                   |
| unpickle             | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 440 us: 1.18x slower                                                    |
| tomli_loads          | 2.62 sec                                                              | 3.09 sec: 1.18x slower                                                  |
| xml_etree_generate   | 104 ms                                                                | 125 ms: 1.20x slower                                                    |
| unpickle_pure_python | 278 us                                                                | 349 us: 1.25x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.08x slower                                                            |

Benchmark hidden because not significant (2): unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.62 ms: 1.17x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.6 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 48.9 ms: 1.17x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 76.1 ms: 1.22x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 35.6 ms: 1.27x slower                                                   |
| mako            | 13.3 ms                                                               | 16.8 ms: 1.27x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 227 us: 2.88x faster                                                    |
| generators                 | 64.2 ms                                                               | 39.5 ms: 1.63x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 592 ms: 1.55x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.26 sec: 1.41x faster                                                  |
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 665 ms: 1.31x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.28x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 646 ms: 1.28x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 814 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 816 ms: 1.13x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.9 ms: 1.11x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 22.8 ms: 1.09x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 30.8 ms: 1.08x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 195 ms: 1.07x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.38 us: 1.03x faster                                                   |
| raytrace                   | 351 ms                                                                | 342 ms: 1.02x faster                                                    |
| pidigits                   | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| logging_format             | 8.22 us                                                               | 8.07 us: 1.02x faster                                                   |
| asyncio_websockets         | 656 ms                                                                | 668 ms: 1.02x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 65.2 ms: 1.03x slower                                                   |
| richards_super             | 70.2 ms                                                               | 72.5 ms: 1.03x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 7.71 ms: 1.04x slower                                                   |
| comprehensions             | 29.0 us                                                               | 30.1 us: 1.04x slower                                                   |
| regex_dna                  | 239 ms                                                                | 249 ms: 1.04x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 175 ms: 1.04x slower                                                    |
| json                       | 5.52 ms                                                               | 5.81 ms: 1.05x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.28 us: 1.05x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.59 sec: 1.07x slower                                                  |
| regex_v8                   | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.77 ms: 1.07x slower                                                   |
| sympy_str                  | 295 ms                                                                | 317 ms: 1.08x slower                                                    |
| thrift                     | 910 us                                                                | 983 us: 1.08x slower                                                    |
| deltablue                  | 4.75 ms                                                               | 5.14 ms: 1.08x slower                                                   |
| sympy_expand               | 482 ms                                                                | 522 ms: 1.08x slower                                                    |
| chaos                      | 78.8 ms                                                               | 85.6 ms: 1.09x slower                                                   |
| pickle                     | 12.8 us                                                               | 14.0 us: 1.09x slower                                                   |
| pycparser                  | 1.25 sec                                                              | 1.37 sec: 1.10x slower                                                  |
| richards                   | 58.1 ms                                                               | 64.4 ms: 1.11x slower                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 2.22 ms: 1.11x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.98 us: 1.12x slower                                                   |
| sympy_integrate            | 23.2 ms                                                               | 25.9 ms: 1.12x slower                                                   |
| sqlglot_normalize          | 132 ms                                                                | 149 ms: 1.12x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 73.7 ms: 1.13x slower                                                   |
| sqlglot_optimize           | 63.4 ms                                                               | 72.3 ms: 1.14x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 87.2 ms: 1.15x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                                   |
| meteor_contest             | 115 ms                                                                | 133 ms: 1.15x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| django_template            | 41.8 ms                                                               | 48.9 ms: 1.17x slower                                                   |
| crypto_pyaes               | 86.5 ms                                                               | 101 ms: 1.17x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.62 ms: 1.17x slower                                                   |
| 2to3                       | 300 ms                                                                | 353 ms: 1.17x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 440 us: 1.18x slower                                                    |
| tomli_loads                | 2.62 sec                                                              | 3.09 sec: 1.18x slower                                                  |
| coverage                   | 84.1 ms                                                               | 100 ms: 1.19x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 5.02 ms: 1.20x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 9.93 ms: 1.20x slower                                                   |
| go                         | 163 ms                                                                | 195 ms: 1.20x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.51 sec: 1.20x slower                                                  |
| xml_etree_generate         | 104 ms                                                                | 125 ms: 1.20x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.25 ms: 1.21x slower                                                   |
| regex_compile              | 137 ms                                                                | 166 ms: 1.22x slower                                                    |
| nbody                      | 113 ms                                                                | 137 ms: 1.22x slower                                                    |
| genshi_xml                 | 62.2 ms                                                               | 76.1 ms: 1.22x slower                                                   |
| deepcopy                   | 435 us                                                                | 535 us: 1.23x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.80 us: 1.24x slower                                                   |
| python_startup             | 10.2 ms                                                               | 12.6 ms: 1.24x slower                                                   |
| unpickle_pure_python       | 278 us                                                                | 349 us: 1.25x slower                                                    |
| float                      | 89.6 ms                                                               | 113 ms: 1.26x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 35.6 ms: 1.27x slower                                                   |
| mako                       | 13.3 ms                                                               | 16.8 ms: 1.27x slower                                                   |
| nqueens                    | 102 ms                                                                | 130 ms: 1.27x slower                                                    |
| fannkuch                   | 451 ms                                                                | 574 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 8.05 ms: 1.28x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.41 sec: 1.30x slower                                                  |
| pprint_safe_repr           | 903 ms                                                                | 1.18 sec: 1.31x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 2.47 ms: 1.32x slower                                                   |
| scimark_fft                | 402 ms                                                                | 539 ms: 1.34x slower                                                    |
| scimark_sor                | 145 ms                                                                | 198 ms: 1.36x slower                                                    |
| async_generators           | 378 ms                                                                | 517 ms: 1.37x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 114 ms: 1.37x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 10.5 ms: 1.39x slower                                                   |
| pyflate                    | 516 ms                                                                | 727 ms: 1.41x slower                                                    |
| spectral_norm              | 131 ms                                                                | 185 ms: 1.41x slower                                                    |
| logging_silent             | 133 ns                                                                | 189 ns: 1.42x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 71.9 us: 1.47x slower                                                   |
| scimark_lu                 | 140 ms                                                                | 207 ms: 1.48x slower                                                    |
| telco                      | 7.80 ms                                                               | 168 ms: 21.55x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                            |

Benchmark hidden because not significant (6): unpickle_list, tornado_http, pylint, bench_thread_pool, pickle_dict, dask
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.05x