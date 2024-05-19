# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-aarch64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.02x faster
- HPT reliability: 98.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 303 ms: 1.01x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.03 ms: 1.09x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| html5lib       | 65.3 ms                                                               | 68.3 ms: 1.05x slower                                                   |
| tornado_http   | 140 ms                                                                | 131 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 486 ms: 1.44x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 785 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 792 ms: 1.16x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| float          | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 131 ms: 1.04x faster                                                    |
| regex_dna      | 239 ms                                                                | 247 ms: 1.03x slower                                                    |
| regex_v8       | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                   |
| regex_effbot   | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 254 us: 1.10x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 192 ms: 1.09x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 358 us: 1.04x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.63 us: 1.03x faster                                                   |
| tomli_loads          | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                                  |
| pickle_list          | 5.01 us                                                               | 5.19 us: 1.04x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                   |
| json_loads           | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| pickle               | 12.8 us                                                               | 13.8 us: 1.07x slower                                                   |
| xml_etree_generate   | 104 ms                                                                | 112 ms: 1.08x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.48 ms: 1.15x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.3 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 61.2 ms: 1.02x faster                                                   |
| genshi_text    | 28.2 ms                                                               | 28.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240518-arminc-aarch64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 197 us: 3.32x faster                                                    |
| generators                 | 64.2 ms                                                               | 39.0 ms: 1.65x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 574 ms: 1.60x faster                                                    |
| async_tree_none            | 701 ms                                                                | 486 ms: 1.44x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.22 sec: 1.43x faster                                                  |
| comprehensions             | 29.0 us                                                               | 20.7 us: 1.40x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| deltablue                  | 4.75 ms                                                               | 3.88 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 785 ms: 1.22x faster                                                    |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.40 ms: 1.17x faster                                                   |
| richards_super             | 70.2 ms                                                               | 60.1 ms: 1.17x faster                                                   |
| chaos                      | 78.8 ms                                                               | 67.6 ms: 1.17x faster                                                   |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 792 ms: 1.16x faster                                                    |
| pylint                     | 397 ms                                                                | 342 ms: 1.16x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 1.73 ms: 1.15x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 21.8 ms: 1.14x faster                                                   |
| sympy_str                  | 295 ms                                                                | 268 ms: 1.10x faster                                                    |
| unpickle_pure_python       | 278 us                                                                | 254 us: 1.10x faster                                                    |
| sympy_integrate            | 23.2 ms                                                               | 21.1 ms: 1.10x faster                                                   |
| richards                   | 58.1 ms                                                               | 53.3 ms: 1.09x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 192 ms: 1.09x faster                                                    |
| dulwich_log                | 63.2 ms                                                               | 58.3 ms: 1.08x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.00 us: 1.08x faster                                                   |
| hexiom                     | 7.57 ms                                                               | 7.03 ms: 1.08x faster                                                   |
| crypto_pyaes               | 86.5 ms                                                               | 81.5 ms: 1.06x faster                                                   |
| tornado_http               | 140 ms                                                                | 131 ms: 1.06x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.29 ms: 1.05x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.85 us: 1.05x faster                                                   |
| pickle_pure_python         | 374 us                                                                | 358 us: 1.04x faster                                                    |
| regex_compile              | 137 ms                                                                | 131 ms: 1.04x faster                                                    |
| sympy_expand               | 482 ms                                                                | 462 ms: 1.04x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.63 us: 1.03x faster                                                   |
| nqueens                    | 102 ms                                                                | 99.0 ms: 1.03x faster                                                   |
| dask                       | 385 ms                                                                | 373 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 132 ms                                                                | 128 ms: 1.03x faster                                                    |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                                  |
| pycparser                  | 1.25 sec                                                              | 1.22 sec: 1.02x faster                                                  |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                                    |
| genshi_xml                 | 62.2 ms                                                               | 61.2 ms: 1.02x faster                                                   |
| scimark_lu                 | 140 ms                                                                | 139 ms: 1.01x faster                                                    |
| mdp                        | 3.35 sec                                                              | 3.37 sec: 1.00x slower                                                  |
| logging_silent             | 133 ns                                                                | 133 ns: 1.01x slower                                                    |
| 2to3                       | 300 ms                                                                | 303 ms: 1.01x slower                                                    |
| float                      | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                                   |
| genshi_text                | 28.2 ms                                                               | 28.6 ms: 1.02x slower                                                   |
| fannkuch                   | 451 ms                                                                | 463 ms: 1.03x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 1.91 sec: 1.03x slower                                                  |
| json                       | 5.52 ms                                                               | 5.68 ms: 1.03x slower                                                   |
| regex_dna                  | 239 ms                                                                | 247 ms: 1.03x slower                                                    |
| deepcopy                   | 435 us                                                                | 450 us: 1.03x slower                                                    |
| thrift                     | 910 us                                                                | 942 us: 1.03x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 935 ms: 1.04x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.19 us: 1.04x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.53 ms: 1.04x slower                                                   |
| deepcopy_memo              | 49.0 us                                                               | 51.3 us: 1.05x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 68.3 ms: 1.05x slower                                                   |
| deepcopy_reduce            | 3.89 us                                                               | 4.07 us: 1.05x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                   |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.07x slower                                                   |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 112 ms: 1.08x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 9.03 ms: 1.09x slower                                                   |
| scimark_sor                | 145 ms                                                                | 159 ms: 1.09x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.90 us: 1.10x slower                                                   |
| scimark_fft                | 402 ms                                                                | 443 ms: 1.10x slower                                                    |
| pyflate                    | 516 ms                                                                | 578 ms: 1.12x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.76 ms: 1.13x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 8.48 ms: 1.15x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| coverage                   | 84.1 ms                                                               | 99.5 ms: 1.18x slower                                                   |
| python_startup             | 10.2 ms                                                               | 12.3 ms: 1.21x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.29 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.42 ms: 1.29x slower                                                   |
| async_generators           | 378 ms                                                                | 496 ms: 1.31x slower                                                    |
| telco                      | 7.80 ms                                                               | 166 ms: 21.22x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                                            |

Benchmark hidden because not significant (10): go, sqlglot_optimize, pickle_dict, bench_mp_pool, scimark_monte_carlo, django_template, nbody, asyncio_websockets, xml_etree_iterparse, mako
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.63% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x