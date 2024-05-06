# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-x86
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 232 ms: 1.21x faster                                                                    |
| chameleon      | 8.08 ms                                                         | 5.61 ms: 1.44x faster                                                                   |
| docutils       | 2.10 sec                                                        | 1.80 sec: 1.17x faster                                                                  |
| html5lib       | 54.3 ms                                                         | 42.8 ms: 1.27x faster                                                                   |
| tornado_http   | 118 ms                                                          | 94.0 ms: 1.26x faster                                                                   |
| Geometric mean | (ref)                                                           | 1.27x faster                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 226 ms: 1.52x faster                                                                    |
| async_tree_memoization     | 408 ms                                                          | 270 ms: 1.51x faster                                                                    |
| async_tree_memoization_tg  | 378 ms                                                          | 253 ms: 1.49x faster                                                                    |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.46x faster                                                                    |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.43x faster                                                                    |
| async_tree_io_tg           | 746 ms                                                          | 527 ms: 1.42x faster                                                                    |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                                    |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                                    |
| Geometric mean             | (ref)                                                           | 1.42x faster                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 76.4 ms: 1.65x faster                                                                   |
| float          | 76.1 ms                                                         | 53.4 ms: 1.42x faster                                                                   |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                                    |
| Geometric mean | (ref)                                                           | 1.34x faster                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 97.4 ms: 1.51x faster                                                                   |
| regex_dna      | 122 ms                                                          | 121 ms: 1.01x faster                                                                    |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                                   |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                                   |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 140 us: 1.65x faster                                                                    |
| pickle_pure_python   | 309 us                                                          | 209 us: 1.48x faster                                                                    |
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                                  |
| json_dumps           | 9.80 ms                                                         | 6.92 ms: 1.42x faster                                                                   |
| xml_etree_process    | 55.0 ms                                                         | 42.3 ms: 1.30x faster                                                                   |
| xml_etree_generate   | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                                   |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.0 ms: 1.16x faster                                                                   |
| unpickle_list        | 3.28 us                                                         | 2.86 us: 1.15x faster                                                                   |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.07x faster                                                                    |
| pickle_list          | 3.27 us                                                         | 3.29 us: 1.01x slower                                                                   |
| pickle_dict          | 20.1 us                                                         | 20.4 us: 1.02x slower                                                                   |
| json_loads           | 20.0 us                                                         | 20.6 us: 1.03x slower                                                                   |
| unpickle             | 9.23 us                                                         | 9.81 us: 1.06x slower                                                                   |
| Geometric mean       | (ref)                                                           | 1.18x faster                                                                            |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                                   |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.87 ms: 1.50x faster                                                                   |
| genshi_xml      | 61.2 ms                                                         | 42.7 ms: 1.43x faster                                                                   |
| genshi_text     | 26.8 ms                                                         | 18.8 ms: 1.43x faster                                                                   |
| django_template | 37.4 ms                                                         | 29.5 ms: 1.27x faster                                                                   |
| Geometric mean  | (ref)                                                           | 1.40x faster                                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 90.7 us: 5.27x faster                                                                   |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.26x faster                                                                   |
| logging_silent             | 119 ns                                                          | 59.8 ns: 1.99x faster                                                                   |
| pylint                     | 418 ms                                                          | 219 ms: 1.91x faster                                                                    |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.89x faster                                                                   |
| deltablue                  | 4.10 ms                                                         | 2.20 ms: 1.86x faster                                                                   |
| deepcopy_memo              | 40.0 us                                                         | 22.9 us: 1.75x faster                                                                   |
| hexiom                     | 7.51 ms                                                         | 4.32 ms: 1.74x faster                                                                   |
| raytrace                   | 327 ms                                                          | 189 ms: 1.74x faster                                                                    |
| chaos                      | 84.4 ms                                                         | 49.1 ms: 1.72x faster                                                                   |
| richards_super             | 58.7 ms                                                         | 34.2 ms: 1.71x faster                                                                   |
| spectral_norm              | 122 ms                                                          | 71.0 ms: 1.71x faster                                                                   |
| sqlglot_parse              | 1.49 ms                                                         | 878 us: 1.70x faster                                                                    |
| scimark_sor                | 135 ms                                                          | 80.9 ms: 1.67x faster                                                                   |
| scimark_lu                 | 102 ms                                                          | 61.4 ms: 1.67x faster                                                                   |
| nbody                      | 126 ms                                                          | 76.4 ms: 1.65x faster                                                                   |
| unpickle_pure_python       | 231 us                                                          | 140 us: 1.65x faster                                                                    |
| sqlglot_transpile          | 1.78 ms                                                         | 1.10 ms: 1.62x faster                                                                   |
| coroutines                 | 23.7 ms                                                         | 14.7 ms: 1.61x faster                                                                   |
| richards                   | 48.8 ms                                                         | 30.3 ms: 1.61x faster                                                                   |
| nqueens                    | 111 ms                                                          | 70.6 ms: 1.58x faster                                                                   |
| async_tree_none            | 343 ms                                                          | 226 ms: 1.52x faster                                                                    |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.7 ms: 1.52x faster                                                                   |
| regex_compile              | 148 ms                                                          | 97.4 ms: 1.51x faster                                                                   |
| async_tree_memoization     | 408 ms                                                          | 270 ms: 1.51x faster                                                                    |
| go                         | 147 ms                                                          | 98.3 ms: 1.50x faster                                                                   |
| mako                       | 10.3 ms                                                         | 6.87 ms: 1.50x faster                                                                   |
| async_tree_memoization_tg  | 378 ms                                                          | 253 ms: 1.49x faster                                                                    |
| pyflate                    | 471 ms                                                          | 316 ms: 1.49x faster                                                                    |
| pprint_pformat             | 1.70 sec                                                        | 1.15 sec: 1.48x faster                                                                  |
| pickle_pure_python         | 309 us                                                          | 209 us: 1.48x faster                                                                    |
| pprint_safe_repr           | 819 ms                                                          | 558 ms: 1.47x faster                                                                    |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.46x faster                                                                    |
| logging_simple             | 10.8 us                                                         | 7.47 us: 1.45x faster                                                                   |
| deepcopy                   | 381 us                                                          | 264 us: 1.44x faster                                                                    |
| chameleon                  | 8.08 ms                                                         | 5.61 ms: 1.44x faster                                                                   |
| genshi_xml                 | 61.2 ms                                                         | 42.7 ms: 1.43x faster                                                                   |
| fannkuch                   | 399 ms                                                          | 279 ms: 1.43x faster                                                                    |
| logging_format             | 11.5 us                                                         | 8.01 us: 1.43x faster                                                                   |
| genshi_text                | 26.8 ms                                                         | 18.8 ms: 1.43x faster                                                                   |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.43x faster                                                                    |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.43x faster                                                                    |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                                  |
| float                      | 76.1 ms                                                         | 53.4 ms: 1.42x faster                                                                   |
| json_dumps                 | 9.80 ms                                                         | 6.92 ms: 1.42x faster                                                                   |
| async_tree_io_tg           | 746 ms                                                          | 527 ms: 1.42x faster                                                                    |
| crypto_pyaes               | 79.4 ms                                                         | 56.5 ms: 1.40x faster                                                                   |
| deepcopy_reduce            | 3.32 us                                                         | 2.36 us: 1.40x faster                                                                   |
| sympy_str                  | 283 ms                                                          | 205 ms: 1.38x faster                                                                    |
| scimark_fft                | 291 ms                                                          | 212 ms: 1.37x faster                                                                    |
| sympy_integrate            | 19.9 ms                                                         | 14.5 ms: 1.37x faster                                                                   |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.11 ms: 1.36x faster                                                                   |
| pycparser                  | 1.04 sec                                                        | 772 ms: 1.35x faster                                                                    |
| sqlglot_optimize           | 51.8 ms                                                         | 39.5 ms: 1.31x faster                                                                   |
| xml_etree_process          | 55.0 ms                                                         | 42.3 ms: 1.30x faster                                                                   |
| sympy_expand               | 462 ms                                                          | 359 ms: 1.29x faster                                                                    |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                                    |
| html5lib                   | 54.3 ms                                                         | 42.8 ms: 1.27x faster                                                                   |
| django_template            | 37.4 ms                                                         | 29.5 ms: 1.27x faster                                                                   |
| mdp                        | 2.07 sec                                                        | 1.64 sec: 1.26x faster                                                                  |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                                    |
| tornado_http               | 118 ms                                                          | 94.0 ms: 1.26x faster                                                                   |
| 2to3                       | 282 ms                                                          | 232 ms: 1.21x faster                                                                    |
| meteor_contest             | 90.9 ms                                                         | 75.2 ms: 1.21x faster                                                                   |
| xml_etree_generate         | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                                   |
| asyncio_tcp                | 787 ms                                                          | 659 ms: 1.19x faster                                                                    |
| docutils                   | 2.10 sec                                                        | 1.80 sec: 1.17x faster                                                                  |
| bench_thread_pool          | 1.14 ms                                                         | 977 us: 1.16x faster                                                                    |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.0 ms: 1.16x faster                                                                   |
| json                       | 4.78 ms                                                         | 4.12 ms: 1.16x faster                                                                   |
| unpickle_list              | 3.28 us                                                         | 2.86 us: 1.15x faster                                                                   |
| sqlite_synth               | 2.15 us                                                         | 1.97 us: 1.09x faster                                                                   |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.07x faster                                                                    |
| bench_mp_pool              | 70.9 ms                                                         | 68.1 ms: 1.04x faster                                                                   |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                                    |
| python_startup_no_site     | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                                   |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                                  |
| regex_dna                  | 122 ms                                                          | 121 ms: 1.01x faster                                                                    |
| pickle_list                | 3.27 us                                                         | 3.29 us: 1.01x slower                                                                   |
| pickle_dict                | 20.1 us                                                         | 20.4 us: 1.02x slower                                                                   |
| json_loads                 | 20.0 us                                                         | 20.6 us: 1.03x slower                                                                   |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                                   |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                                   |
| pathlib                    | 79.9 ms                                                         | 84.8 ms: 1.06x slower                                                                   |
| unpickle                   | 9.23 us                                                         | 9.81 us: 1.06x slower                                                                   |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                                   |
| async_generators           | 260 ms                                                          | 280 ms: 1.08x slower                                                                    |
| telco                      | 5.29 ms                                                         | 5.90 ms: 1.11x slower                                                                   |
| create_gc_cycles           | 618 us                                                          | 732 us: 1.19x slower                                                                    |
| sqlglot_normalize          | 113 ms                                                          | 203 ms: 1.79x slower                                                                    |
| coverage                   | 58.0 ms                                                         | 506 ms: 8.72x slower                                                                    |
| thrift                     | 801 us                                                          | 9.88 ms: 12.34x slower                                                                  |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                            |

Benchmark hidden because not significant (2): pickle, python_startup
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.31x
- 95% likely to have a speedup of 1.30x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown