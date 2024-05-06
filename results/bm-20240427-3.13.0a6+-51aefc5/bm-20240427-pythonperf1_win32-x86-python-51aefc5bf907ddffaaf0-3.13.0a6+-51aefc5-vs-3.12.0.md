# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 231 ms: 1.21x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.56 ms: 1.39x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.81 sec: 1.10x faster                                                          |
| tornado_http   | 105 ms                                                          | 104 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 251 ms: 1.40x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 267 ms: 1.36x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| async_tree_none            | 298 ms                                                          | 221 ms: 1.35x faster                                                            |
| async_tree_io              | 693 ms                                                          | 517 ms: 1.34x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 526 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 449 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 468 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.31x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 80.9 ms: 1.57x faster                                                           |
| float          | 76.7 ms                                                         | 52.7 ms: 1.46x faster                                                           |
| pidigits       | 199 ms                                                          | 200 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 95.0 ms: 1.36x faster                                                           |
| regex_dna      | 127 ms                                                          | 121 ms: 1.05x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.94 ms: 1.05x faster                                                           |
| regex_v8       | 15.0 ms                                                         | 16.4 ms: 1.09x slower                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 138 us: 1.52x faster                                                            |
| pickle_pure_python   | 286 us                                                          | 202 us: 1.42x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 42.0 ms: 1.27x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 59.8 ms: 1.21x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.5 ms: 1.19x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 103 ms: 1.10x faster                                                            |
| json_dumps           | 7.40 ms                                                         | 6.75 ms: 1.10x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.2 us: 1.01x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| pickle               | 7.79 us                                                         | 7.92 us: 1.02x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.94 us: 1.02x slower                                                           |
| pickle_list          | 3.37 us                                                         | 3.59 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                    |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.7 ms: 1.02x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.87 ms: 1.45x faster                                                           |
| django_template | 36.9 ms                                                         | 28.1 ms: 1.31x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.38x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.1 ms: 1.74x faster                                                           |
| logging_silent             | 101 ns                                                          | 58.1 ns: 1.74x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 22.6 us: 1.70x faster                                                           |
| raytrace                   | 308 ms                                                          | 184 ms: 1.68x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.15 ms: 1.67x faster                                                           |
| scimark_sor                | 130 ms                                                          | 78.5 ms: 1.65x faster                                                           |
| comprehensions             | 19.2 us                                                         | 11.7 us: 1.65x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 4.18 ms: 1.63x faster                                                           |
| nbody                      | 127 ms                                                          | 80.9 ms: 1.57x faster                                                           |
| chaos                      | 69.4 ms                                                         | 44.8 ms: 1.55x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 60.2 ms: 1.55x faster                                                           |
| spectral_norm              | 104 ms                                                          | 67.9 ms: 1.53x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 138 us: 1.52x faster                                                            |
| float                      | 76.7 ms                                                         | 52.7 ms: 1.46x faster                                                           |
| mako                       | 9.96 ms                                                         | 6.87 ms: 1.45x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 46.1 ms: 1.44x faster                                                           |
| go                         | 137 ms                                                          | 96.2 ms: 1.43x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 66.0 ms: 1.42x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 202 us: 1.42x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 883 us: 1.41x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 251 ms: 1.40x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 5.56 ms: 1.39x faster                                                           |
| richards_super             | 46.5 ms                                                         | 33.4 ms: 1.39x faster                                                           |
| richards                   | 41.3 ms                                                         | 29.8 ms: 1.39x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.12 ms: 1.37x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.13 us: 1.37x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 267 ms: 1.36x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| regex_compile              | 129 ms                                                          | 95.0 ms: 1.36x faster                                                           |
| logging_format             | 10.4 us                                                         | 7.66 us: 1.36x faster                                                           |
| pyflate                    | 424 ms                                                          | 314 ms: 1.35x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| async_tree_none            | 298 ms                                                          | 221 ms: 1.35x faster                                                            |
| async_tree_io              | 693 ms                                                          | 517 ms: 1.34x faster                                                            |
| deepcopy                   | 360 us                                                          | 269 us: 1.34x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.12 sec: 1.33x faster                                                          |
| coroutines                 | 20.9 ms                                                         | 15.7 ms: 1.33x faster                                                           |
| django_template            | 36.9 ms                                                         | 28.1 ms: 1.31x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 549 ms: 1.31x faster                                                            |
| fannkuch                   | 354 ms                                                          | 270 ms: 1.31x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.47 us: 1.31x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 2.99 ms: 1.29x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 526 ms: 1.29x faster                                                            |
| scimark_fft                | 271 ms                                                          | 212 ms: 1.28x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 42.0 ms: 1.27x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 38.3 ms: 1.27x faster                                                           |
| pycparser                  | 978 ms                                                          | 773 ms: 1.27x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 55.1 ms: 1.26x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 14.4 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 449 ms: 1.22x faster                                                            |
| 2to3                       | 280 ms                                                          | 231 ms: 1.21x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 59.8 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 468 ms: 1.21x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 102 ms: 1.20x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.61 sec: 1.19x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.5 ms: 1.19x faster                                                           |
| sympy_str                  | 240 ms                                                          | 202 ms: 1.19x faster                                                            |
| meteor_contest             | 86.9 ms                                                         | 74.4 ms: 1.17x faster                                                           |
| sympy_expand               | 398 ms                                                          | 351 ms: 1.13x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 995 us: 1.11x faster                                                            |
| async_generators           | 313 ms                                                          | 283 ms: 1.11x faster                                                            |
| xml_etree_parse            | 113 ms                                                          | 103 ms: 1.10x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.81 sec: 1.10x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.75 ms: 1.10x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 70.0 ms: 1.08x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.94 us: 1.07x faster                                                           |
| regex_dna                  | 127 ms                                                          | 121 ms: 1.05x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.94 ms: 1.05x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 88.7 ms: 1.03x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 17.2 sec: 1.03x faster                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 18.7 ms: 1.02x faster                                                           |
| tornado_http               | 105 ms                                                          | 104 ms: 1.01x faster                                                            |
| json_loads                 | 20.4 us                                                         | 20.2 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 200 ms: 1.00x slower                                                            |
| gc_traversal               | 1.44 ms                                                         | 1.45 ms: 1.01x slower                                                           |
| pickle_dict                | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| pickle                     | 7.79 us                                                         | 7.92 us: 1.02x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.94 us: 1.02x slower                                                           |
| typing_runtime_protocols   | 126 us                                                          | 131 us: 1.04x slower                                                            |
| pickle_list                | 3.37 us                                                         | 3.59 us: 1.07x slower                                                           |
| telco                      | 5.51 ms                                                         | 5.98 ms: 1.08x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.4 ms: 1.09x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 743 us: 1.14x slower                                                            |
| asyncio_tcp                | 662 ms                                                          | 812 ms: 1.23x slower                                                            |
| sqlglot_normalize          | 100 ms                                                          | 193 ms: 1.93x slower                                                            |
| coverage                   | 48.4 ms                                                         | 399 ms: 8.23x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.20x faster                                                                    |

Benchmark hidden because not significant (3): unpickle_list, json, python_startup
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.22x
- 95% likely to have a speedup of 1.21x
- 99% likely to have a speedup of 1.19x

# Memory
- memory change: unknown