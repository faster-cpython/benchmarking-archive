# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 258 ms: 1.09x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.25 ms: 1.29x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| html5lib       | 54.3 ms                                                         | 46.6 ms: 1.16x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.9 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 268 ms: 1.41x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 290 ms: 1.41x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 549 ms: 1.36x faster                                                            |
| async_tree_io              | 754 ms                                                          | 556 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 460 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 490 ms: 1.20x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.1 ms: 1.43x faster                                                           |
| nbody          | 126 ms                                                          | 94.8 ms: 1.33x faster                                                           |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 112 ms: 1.32x faster                                                            |
| regex_dna      | 122 ms                                                          | 121 ms: 1.01x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 222 us: 1.39x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 172 us: 1.34x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.80 sec: 1.29x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 44.2 ms: 1.24x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.0 ms: 1.16x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 61.6 ms: 1.16x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.82 us: 1.16x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 106 ms: 1.08x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 20.0 us: 1.00x faster                                                           |
| pickle               | 7.99 us                                                         | 8.13 us: 1.02x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.33 us: 1.02x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 22.0 ms: 1.17x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 6.99 ms: 1.47x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                                           |
| genshi_text    | 26.8 ms                                                         | 22.8 ms: 1.17x faster                                                           |
| Geometric mean | (ref)                                                           | 1.30x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 101 us: 4.76x faster                                                            |
| generators                 | 52.2 ms                                                         | 22.0 ms: 2.37x faster                                                           |
| logging_silent             | 119 ns                                                          | 61.0 ns: 1.95x faster                                                           |
| pylint                     | 418 ms                                                          | 224 ms: 1.87x faster                                                            |
| spectral_norm              | 122 ms                                                          | 73.6 ms: 1.65x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 24.8 us: 1.62x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.1 ms: 1.57x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.74 ms: 1.50x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 997 us: 1.49x faster                                                            |
| richards_super             | 58.7 ms                                                         | 39.5 ms: 1.48x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.99 ms: 1.47x faster                                                           |
| float                      | 76.1 ms                                                         | 53.1 ms: 1.43x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.25 ms: 1.43x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                            |
| raytrace                   | 327 ms                                                          | 231 ms: 1.42x faster                                                            |
| comprehensions             | 22.1 us                                                         | 15.6 us: 1.41x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 268 ms: 1.41x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 290 ms: 1.41x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 222 us: 1.39x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.39x faster                                                            |
| richards                   | 48.8 ms                                                         | 35.2 ms: 1.39x faster                                                           |
| chaos                      | 84.4 ms                                                         | 61.2 ms: 1.38x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 549 ms: 1.36x faster                                                            |
| async_tree_io              | 754 ms                                                          | 556 ms: 1.36x faster                                                            |
| scimark_sor                | 135 ms                                                          | 101 ms: 1.34x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 172 us: 1.34x faster                                                            |
| logging_simple             | 10.8 us                                                         | 8.11 us: 1.33x faster                                                           |
| nbody                      | 126 ms                                                          | 94.8 ms: 1.33x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 112 ms: 1.33x faster                                                            |
| regex_compile              | 148 ms                                                          | 112 ms: 1.32x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.22 ms: 1.31x faster                                                           |
| deepcopy                   | 381 us                                                          | 291 us: 1.31x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.76 us: 1.31x faster                                                           |
| pyflate                    | 471 ms                                                          | 362 ms: 1.30x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 6.25 ms: 1.29x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.80 sec: 1.29x faster                                                          |
| sympy_str                  | 283 ms                                                          | 221 ms: 1.28x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 62.4 ms: 1.27x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.61 us: 1.27x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 460 ms: 1.25x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 44.2 ms: 1.24x faster                                                           |
| fannkuch                   | 399 ms                                                          | 321 ms: 1.24x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.10 ms: 1.23x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 850 ms: 1.23x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 642 ms: 1.22x faster                                                            |
| tornado_http               | 118 ms                                                          | 96.9 ms: 1.22x faster                                                           |
| sympy_expand               | 462 ms                                                          | 382 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 490 ms: 1.20x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.6 ms: 1.20x faster                                                           |
| scimark_fft                | 291 ms                                                          | 245 ms: 1.19x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 86.2 ms: 1.19x faster                                                           |
| go                         | 147 ms                                                          | 124 ms: 1.18x faster                                                            |
| nqueens                    | 111 ms                                                          | 94.2 ms: 1.18x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 22.8 ms: 1.17x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 46.6 ms: 1.16x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.0 ms: 1.16x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 61.6 ms: 1.16x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.82 us: 1.16x faster                                                           |
| json                       | 4.78 ms                                                         | 4.13 ms: 1.16x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.80 sec: 1.15x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1.00 ms: 1.14x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 46.2 ms: 1.12x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 63.3 ms: 1.12x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 82.6 ms: 1.10x faster                                                           |
| 2to3                       | 282 ms                                                          | 258 ms: 1.09x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.98 us: 1.08x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 106 ms: 1.08x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.58 sec: 1.07x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 769 ms: 1.07x faster                                                            |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| regex_dna                  | 122 ms                                                          | 121 ms: 1.01x faster                                                            |
| pickle_dict                | 20.1 us                                                         | 20.0 us: 1.00x faster                                                           |
| pickle                     | 7.99 us                                                         | 8.13 us: 1.02x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.33 us: 1.02x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 73.8 ms: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 87.1 ms: 1.09x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                           |
| async_generators           | 260 ms                                                          | 288 ms: 1.11x slower                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 22.0 ms: 1.17x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 745 us: 1.21x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.43 ms: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 233 ms: 2.06x slower                                                            |
| coverage                   | 58.0 ms                                                         | 531 ms: 9.14x slower                                                            |
| thrift                     | 801 us                                                          | 10.7 ms: 13.41x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.16x faster                                                                    |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown