# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 255 ms: 1.11x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.27 ms: 1.29x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.93 sec: 1.08x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.4 ms: 1.20x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.5 ms: 1.24x faster                                                           |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 287 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 267 ms: 1.42x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                            |
| async_tree_io              | 754 ms                                                          | 553 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 491 ms: 1.20x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.2 ms: 1.43x faster                                                           |
| nbody          | 126 ms                                                          | 96.9 ms: 1.30x faster                                                           |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 216 us: 1.43x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.71 sec: 1.36x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 174 us: 1.33x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 43.0 ms: 1.28x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.82 us: 1.16x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.7 ms: 1.15x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_list          | 3.27 us                                                         | 3.17 us: 1.03x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                                           |
| pickle               | 7.99 us                                                         | 7.94 us: 1.01x faster                                                           |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 23.9 ms: 1.09x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 7.13 ms: 1.44x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 46.6 ms: 1.31x faster                                                           |
| genshi_text    | 26.8 ms                                                         | 20.7 ms: 1.29x faster                                                           |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 96.1 us: 4.98x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.3 ms: 2.34x faster                                                           |
| logging_silent             | 119 ns                                                          | 59.4 ns: 2.01x faster                                                           |
| pylint                     | 418 ms                                                          | 220 ms: 1.90x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.0 ms: 1.71x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 25.3 us: 1.58x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.1 ms: 1.58x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 988 us: 1.51x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.72 ms: 1.51x faster                                                           |
| raytrace                   | 327 ms                                                          | 220 ms: 1.49x faster                                                            |
| richards_super             | 58.7 ms                                                         | 39.5 ms: 1.49x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.13 ms: 1.44x faster                                                           |
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.44x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                                           |
| float                      | 76.1 ms                                                         | 53.2 ms: 1.43x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 216 us: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 287 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 267 ms: 1.42x faster                                                            |
| comprehensions             | 22.1 us                                                         | 15.6 us: 1.41x faster                                                           |
| richards                   | 48.8 ms                                                         | 34.8 ms: 1.40x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.39x faster                                                            |
| scimark_sor                | 135 ms                                                          | 97.4 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                            |
| chaos                      | 84.4 ms                                                         | 61.9 ms: 1.36x faster                                                           |
| async_tree_io              | 754 ms                                                          | 553 ms: 1.36x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.93 us: 1.36x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.71 sec: 1.36x faster                                                          |
| sympy_sum                  | 149 ms                                                          | 110 ms: 1.35x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.53 us: 1.34x faster                                                           |
| regex_compile              | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 174 us: 1.33x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 46.6 ms: 1.31x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.23 ms: 1.31x faster                                                           |
| sympy_str                  | 283 ms                                                          | 217 ms: 1.30x faster                                                            |
| pyflate                    | 471 ms                                                          | 361 ms: 1.30x faster                                                            |
| nbody                      | 126 ms                                                          | 96.9 ms: 1.30x faster                                                           |
| deepcopy                   | 381 us                                                          | 294 us: 1.30x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 607 ms: 1.30x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 20.7 ms: 1.29x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.27 ms: 1.29x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 43.0 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 63.5 ms: 1.25x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 841 ms: 1.24x faster                                                            |
| sympy_expand               | 462 ms                                                          | 373 ms: 1.24x faster                                                            |
| tornado_http               | 118 ms                                                          | 95.5 ms: 1.24x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.69 us: 1.23x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 6.12 ms: 1.23x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.4 ms: 1.22x faster                                                           |
| fannkuch                   | 399 ms                                                          | 329 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 491 ms: 1.20x faster                                                            |
| nqueens                    | 111 ms                                                          | 92.9 ms: 1.20x faster                                                           |
| go                         | 147 ms                                                          | 123 ms: 1.20x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 45.4 ms: 1.20x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.73 sec: 1.20x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 59.4 ms: 1.19x faster                                                           |
| scimark_fft                | 291 ms                                                          | 245 ms: 1.19x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 87.5 ms: 1.17x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.82 us: 1.16x faster                                                           |
| json                       | 4.78 ms                                                         | 4.12 ms: 1.16x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 981 us: 1.16x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.7 ms: 1.15x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 45.4 ms: 1.14x faster                                                           |
| 2to3                       | 282 ms                                                          | 255 ms: 1.11x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 82.0 ms: 1.11x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.53 sec: 1.10x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.95 us: 1.10x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 749 ms: 1.09x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.93 sec: 1.08x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_list                | 3.27 us                                                         | 3.17 us: 1.03x faster                                                           |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| pickle                     | 7.99 us                                                         | 7.94 us: 1.01x faster                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 71.8 ms: 1.01x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.05x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 84.6 ms: 1.06x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| python_startup             | 22.0 ms                                                         | 23.9 ms: 1.09x slower                                                           |
| async_generators           | 260 ms                                                          | 286 ms: 1.10x slower                                                            |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 749 us: 1.21x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.84 ms: 1.29x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 232 ms: 2.05x slower                                                            |
| coverage                   | 58.0 ms                                                         | 499 ms: 8.59x slower                                                            |
| thrift                     | 801 us                                                          | 10.5 ms: 13.17x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.17x faster                                                                    |

Benchmark hidden because not significant (2): json_loads, regex_dna
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown