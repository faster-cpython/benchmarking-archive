# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-x86
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 235 ms: 1.20x faster                                                             |
| chameleon      | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                            |
| docutils       | 2.10 sec                                                        | 1.80 sec: 1.16x faster                                                           |
| html5lib       | 54.3 ms                                                         | 43.1 ms: 1.26x faster                                                            |
| tornado_http   | 118 ms                                                          | 102 ms: 1.16x faster                                                             |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                             |
| async_tree_memoization     | 408 ms                                                          | 275 ms: 1.49x faster                                                             |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                             |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                             |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.42x faster                                                             |
| async_tree_io_tg           | 746 ms                                                          | 539 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 480 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                           | 1.40x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 80.3 ms: 1.57x faster                                                            |
| float          | 76.1 ms                                                         | 53.0 ms: 1.44x faster                                                            |
| pidigits       | 203 ms                                                          | 200 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.3 ms: 1.53x faster                                                            |
| regex_dna      | 122 ms                                                          | 121 ms: 1.01x faster                                                             |
| regex_effbot   | 1.82 ms                                                         | 1.87 ms: 1.03x slower                                                            |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 140 us: 1.66x faster                                                             |
| pickle_pure_python   | 309 us                                                          | 209 us: 1.48x faster                                                             |
| tomli_loads          | 2.31 sec                                                        | 1.58 sec: 1.46x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 41.8 ms: 1.32x faster                                                            |
| xml_etree_generate   | 71.6 ms                                                         | 58.8 ms: 1.22x faster                                                            |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.2 ms: 1.16x faster                                                            |
| unpickle_list        | 3.28 us                                                         | 2.90 us: 1.13x faster                                                            |
| xml_etree_parse      | 114 ms                                                          | 106 ms: 1.08x faster                                                             |
| pickle               | 7.99 us                                                         | 7.90 us: 1.01x faster                                                            |
| json_loads           | 20.0 us                                                         | 19.9 us: 1.01x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 20.3 us: 1.01x slower                                                            |
| unpickle             | 9.23 us                                                         | 9.97 us: 1.08x slower                                                            |
| Geometric mean       | (ref)                                                           | 1.19x faster                                                                     |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                            |
| python_startup         | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                            |
| Geometric mean         | (ref)                                                           | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                                            |
| genshi_xml      | 61.2 ms                                                         | 43.1 ms: 1.42x faster                                                            |
| genshi_text     | 26.8 ms                                                         | 18.9 ms: 1.42x faster                                                            |
| django_template | 37.4 ms                                                         | 29.8 ms: 1.25x faster                                                            |
| Geometric mean  | (ref)                                                           | 1.39x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 131 us: 3.66x faster                                                             |
| generators                 | 52.2 ms                                                         | 22.6 ms: 2.31x faster                                                            |
| logging_silent             | 119 ns                                                          | 56.1 ns: 2.12x faster                                                            |
| pylint                     | 418 ms                                                          | 218 ms: 1.92x faster                                                             |
| deltablue                  | 4.10 ms                                                         | 2.16 ms: 1.90x faster                                                            |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.88x faster                                                            |
| raytrace                   | 327 ms                                                          | 182 ms: 1.80x faster                                                             |
| spectral_norm              | 122 ms                                                          | 67.9 ms: 1.79x faster                                                            |
| richards_super             | 58.7 ms                                                         | 33.0 ms: 1.78x faster                                                            |
| chaos                      | 84.4 ms                                                         | 47.5 ms: 1.78x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 4.24 ms: 1.77x faster                                                            |
| deepcopy_memo              | 40.0 us                                                         | 23.3 us: 1.72x faster                                                            |
| scimark_sor                | 135 ms                                                          | 79.1 ms: 1.71x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 60.7 ms: 1.68x faster                                                            |
| richards                   | 48.8 ms                                                         | 29.5 ms: 1.66x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 140 us: 1.66x faster                                                             |
| sqlglot_parse              | 1.49 ms                                                         | 907 us: 1.64x faster                                                             |
| nqueens                    | 111 ms                                                          | 68.2 ms: 1.63x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.13 ms: 1.57x faster                                                            |
| nbody                      | 126 ms                                                          | 80.3 ms: 1.57x faster                                                            |
| regex_compile              | 148 ms                                                          | 96.3 ms: 1.53x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.12 us: 1.52x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.8 ms: 1.51x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.7 ms: 1.51x faster                                                            |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                             |
| pyflate                    | 471 ms                                                          | 313 ms: 1.51x faster                                                             |
| async_tree_memoization     | 408 ms                                                          | 275 ms: 1.49x faster                                                             |
| pickle_pure_python         | 309 us                                                          | 209 us: 1.48x faster                                                             |
| mako                       | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                             |
| go                         | 147 ms                                                          | 99.6 ms: 1.48x faster                                                            |
| logging_format             | 11.5 us                                                         | 7.80 us: 1.47x faster                                                            |
| fannkuch                   | 399 ms                                                          | 273 ms: 1.47x faster                                                             |
| tomli_loads                | 2.31 sec                                                        | 1.58 sec: 1.46x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.17 sec: 1.45x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 54.9 ms: 1.45x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                             |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.44x faster                                                             |
| float                      | 76.1 ms                                                         | 53.0 ms: 1.44x faster                                                            |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.42x faster                                                             |
| sympy_str                  | 283 ms                                                          | 199 ms: 1.42x faster                                                             |
| pprint_safe_repr           | 819 ms                                                          | 576 ms: 1.42x faster                                                             |
| chameleon                  | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 43.1 ms: 1.42x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 18.9 ms: 1.42x faster                                                            |
| deepcopy                   | 381 us                                                          | 272 us: 1.40x faster                                                             |
| sympy_integrate            | 19.9 ms                                                         | 14.2 ms: 1.40x faster                                                            |
| scimark_fft                | 291 ms                                                          | 208 ms: 1.40x faster                                                             |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.06 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 539 ms: 1.38x faster                                                             |
| pycparser                  | 1.04 sec                                                        | 766 ms: 1.36x faster                                                             |
| sqlglot_optimize           | 51.8 ms                                                         | 38.7 ms: 1.34x faster                                                            |
| sympy_expand               | 462 ms                                                          | 347 ms: 1.33x faster                                                             |
| xml_etree_process          | 55.0 ms                                                         | 41.8 ms: 1.32x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.58 us: 1.29x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.61 sec: 1.28x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 43.1 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                             |
| django_template            | 37.4 ms                                                         | 29.8 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 480 ms: 1.23x faster                                                             |
| xml_etree_generate         | 71.6 ms                                                         | 58.8 ms: 1.22x faster                                                            |
| 2to3                       | 282 ms                                                          | 235 ms: 1.20x faster                                                             |
| meteor_contest             | 90.9 ms                                                         | 76.9 ms: 1.18x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.80 sec: 1.16x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.2 ms: 1.16x faster                                                            |
| tornado_http               | 118 ms                                                          | 102 ms: 1.16x faster                                                             |
| json                       | 4.78 ms                                                         | 4.17 ms: 1.15x faster                                                            |
| bench_thread_pool          | 1.14 ms                                                         | 992 us: 1.15x faster                                                             |
| unpickle_list              | 3.28 us                                                         | 2.90 us: 1.13x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                            |
| xml_etree_parse            | 114 ms                                                          | 106 ms: 1.08x faster                                                             |
| python_startup_no_site     | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 69.8 ms: 1.02x faster                                                            |
| pidigits                   | 203 ms                                                          | 200 ms: 1.01x faster                                                             |
| pickle                     | 7.99 us                                                         | 7.90 us: 1.01x faster                                                            |
| regex_dna                  | 122 ms                                                          | 121 ms: 1.01x faster                                                             |
| json_loads                 | 20.0 us                                                         | 19.9 us: 1.01x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.2 sec: 1.01x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.3 us: 1.01x slower                                                            |
| regex_effbot               | 1.82 ms                                                         | 1.87 ms: 1.03x slower                                                            |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                            |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                            |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.06x slower                                                            |
| unpickle                   | 9.23 us                                                         | 9.97 us: 1.08x slower                                                            |
| telco                      | 5.29 ms                                                         | 5.87 ms: 1.11x slower                                                            |
| async_generators           | 260 ms                                                          | 289 ms: 1.11x slower                                                             |
| asyncio_tcp                | 787 ms                                                          | 878 ms: 1.12x slower                                                             |
| pathlib                    | 79.9 ms                                                         | 90.2 ms: 1.13x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 740 us: 1.20x slower                                                             |
| sqlglot_normalize          | 113 ms                                                          | 200 ms: 1.77x slower                                                             |
| coverage                   | 58.0 ms                                                         | 498 ms: 8.59x slower                                                             |
| thrift                     | 801 us                                                          | 9.90 ms: 12.37x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                                     |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.32x
- 95% likely to have a speedup of 1.30x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown