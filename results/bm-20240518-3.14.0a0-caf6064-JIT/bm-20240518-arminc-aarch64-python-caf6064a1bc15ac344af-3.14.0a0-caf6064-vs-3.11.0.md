# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-aarch64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.05x slower
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 360 ms: 1.20x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.20 ms: 1.11x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| html5lib       | 65.3 ms                                                               | 70.6 ms: 1.08x slower                                                   |
| tornado_http   | 140 ms                                                                | 145 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 497 ms: 1.41x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 617 ms: 1.34x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 655 ms: 1.33x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.30x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.25 sec: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 807 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 813 ms: 1.13x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                                    |
| nbody          | 113 ms                                                                | 114 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                   |
| regex_dna      | 239 ms                                                                | 251 ms: 1.05x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                   |
| regex_compile  | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| xml_etree_parse      | 209 ms                                                                | 188 ms: 1.11x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.55 us: 1.05x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 276 us: 1.01x faster                                                    |
| tomli_loads          | 2.62 sec                                                              | 2.65 sec: 1.01x slower                                                  |
| pickle_dict          | 37.6 us                                                               | 38.2 us: 1.02x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 387 us: 1.04x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.1 us: 1.06x slower                                                   |
| pickle_list          | 5.01 us                                                               | 5.32 us: 1.06x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 81.0 ms: 1.06x slower                                                   |
| pickle               | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| xml_etree_generate   | 104 ms                                                                | 117 ms: 1.12x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.9 ms: 1.46x slower                                                   |
| python_startup_no_site | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.1 ms: 1.02x faster                                                   |
| django_template | 41.8 ms                                                               | 49.6 ms: 1.19x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 35.2 ms: 1.25x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 83.5 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 208 us: 3.14x faster                                                    |
| generators                 | 64.2 ms                                                               | 38.3 ms: 1.68x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 615 ms: 1.50x faster                                                    |
| async_tree_none            | 701 ms                                                                | 497 ms: 1.41x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.27 sec: 1.40x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 617 ms: 1.34x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 655 ms: 1.33x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.30x faster                                                  |
| comprehensions             | 29.0 us                                                               | 23.0 us: 1.26x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.25 sec: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 807 ms: 1.18x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                   |
| richards_super             | 70.2 ms                                                               | 61.7 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 813 ms: 1.13x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 22.0 ms: 1.13x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 188 ms: 1.11x faster                                                    |
| raytrace                   | 351 ms                                                                | 325 ms: 1.08x faster                                                    |
| richards                   | 58.1 ms                                                               | 54.1 ms: 1.07x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.79 us: 1.05x faster                                                   |
| unpickle_list              | 6.86 us                                                               | 6.55 us: 1.05x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.24 us: 1.05x faster                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.58 ms: 1.04x faster                                                   |
| deltablue                  | 4.75 ms                                                               | 4.58 ms: 1.04x faster                                                   |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.32 ms: 1.02x faster                                                   |
| mako                       | 13.3 ms                                                               | 13.1 ms: 1.02x faster                                                   |
| unpickle_pure_python       | 278 us                                                                | 276 us: 1.01x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.01 ms: 1.01x slower                                                   |
| nbody                      | 113 ms                                                                | 114 ms: 1.01x slower                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.65 sec: 1.01x slower                                                  |
| asyncio_websockets         | 656 ms                                                                | 665 ms: 1.01x slower                                                    |
| pickle_dict                | 37.6 us                                                               | 38.2 us: 1.02x slower                                                   |
| deepcopy_memo              | 49.0 us                                                               | 50.0 us: 1.02x slower                                                   |
| dask                       | 385 ms                                                                | 393 ms: 1.02x slower                                                    |
| meteor_contest             | 115 ms                                                                | 119 ms: 1.03x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 387 us: 1.04x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.48 sec: 1.04x slower                                                  |
| json                       | 5.52 ms                                                               | 5.72 ms: 1.04x slower                                                   |
| tornado_http               | 140 ms                                                                | 145 ms: 1.04x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                   |
| thrift                     | 910 us                                                                | 953 us: 1.05x slower                                                    |
| regex_dna                  | 239 ms                                                                | 251 ms: 1.05x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 87.5 ms: 1.05x slower                                                   |
| logging_silent             | 133 ns                                                                | 140 ns: 1.05x slower                                                    |
| fannkuch                   | 451 ms                                                                | 477 ms: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.32 us: 1.06x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 81.0 ms: 1.06x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.82 us: 1.07x slower                                                   |
| sympy_str                  | 295 ms                                                                | 317 ms: 1.08x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 70.6 ms: 1.08x slower                                                   |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                  |
| sympy_sum                  | 168 ms                                                                | 184 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.88 ms: 1.09x slower                                                   |
| sqlglot_normalize          | 132 ms                                                                | 145 ms: 1.10x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 69.8 ms: 1.10x slower                                                   |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 69.7 ms: 1.10x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 9.20 ms: 1.11x slower                                                   |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.11x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.0 ms: 1.12x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 117 ms: 1.12x slower                                                    |
| chaos                      | 78.8 ms                                                               | 88.5 ms: 1.12x slower                                                   |
| sympy_expand               | 482 ms                                                                | 541 ms: 1.12x slower                                                    |
| scimark_fft                | 402 ms                                                                | 456 ms: 1.13x slower                                                    |
| deepcopy                   | 435 us                                                                | 494 us: 1.14x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                   |
| nqueens                    | 102 ms                                                                | 119 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.66 ms: 1.17x slower                                                   |
| django_template            | 41.8 ms                                                               | 49.6 ms: 1.19x slower                                                   |
| coverage                   | 84.1 ms                                                               | 100 ms: 1.19x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.18 ms: 1.20x slower                                                   |
| hexiom                     | 7.57 ms                                                               | 9.07 ms: 1.20x slower                                                   |
| 2to3                       | 300 ms                                                                | 360 ms: 1.20x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.67 us: 1.20x slower                                                   |
| pyflate                    | 516 ms                                                                | 623 ms: 1.21x slower                                                    |
| scimark_sor                | 145 ms                                                                | 176 ms: 1.21x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| pprint_safe_repr           | 903 ms                                                                | 1.10 sec: 1.22x slower                                                  |
| pprint_pformat             | 1.85 sec                                                              | 2.28 sec: 1.23x slower                                                  |
| flaskblogging              | 4.19 ms                                                               | 5.23 ms: 1.25x slower                                                   |
| regex_compile              | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 35.2 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.42 ms: 1.29x slower                                                   |
| scimark_lu                 | 140 ms                                                                | 182 ms: 1.30x slower                                                    |
| genshi_xml                 | 62.2 ms                                                               | 83.5 ms: 1.34x slower                                                   |
| async_generators           | 378 ms                                                                | 514 ms: 1.36x slower                                                    |
| python_startup             | 10.2 ms                                                               | 14.9 ms: 1.46x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                   |
| telco                      | 7.80 ms                                                               | 167 ms: 21.35x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                                            |

Benchmark hidden because not significant (4): crypto_pyaes, float, xml_etree_iterparse, pylint
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.85% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x