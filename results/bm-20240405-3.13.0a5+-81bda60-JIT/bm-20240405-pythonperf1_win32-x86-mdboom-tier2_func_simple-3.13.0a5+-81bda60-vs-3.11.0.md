# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-x86
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 255 ms: 1.11x faster                                                         |
| chameleon      | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                        |
| docutils       | 2.10 sec                                                        | 1.94 sec: 1.08x faster                                                       |
| html5lib       | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                        |
| tornado_http   | 118 ms                                                          | 96.6 ms: 1.23x faster                                                        |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.42x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 216 ms: 1.39x faster                                                         |
| async_tree_io              | 754 ms                                                          | 542 ms: 1.39x faster                                                         |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                           | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                        |
| nbody          | 126 ms                                                          | 96.4 ms: 1.31x faster                                                        |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 112 ms: 1.31x faster                                                         |
| regex_dna      | 122 ms                                                          | 124 ms: 1.02x slower                                                         |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                        |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                        |
| pickle_pure_python   | 309 us                                                          | 221 us: 1.40x faster                                                         |
| unpickle_pure_python | 231 us                                                          | 173 us: 1.34x faster                                                         |
| tomli_loads          | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                       |
| xml_etree_process    | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                        |
| unpickle_list        | 3.28 us                                                         | 2.75 us: 1.19x faster                                                        |
| xml_etree_generate   | 71.6 ms                                                         | 60.4 ms: 1.19x faster                                                        |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                        |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.07x faster                                                         |
| pickle_list          | 3.27 us                                                         | 3.17 us: 1.03x faster                                                        |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                                        |
| unpickle             | 9.23 us                                                         | 9.95 us: 1.08x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                 |

Benchmark hidden because not significant (2): pickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.1 ms: 1.10x slower                                                        |
| python_startup_no_site | 18.8 ms                                                         | 21.7 ms: 1.15x slower                                                        |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 7.14 ms: 1.44x faster                                                        |
| genshi_xml     | 61.2 ms                                                         | 47.8 ms: 1.28x faster                                                        |
| genshi_text    | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                        |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 98.7 us: 4.85x faster                                                        |
| generators                 | 52.2 ms                                                         | 22.4 ms: 2.33x faster                                                        |
| logging_silent             | 119 ns                                                          | 60.0 ns: 1.99x faster                                                        |
| pylint                     | 418 ms                                                          | 222 ms: 1.88x faster                                                         |
| spectral_norm              | 122 ms                                                          | 72.3 ms: 1.68x faster                                                        |
| coroutines                 | 23.7 ms                                                         | 14.9 ms: 1.60x faster                                                        |
| deepcopy_memo              | 40.0 us                                                         | 25.3 us: 1.58x faster                                                        |
| deltablue                  | 4.10 ms                                                         | 2.74 ms: 1.50x faster                                                        |
| sqlglot_parse              | 1.49 ms                                                         | 1.00 ms: 1.48x faster                                                        |
| raytrace                   | 327 ms                                                          | 222 ms: 1.48x faster                                                         |
| richards_super             | 58.7 ms                                                         | 40.0 ms: 1.47x faster                                                        |
| json_dumps                 | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                        |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.44x faster                                                        |
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                         |
| mako                       | 10.3 ms                                                         | 7.14 ms: 1.44x faster                                                        |
| chaos                      | 84.4 ms                                                         | 58.8 ms: 1.44x faster                                                        |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.42x faster                                                         |
| float                      | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                        |
| comprehensions             | 22.1 us                                                         | 15.7 us: 1.41x faster                                                        |
| pickle_pure_python         | 309 us                                                          | 221 us: 1.40x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 216 ms: 1.39x faster                                                         |
| richards                   | 48.8 ms                                                         | 35.1 ms: 1.39x faster                                                        |
| async_tree_io              | 754 ms                                                          | 542 ms: 1.39x faster                                                         |
| scimark_sor                | 135 ms                                                          | 97.3 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 109 ms: 1.37x faster                                                         |
| logging_simple             | 10.8 us                                                         | 8.06 us: 1.34x faster                                                        |
| unpickle_pure_python       | 231 us                                                          | 173 us: 1.34x faster                                                         |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.18 ms: 1.33x faster                                                        |
| tomli_loads                | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                       |
| regex_compile              | 148 ms                                                          | 112 ms: 1.31x faster                                                         |
| logging_format             | 11.5 us                                                         | 8.73 us: 1.31x faster                                                        |
| chameleon                  | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                        |
| nbody                      | 126 ms                                                          | 96.4 ms: 1.31x faster                                                        |
| sympy_str                  | 283 ms                                                          | 217 ms: 1.31x faster                                                         |
| deepcopy                   | 381 us                                                          | 294 us: 1.29x faster                                                         |
| genshi_xml                 | 61.2 ms                                                         | 47.8 ms: 1.28x faster                                                        |
| pyflate                    | 471 ms                                                          | 368 ms: 1.28x faster                                                         |
| xml_etree_process          | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                        |
| deepcopy_reduce            | 3.32 us                                                         | 2.62 us: 1.27x faster                                                        |
| sympy_expand               | 462 ms                                                          | 368 ms: 1.25x faster                                                         |
| asyncio_tcp                | 787 ms                                                          | 628 ms: 1.25x faster                                                         |
| crypto_pyaes               | 79.4 ms                                                         | 63.4 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                         |
| pycparser                  | 1.04 sec                                                        | 841 ms: 1.24x faster                                                         |
| genshi_text                | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                        |
| sympy_integrate            | 19.9 ms                                                         | 16.2 ms: 1.23x faster                                                        |
| scimark_fft                | 291 ms                                                          | 237 ms: 1.23x faster                                                         |
| tornado_http               | 118 ms                                                          | 96.6 ms: 1.23x faster                                                        |
| hexiom                     | 7.51 ms                                                         | 6.14 ms: 1.22x faster                                                        |
| fannkuch                   | 399 ms                                                          | 327 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.22x faster                                                         |
| go                         | 147 ms                                                          | 121 ms: 1.21x faster                                                         |
| nqueens                    | 111 ms                                                          | 93.0 ms: 1.20x faster                                                        |
| unpickle_list              | 3.28 us                                                         | 2.75 us: 1.19x faster                                                        |
| scimark_lu                 | 102 ms                                                          | 86.1 ms: 1.19x faster                                                        |
| xml_etree_generate         | 71.6 ms                                                         | 60.4 ms: 1.19x faster                                                        |
| json                       | 4.78 ms                                                         | 4.04 ms: 1.18x faster                                                        |
| html5lib                   | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                        |
| mdp                        | 2.07 sec                                                        | 1.76 sec: 1.17x faster                                                       |
| scimark_monte_carlo        | 70.8 ms                                                         | 61.2 ms: 1.16x faster                                                        |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                        |
| bench_thread_pool          | 1.14 ms                                                         | 985 us: 1.15x faster                                                         |
| sqlite_synth               | 2.15 us                                                         | 1.90 us: 1.13x faster                                                        |
| sqlglot_optimize           | 51.8 ms                                                         | 46.4 ms: 1.12x faster                                                        |
| 2to3                       | 282 ms                                                          | 255 ms: 1.11x faster                                                         |
| pprint_pformat             | 1.70 sec                                                        | 1.54 sec: 1.10x faster                                                       |
| meteor_contest             | 90.9 ms                                                         | 83.4 ms: 1.09x faster                                                        |
| pprint_safe_repr           | 819 ms                                                          | 757 ms: 1.08x faster                                                         |
| docutils                   | 2.10 sec                                                        | 1.94 sec: 1.08x faster                                                       |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.07x faster                                                         |
| pickle_list                | 3.27 us                                                         | 3.17 us: 1.03x faster                                                        |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                         |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                       |
| regex_dna                  | 122 ms                                                          | 124 ms: 1.02x slower                                                         |
| bench_mp_pool              | 70.9 ms                                                         | 72.5 ms: 1.02x slower                                                        |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                        |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.05x slower                                                        |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                        |
| unpickle                   | 9.23 us                                                         | 9.95 us: 1.08x slower                                                        |
| pathlib                    | 79.9 ms                                                         | 86.7 ms: 1.08x slower                                                        |
| async_generators           | 260 ms                                                          | 283 ms: 1.09x slower                                                         |
| python_startup             | 22.0 ms                                                         | 24.1 ms: 1.10x slower                                                        |
| python_startup_no_site     | 18.8 ms                                                         | 21.7 ms: 1.15x slower                                                        |
| create_gc_cycles           | 618 us                                                          | 738 us: 1.19x slower                                                         |
| telco                      | 5.29 ms                                                         | 6.42 ms: 1.21x slower                                                        |
| sqlglot_normalize          | 113 ms                                                          | 235 ms: 2.08x slower                                                         |
| coverage                   | 58.0 ms                                                         | 505 ms: 8.71x slower                                                         |
| thrift                     | 801 us                                                          | 10.7 ms: 13.37x slower                                                       |
| Geometric mean             | (ref)                                                           | 1.17x faster                                                                 |

Benchmark hidden because not significant (2): pickle, json_loads
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown