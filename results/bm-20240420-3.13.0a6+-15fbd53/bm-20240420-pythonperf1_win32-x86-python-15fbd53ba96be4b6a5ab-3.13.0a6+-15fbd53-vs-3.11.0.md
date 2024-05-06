# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 229 ms: 1.23x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| html5lib       | 54.3 ms                                                         | 42.2 ms: 1.29x faster                                                           |
| tornado_http   | 118 ms                                                          | 92.8 ms: 1.28x faster                                                           |
| Geometric mean | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 225 ms: 1.52x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 270 ms: 1.51x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 251 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.47x faster                                                            |
| async_tree_io              | 754 ms                                                          | 523 ms: 1.44x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 523 ms: 1.43x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 470 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 488 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 80.7 ms: 1.56x faster                                                           |
| float          | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 94.7 ms: 1.56x faster                                                           |
| regex_dna      | 122 ms                                                          | 124 ms: 1.02x slower                                                            |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 137 us: 1.69x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 199 us: 1.56x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 42.2 ms: 1.30x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.6 ms: 1.18x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.15x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.93 us: 1.12x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_list          | 3.27 us                                                         | 3.20 us: 1.02x faster                                                           |
| pickle               | 7.99 us                                                         | 7.84 us: 1.02x faster                                                           |
| json_loads           | 20.0 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.0 us: 1.01x faster                                                           |
| unpickle             | 9.23 us                                                         | 9.77 us: 1.06x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.19x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                                           |
| python_startup         | 22.0 ms                                                         | 21.8 ms: 1.01x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.73 ms: 1.53x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 41.4 ms: 1.48x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 18.6 ms: 1.44x faster                                                           |
| django_template | 37.4 ms                                                         | 28.8 ms: 1.30x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.43x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 89.8 us: 5.32x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.4 ms: 2.33x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.0 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 217 ms: 1.93x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.13 ms: 1.92x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.6 us: 1.91x faster                                                           |
| chaos                      | 84.4 ms                                                         | 45.0 ms: 1.88x faster                                                           |
| spectral_norm              | 122 ms                                                          | 66.8 ms: 1.82x faster                                                           |
| raytrace                   | 327 ms                                                          | 182 ms: 1.80x faster                                                            |
| richards_super             | 58.7 ms                                                         | 32.7 ms: 1.80x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 22.8 us: 1.76x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.29 ms: 1.75x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 873 us: 1.71x faster                                                            |
| scimark_sor                | 135 ms                                                          | 79.5 ms: 1.70x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 60.2 ms: 1.70x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 137 us: 1.69x faster                                                            |
| richards                   | 48.8 ms                                                         | 29.4 ms: 1.66x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.5 ms: 1.64x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.10 ms: 1.62x faster                                                           |
| nqueens                    | 111 ms                                                          | 69.4 ms: 1.60x faster                                                           |
| nbody                      | 126 ms                                                          | 80.7 ms: 1.56x faster                                                           |
| regex_compile              | 148 ms                                                          | 94.7 ms: 1.56x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 199 us: 1.56x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.0 ms: 1.54x faster                                                           |
| pyflate                    | 471 ms                                                          | 308 ms: 1.53x faster                                                            |
| mako                       | 10.3 ms                                                         | 6.73 ms: 1.53x faster                                                           |
| async_tree_none            | 343 ms                                                          | 225 ms: 1.52x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 270 ms: 1.51x faster                                                            |
| go                         | 147 ms                                                          | 97.2 ms: 1.51x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.13 sec: 1.50x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 251 ms: 1.50x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 553 ms: 1.48x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 41.4 ms: 1.48x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 101 ms: 1.48x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.47x faster                                                            |
| fannkuch                   | 399 ms                                                          | 273 ms: 1.46x faster                                                            |
| deepcopy                   | 381 us                                                          | 263 us: 1.45x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.48 us: 1.45x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.30 us: 1.44x faster                                                           |
| async_tree_io              | 754 ms                                                          | 523 ms: 1.44x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 18.6 ms: 1.44x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 55.5 ms: 1.43x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 523 ms: 1.43x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.04 us: 1.43x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                           |
| sympy_str                  | 283 ms                                                          | 200 ms: 1.42x faster                                                            |
| scimark_fft                | 291 ms                                                          | 206 ms: 1.42x faster                                                            |
| float                      | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 14.2 ms: 1.40x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.07 ms: 1.38x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 758 ms: 1.38x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 38.7 ms: 1.34x faster                                                           |
| sympy_expand               | 462 ms                                                          | 348 ms: 1.33x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 42.2 ms: 1.30x faster                                                           |
| django_template            | 37.4 ms                                                         | 28.8 ms: 1.30x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 42.2 ms: 1.29x faster                                                           |
| tornado_http               | 118 ms                                                          | 92.8 ms: 1.28x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.67 sec: 1.24x faster                                                          |
| 2to3                       | 282 ms                                                          | 229 ms: 1.23x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 639 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 470 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 488 ms: 1.21x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 75.5 ms: 1.20x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.6 ms: 1.18x faster                                                           |
| json                       | 4.78 ms                                                         | 4.07 ms: 1.18x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 971 us: 1.17x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.15x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.93 us: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 68.1 ms: 1.04x faster                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                                           |
| pidigits                   | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| pickle_list                | 3.27 us                                                         | 3.20 us: 1.02x faster                                                           |
| pickle                     | 7.99 us                                                         | 7.84 us: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| python_startup             | 22.0 ms                                                         | 21.8 ms: 1.01x faster                                                           |
| json_loads                 | 20.0 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_dict                | 20.1 us                                                         | 20.0 us: 1.01x faster                                                           |
| regex_dna                  | 122 ms                                                          | 124 ms: 1.02x slower                                                            |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 84.2 ms: 1.05x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.77 us: 1.06x slower                                                           |
| async_generators           | 260 ms                                                          | 298 ms: 1.15x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 728 us: 1.18x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.25 ms: 1.18x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 201 ms: 1.77x slower                                                            |
| coverage                   | 58.0 ms                                                         | 489 ms: 8.43x slower                                                            |
| thrift                     | 801 us                                                          | 9.59 ms: 11.98x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.29x faster                                                                    |
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.33x
- 95% likely to have a speedup of 1.31x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown