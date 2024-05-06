# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 253 ms: 1.12x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.02 ms: 1.34x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.0 ms: 1.25x faster                                                           |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 240 ms: 1.43x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 266 ms: 1.42x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 289 ms: 1.41x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 215 ms: 1.40x faster                                                            |
| async_tree_io              | 754 ms                                                          | 540 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 484 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.36x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 52.2 ms: 1.46x faster                                                           |
| nbody          | 126 ms                                                          | 92.0 ms: 1.37x faster                                                           |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                           |
| unpickle_pure_python | 231 us                                                          | 164 us: 1.41x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 222 us: 1.39x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.73 sec: 1.34x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 43.7 ms: 1.26x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 62.6 ms: 1.14x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.4 ms: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 109 ms: 1.05x faster                                                            |
| pickle_list          | 3.27 us                                                         | 3.19 us: 1.02x faster                                                           |
| json_loads           | 20.0 us                                                         | 19.8 us: 1.01x faster                                                           |
| pickle               | 7.99 us                                                         | 7.96 us: 1.00x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.2 us: 1.00x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.7 ms: 1.10x slower                                                           |
| python_startup         | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.88 ms: 1.49x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 44.7 ms: 1.37x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.4 ms: 1.31x faster                                                           |
| django_template | 37.4 ms                                                         | 33.3 ms: 1.12x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.32x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 95.5 us: 5.01x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.5 ms: 2.32x faster                                                           |
| logging_silent             | 119 ns                                                          | 59.9 ns: 1.99x faster                                                           |
| pylint                     | 418 ms                                                          | 233 ms: 1.79x faster                                                            |
| spectral_norm              | 122 ms                                                          | 70.6 ms: 1.72x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 24.9 us: 1.61x faster                                                           |
| richards_super             | 58.7 ms                                                         | 37.5 ms: 1.57x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.6 ms: 1.52x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.71 ms: 1.51x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 994 us: 1.50x faster                                                            |
| mako                       | 10.3 ms                                                         | 6.88 ms: 1.49x faster                                                           |
| richards                   | 48.8 ms                                                         | 33.0 ms: 1.48x faster                                                           |
| raytrace                   | 327 ms                                                          | 223 ms: 1.47x faster                                                            |
| float                      | 76.1 ms                                                         | 52.2 ms: 1.46x faster                                                           |
| comprehensions             | 22.1 us                                                         | 15.2 us: 1.46x faster                                                           |
| chaos                      | 84.4 ms                                                         | 58.0 ms: 1.45x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                           |
| async_tree_none            | 343 ms                                                          | 240 ms: 1.43x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.25 ms: 1.43x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 266 ms: 1.42x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 289 ms: 1.41x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 164 us: 1.41x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 215 ms: 1.40x faster                                                            |
| async_tree_io              | 754 ms                                                          | 540 ms: 1.40x faster                                                            |
| scimark_sor                | 135 ms                                                          | 97.3 ms: 1.39x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 222 us: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 44.7 ms: 1.37x faster                                                           |
| nbody                      | 126 ms                                                          | 92.0 ms: 1.37x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 110 ms: 1.35x faster                                                            |
| regex_compile              | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.73 sec: 1.34x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 6.02 ms: 1.34x faster                                                           |
| logging_simple             | 10.8 us                                                         | 8.09 us: 1.34x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.17 ms: 1.33x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.66 us: 1.32x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.4 ms: 1.31x faster                                                           |
| sympy_str                  | 283 ms                                                          | 218 ms: 1.30x faster                                                            |
| deepcopy                   | 381 us                                                          | 295 us: 1.29x faster                                                            |
| pyflate                    | 471 ms                                                          | 366 ms: 1.29x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 5.86 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.27x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 43.7 ms: 1.26x faster                                                           |
| fannkuch                   | 399 ms                                                          | 317 ms: 1.26x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 63.2 ms: 1.26x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.65 us: 1.25x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 835 ms: 1.25x faster                                                            |
| tornado_http               | 118 ms                                                          | 95.0 ms: 1.25x faster                                                           |
| go                         | 147 ms                                                          | 119 ms: 1.24x faster                                                            |
| nqueens                    | 111 ms                                                          | 90.7 ms: 1.23x faster                                                           |
| sympy_expand               | 462 ms                                                          | 377 ms: 1.23x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.3 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 484 ms: 1.22x faster                                                            |
| scimark_fft                | 291 ms                                                          | 241 ms: 1.21x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 652 ms: 1.21x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.72 sec: 1.20x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 60.4 ms: 1.17x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 88.0 ms: 1.16x faster                                                           |
| json                       | 4.78 ms                                                         | 4.13 ms: 1.16x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 62.6 ms: 1.14x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.4 ms: 1.14x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 45.7 ms: 1.13x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.50 sec: 1.13x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 80.7 ms: 1.13x faster                                                           |
| django_template            | 37.4 ms                                                         | 33.3 ms: 1.12x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                                           |
| 2to3                       | 282 ms                                                          | 253 ms: 1.12x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 735 ms: 1.12x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 109 ms: 1.05x faster                                                            |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| pickle_list                | 3.27 us                                                         | 3.19 us: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| json_loads                 | 20.0 us                                                         | 19.8 us: 1.01x faster                                                           |
| pickle                     | 7.99 us                                                         | 7.96 us: 1.00x faster                                                           |
| pickle_dict                | 20.1 us                                                         | 20.2 us: 1.00x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 74.2 ms: 1.05x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.9 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 20.7 ms: 1.10x slower                                                           |
| python_startup             | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| async_generators           | 260 ms                                                          | 289 ms: 1.11x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 727 us: 1.18x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.36 ms: 1.20x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 234 ms: 2.07x slower                                                            |
| coverage                   | 58.0 ms                                                         | 499 ms: 8.59x slower                                                            |
| thrift                     | 801 us                                                          | 10.6 ms: 13.25x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.18x faster                                                                    |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown