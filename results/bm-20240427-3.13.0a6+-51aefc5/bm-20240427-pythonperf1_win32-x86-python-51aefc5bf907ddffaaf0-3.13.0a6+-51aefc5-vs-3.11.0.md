# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 231 ms: 1.22x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.56 ms: 1.45x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| html5lib       | 54.3 ms                                                         | 43.3 ms: 1.25x faster                                                           |
| tornado_http   | 118 ms                                                          | 104 ms: 1.14x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 221 ms: 1.55x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 267 ms: 1.53x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 251 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.48x faster                                                            |
| async_tree_io              | 754 ms                                                          | 517 ms: 1.46x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 526 ms: 1.42x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 449 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.43x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 80.9 ms: 1.56x faster                                                           |
| float          | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                           |
| pidigits       | 203 ms                                                          | 200 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 95.0 ms: 1.55x faster                                                           |
| regex_dna      | 122 ms                                                          | 121 ms: 1.01x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.4 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 138 us: 1.67x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 202 us: 1.53x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.75 ms: 1.45x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 42.0 ms: 1.31x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 59.8 ms: 1.20x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.5 ms: 1.15x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.92 us: 1.12x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| pickle               | 7.99 us                                                         | 7.92 us: 1.01x faster                                                           |
| json_loads           | 20.0 us                                                         | 20.2 us: 1.01x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.94 us: 1.08x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.59 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.18x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                         | 22.4 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.87 ms: 1.50x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 18.2 ms: 1.47x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 42.8 ms: 1.43x faster                                                           |
| django_template | 37.4 ms                                                         | 28.1 ms: 1.33x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.43x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 131 us: 3.65x faster                                                            |
| generators                 | 52.2 ms                                                         | 22.1 ms: 2.36x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.1 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 218 ms: 1.92x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.15 ms: 1.91x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.89x faster                                                           |
| chaos                      | 84.4 ms                                                         | 44.8 ms: 1.88x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.18 ms: 1.80x faster                                                           |
| spectral_norm              | 122 ms                                                          | 67.9 ms: 1.79x faster                                                           |
| raytrace                   | 327 ms                                                          | 184 ms: 1.78x faster                                                            |
| deepcopy_memo              | 40.0 us                                                         | 22.6 us: 1.77x faster                                                           |
| richards_super             | 58.7 ms                                                         | 33.4 ms: 1.76x faster                                                           |
| scimark_sor                | 135 ms                                                          | 78.5 ms: 1.72x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 60.2 ms: 1.70x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 883 us: 1.69x faster                                                            |
| nqueens                    | 111 ms                                                          | 66.0 ms: 1.69x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 138 us: 1.67x faster                                                            |
| richards                   | 48.8 ms                                                         | 29.8 ms: 1.64x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.12 ms: 1.60x faster                                                           |
| nbody                      | 126 ms                                                          | 80.9 ms: 1.56x faster                                                           |
| regex_compile              | 148 ms                                                          | 95.0 ms: 1.55x faster                                                           |
| async_tree_none            | 343 ms                                                          | 221 ms: 1.55x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.1 ms: 1.54x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 202 us: 1.53x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 267 ms: 1.53x faster                                                            |
| go                         | 147 ms                                                          | 96.2 ms: 1.53x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.13 us: 1.52x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.7 ms: 1.51x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.12 sec: 1.51x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 251 ms: 1.51x faster                                                            |
| pyflate                    | 471 ms                                                          | 314 ms: 1.50x faster                                                            |
| mako                       | 10.3 ms                                                         | 6.87 ms: 1.50x faster                                                           |
| logging_format             | 11.5 us                                                         | 7.66 us: 1.50x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 549 ms: 1.49x faster                                                            |
| fannkuch                   | 399 ms                                                          | 270 ms: 1.48x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.48x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 18.2 ms: 1.47x faster                                                           |
| async_tree_io              | 754 ms                                                          | 517 ms: 1.46x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 102 ms: 1.46x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.56 ms: 1.45x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.75 ms: 1.45x faster                                                           |
| float                      | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 55.1 ms: 1.44x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 42.8 ms: 1.43x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 526 ms: 1.42x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.99 ms: 1.41x faster                                                           |
| deepcopy                   | 381 us                                                          | 269 us: 1.41x faster                                                            |
| sympy_str                  | 283 ms                                                          | 202 ms: 1.40x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.4 ms: 1.38x faster                                                           |
| scimark_fft                | 291 ms                                                          | 212 ms: 1.37x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 38.3 ms: 1.35x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 773 ms: 1.35x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.47 us: 1.34x faster                                                           |
| django_template            | 37.4 ms                                                         | 28.1 ms: 1.33x faster                                                           |
| sympy_expand               | 462 ms                                                          | 351 ms: 1.32x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 42.0 ms: 1.31x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 449 ms: 1.29x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.61 sec: 1.28x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 43.3 ms: 1.25x faster                                                           |
| 2to3                       | 282 ms                                                          | 231 ms: 1.22x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 74.4 ms: 1.22x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 59.8 ms: 1.20x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.5 ms: 1.15x faster                                                           |
| json                       | 4.78 ms                                                         | 4.14 ms: 1.15x faster                                                           |
| tornado_http               | 118 ms                                                          | 104 ms: 1.14x faster                                                            |
| bench_thread_pool          | 1.14 ms                                                         | 995 us: 1.14x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.92 us: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                           |
| pidigits                   | 203 ms                                                          | 200 ms: 1.01x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 70.0 ms: 1.01x faster                                                           |
| pickle                     | 7.99 us                                                         | 7.92 us: 1.01x faster                                                           |
| regex_dna                  | 122 ms                                                          | 121 ms: 1.01x faster                                                            |
| json_loads                 | 20.0 us                                                         | 20.2 us: 1.01x slower                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.2 sec: 1.01x slower                                                          |
| python_startup             | 22.0 ms                                                         | 22.4 ms: 1.02x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.06x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.94 us: 1.08x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.4 ms: 1.08x slower                                                           |
| async_generators           | 260 ms                                                          | 283 ms: 1.09x slower                                                            |
| pickle_list                | 3.27 us                                                         | 3.59 us: 1.10x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 88.7 ms: 1.11x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.98 ms: 1.13x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 743 us: 1.20x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 193 ms: 1.71x slower                                                            |
| coverage                   | 58.0 ms                                                         | 399 ms: 6.87x slower                                                            |
| thrift                     | 801 us                                                          | 9.80 ms: 12.24x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                    |

Benchmark hidden because not significant (3): python_startup_no_site, pickle_dict, asyncio_tcp
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.33x
- 95% likely to have a speedup of 1.32x
- 99% likely to have a speedup of 1.28x

# Memory
- memory change: unknown