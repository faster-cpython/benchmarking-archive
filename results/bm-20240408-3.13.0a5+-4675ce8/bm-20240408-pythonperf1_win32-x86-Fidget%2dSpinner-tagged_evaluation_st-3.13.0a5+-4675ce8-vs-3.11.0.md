# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-x86
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 230 ms: 1.23x faster                                                                      |
| chameleon      | 8.08 ms                                                         | 5.67 ms: 1.43x faster                                                                     |
| docutils       | 2.10 sec                                                        | 1.77 sec: 1.18x faster                                                                    |
| html5lib       | 54.3 ms                                                         | 42.4 ms: 1.28x faster                                                                     |
| tornado_http   | 118 ms                                                          | 91.6 ms: 1.29x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.28x faster                                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 216 ms: 1.58x faster                                                                      |
| async_tree_memoization     | 408 ms                                                          | 262 ms: 1.56x faster                                                                      |
| async_tree_memoization_tg  | 378 ms                                                          | 244 ms: 1.54x faster                                                                      |
| async_tree_none_tg         | 301 ms                                                          | 199 ms: 1.51x faster                                                                      |
| async_tree_io              | 754 ms                                                          | 510 ms: 1.48x faster                                                                      |
| async_tree_io_tg           | 746 ms                                                          | 514 ms: 1.45x faster                                                                      |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 439 ms: 1.31x faster                                                                      |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 457 ms: 1.29x faster                                                                      |
| Geometric mean             | (ref)                                                           | 1.46x faster                                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.1 ms: 1.68x faster                                                                     |
| float          | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                                     |
| pidigits       | 203 ms                                                          | 196 ms: 1.04x faster                                                                      |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.3 ms: 1.53x faster                                                                     |
| regex_dna      | 122 ms                                                          | 117 ms: 1.04x faster                                                                      |
| regex_effbot   | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                                     |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                                     |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 145 us: 1.60x faster                                                                      |
| pickle_pure_python   | 309 us                                                          | 206 us: 1.50x faster                                                                      |
| json_dumps           | 9.80 ms                                                         | 6.55 ms: 1.50x faster                                                                     |
| tomli_loads          | 2.31 sec                                                        | 1.59 sec: 1.46x faster                                                                    |
| xml_etree_process    | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                                     |
| xml_etree_generate   | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                                     |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.1 ms: 1.16x faster                                                                     |
| unpickle_list        | 3.28 us                                                         | 3.00 us: 1.09x faster                                                                     |
| xml_etree_parse      | 114 ms                                                          | 106 ms: 1.07x faster                                                                      |
| pickle_list          | 3.27 us                                                         | 3.21 us: 1.02x faster                                                                     |
| pickle               | 7.99 us                                                         | 7.88 us: 1.01x faster                                                                     |
| json_loads           | 20.0 us                                                         | 20.1 us: 1.00x slower                                                                     |
| unpickle             | 9.23 us                                                         | 9.87 us: 1.07x slower                                                                     |
| Geometric mean       | (ref)                                                           | 1.18x faster                                                                              |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                                     |
| python_startup_no_site | 18.8 ms                                                         | 19.8 ms: 1.05x slower                                                                     |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 6.76 ms: 1.52x faster                                                                     |
| genshi_xml     | 61.2 ms                                                         | 43.9 ms: 1.40x faster                                                                     |
| genshi_text    | 26.8 ms                                                         | 19.7 ms: 1.36x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.42x faster                                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 92.8 us: 5.16x faster                                                                     |
| generators                 | 52.2 ms                                                         | 22.5 ms: 2.32x faster                                                                     |
| logging_silent             | 119 ns                                                          | 57.5 ns: 2.07x faster                                                                     |
| pylint                     | 418 ms                                                          | 204 ms: 2.05x faster                                                                      |
| deltablue                  | 4.10 ms                                                         | 2.14 ms: 1.91x faster                                                                     |
| comprehensions             | 22.1 us                                                         | 11.8 us: 1.87x faster                                                                     |
| chaos                      | 84.4 ms                                                         | 46.8 ms: 1.80x faster                                                                     |
| hexiom                     | 7.51 ms                                                         | 4.22 ms: 1.78x faster                                                                     |
| spectral_norm              | 122 ms                                                          | 68.7 ms: 1.77x faster                                                                     |
| deepcopy_memo              | 40.0 us                                                         | 22.8 us: 1.76x faster                                                                     |
| richards_super             | 58.7 ms                                                         | 33.6 ms: 1.75x faster                                                                     |
| raytrace                   | 327 ms                                                          | 188 ms: 1.74x faster                                                                      |
| scimark_sor                | 135 ms                                                          | 79.0 ms: 1.71x faster                                                                     |
| scimark_lu                 | 102 ms                                                          | 59.7 ms: 1.71x faster                                                                     |
| sqlglot_parse              | 1.49 ms                                                         | 878 us: 1.70x faster                                                                      |
| nbody                      | 126 ms                                                          | 75.1 ms: 1.68x faster                                                                     |
| coroutines                 | 23.7 ms                                                         | 14.2 ms: 1.67x faster                                                                     |
| richards                   | 48.8 ms                                                         | 29.7 ms: 1.65x faster                                                                     |
| sqlglot_transpile          | 1.78 ms                                                         | 1.10 ms: 1.62x faster                                                                     |
| unpickle_pure_python       | 231 us                                                          | 145 us: 1.60x faster                                                                      |
| async_tree_none            | 343 ms                                                          | 216 ms: 1.58x faster                                                                      |
| nqueens                    | 111 ms                                                          | 70.9 ms: 1.57x faster                                                                     |
| scimark_monte_carlo        | 70.8 ms                                                         | 45.5 ms: 1.56x faster                                                                     |
| async_tree_memoization     | 408 ms                                                          | 262 ms: 1.56x faster                                                                      |
| pyflate                    | 471 ms                                                          | 304 ms: 1.55x faster                                                                      |
| async_tree_memoization_tg  | 378 ms                                                          | 244 ms: 1.54x faster                                                                      |
| regex_compile              | 148 ms                                                          | 96.3 ms: 1.53x faster                                                                     |
| go                         | 147 ms                                                          | 96.6 ms: 1.52x faster                                                                     |
| mako                       | 10.3 ms                                                         | 6.76 ms: 1.52x faster                                                                     |
| async_tree_none_tg         | 301 ms                                                          | 199 ms: 1.51x faster                                                                      |
| pickle_pure_python         | 309 us                                                          | 206 us: 1.50x faster                                                                      |
| json_dumps                 | 9.80 ms                                                         | 6.55 ms: 1.50x faster                                                                     |
| pprint_pformat             | 1.70 sec                                                        | 1.14 sec: 1.49x faster                                                                    |
| sympy_sum                  | 149 ms                                                          | 101 ms: 1.48x faster                                                                      |
| async_tree_io              | 754 ms                                                          | 510 ms: 1.48x faster                                                                      |
| crypto_pyaes               | 79.4 ms                                                         | 53.9 ms: 1.47x faster                                                                     |
| pprint_safe_repr           | 819 ms                                                          | 558 ms: 1.47x faster                                                                      |
| tomli_loads                | 2.31 sec                                                        | 1.59 sec: 1.46x faster                                                                    |
| fannkuch                   | 399 ms                                                          | 275 ms: 1.45x faster                                                                      |
| async_tree_io_tg           | 746 ms                                                          | 514 ms: 1.45x faster                                                                      |
| float                      | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                                     |
| logging_simple             | 10.8 us                                                         | 7.54 us: 1.43x faster                                                                     |
| scimark_fft                | 291 ms                                                          | 204 ms: 1.43x faster                                                                      |
| chameleon                  | 8.08 ms                                                         | 5.67 ms: 1.43x faster                                                                     |
| sympy_str                  | 283 ms                                                          | 200 ms: 1.42x faster                                                                      |
| logging_format             | 11.5 us                                                         | 8.12 us: 1.41x faster                                                                     |
| sympy_integrate            | 19.9 ms                                                         | 14.2 ms: 1.41x faster                                                                     |
| deepcopy                   | 381 us                                                          | 272 us: 1.40x faster                                                                      |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.03 ms: 1.40x faster                                                                     |
| genshi_xml                 | 61.2 ms                                                         | 43.9 ms: 1.40x faster                                                                     |
| deepcopy_reduce            | 3.32 us                                                         | 2.43 us: 1.36x faster                                                                     |
| pycparser                  | 1.04 sec                                                        | 767 ms: 1.36x faster                                                                      |
| genshi_text                | 26.8 ms                                                         | 19.7 ms: 1.36x faster                                                                     |
| sympy_expand               | 462 ms                                                          | 349 ms: 1.33x faster                                                                      |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 439 ms: 1.31x faster                                                                      |
| sqlglot_optimize           | 51.8 ms                                                         | 39.6 ms: 1.31x faster                                                                     |
| tornado_http               | 118 ms                                                          | 91.6 ms: 1.29x faster                                                                     |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 457 ms: 1.29x faster                                                                      |
| xml_etree_process          | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                                     |
| html5lib                   | 54.3 ms                                                         | 42.4 ms: 1.28x faster                                                                     |
| mdp                        | 2.07 sec                                                        | 1.62 sec: 1.28x faster                                                                    |
| 2to3                       | 282 ms                                                          | 230 ms: 1.23x faster                                                                      |
| asyncio_tcp                | 787 ms                                                          | 649 ms: 1.21x faster                                                                      |
| meteor_contest             | 90.9 ms                                                         | 75.5 ms: 1.20x faster                                                                     |
| xml_etree_generate         | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                                     |
| json                       | 4.78 ms                                                         | 4.04 ms: 1.18x faster                                                                     |
| docutils                   | 2.10 sec                                                        | 1.77 sec: 1.18x faster                                                                    |
| bench_thread_pool          | 1.14 ms                                                         | 979 us: 1.16x faster                                                                      |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.1 ms: 1.16x faster                                                                     |
| sqlite_synth               | 2.15 us                                                         | 1.90 us: 1.13x faster                                                                     |
| unpickle_list              | 3.28 us                                                         | 3.00 us: 1.09x faster                                                                     |
| xml_etree_parse            | 114 ms                                                          | 106 ms: 1.07x faster                                                                      |
| bench_mp_pool              | 70.9 ms                                                         | 68.0 ms: 1.04x faster                                                                     |
| regex_dna                  | 122 ms                                                          | 117 ms: 1.04x faster                                                                      |
| pidigits                   | 203 ms                                                          | 196 ms: 1.04x faster                                                                      |
| pickle_list                | 3.27 us                                                         | 3.21 us: 1.02x faster                                                                     |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                                    |
| pickle                     | 7.99 us                                                         | 7.88 us: 1.01x faster                                                                     |
| json_loads                 | 20.0 us                                                         | 20.1 us: 1.00x slower                                                                     |
| python_startup             | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                                     |
| regex_effbot               | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                                     |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                                     |
| python_startup_no_site     | 18.8 ms                                                         | 19.8 ms: 1.05x slower                                                                     |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                                     |
| unpickle                   | 9.23 us                                                         | 9.87 us: 1.07x slower                                                                     |
| async_generators           | 260 ms                                                          | 278 ms: 1.07x slower                                                                      |
| pathlib                    | 79.9 ms                                                         | 85.6 ms: 1.07x slower                                                                     |
| telco                      | 5.29 ms                                                         | 6.00 ms: 1.13x slower                                                                     |
| create_gc_cycles           | 618 us                                                          | 733 us: 1.19x slower                                                                      |
| sqlglot_normalize          | 113 ms                                                          | 206 ms: 1.82x slower                                                                      |
| coverage                   | 58.0 ms                                                         | 507 ms: 8.74x slower                                                                      |
| thrift                     | 801 us                                                          | 9.74 ms: 12.17x slower                                                                    |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                                              |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.34x
- 95% likely to have a speedup of 1.32x
- 99% likely to have a speedup of 1.29x

# Memory
- memory change: unknown