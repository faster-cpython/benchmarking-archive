# Results vs. 3.11.0

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-x86
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 257 ms: 1.10x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.17 ms: 1.31x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.93 sec: 1.09x faster                                                          |
| html5lib       | 54.3 ms                                                         | 46.5 ms: 1.17x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.1 ms: 1.23x faster                                                           |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 264 ms: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 547 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 549 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.38x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.6 ms: 1.42x faster                                                           |
| nbody          | 126 ms                                                          | 95.8 ms: 1.31x faster                                                           |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 114 ms: 1.30x faster                                                            |
| regex_dna      | 122 ms                                                          | 120 ms: 1.02x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.93 ms: 1.42x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 220 us: 1.40x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.73 sec: 1.34x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 180 us: 1.29x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 43.7 ms: 1.26x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.85 us: 1.15x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 62.4 ms: 1.15x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.07x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| json_loads           | 20.0 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.25 us: 1.00x faster                                                           |
| unpickle             | 9.23 us                                                         | 10.0 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.3 ms: 1.10x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 21.9 ms: 1.17x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.10 ms: 1.45x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 48.6 ms: 1.26x faster                                                           |
| django_template | 37.4 ms                                                         | 33.4 ms: 1.12x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.27x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 96.5 us: 4.96x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.1 ms: 2.26x faster                                                           |
| logging_silent             | 119 ns                                                          | 60.3 ns: 1.98x faster                                                           |
| pylint                     | 418 ms                                                          | 222 ms: 1.88x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.2 ms: 1.71x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.7 ms: 1.61x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.62 ms: 1.56x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 26.3 us: 1.52x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.01 ms: 1.48x faster                                                           |
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                            |
| richards_super             | 58.7 ms                                                         | 40.2 ms: 1.46x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.45x faster                                                            |
| mako                       | 10.3 ms                                                         | 7.10 ms: 1.45x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 264 ms: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                            |
| float                      | 76.1 ms                                                         | 53.6 ms: 1.42x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.93 ms: 1.42x faster                                                           |
| comprehensions             | 22.1 us                                                         | 15.6 us: 1.41x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.26 ms: 1.41x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 220 us: 1.40x faster                                                            |
| unpack_sequence            | 65.2 ns                                                         | 46.6 ns: 1.40x faster                                                           |
| async_tree_io              | 754 ms                                                          | 547 ms: 1.38x faster                                                            |
| richards                   | 48.8 ms                                                         | 35.6 ms: 1.37x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 549 ms: 1.36x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 110 ms: 1.35x faster                                                            |
| scimark_sor                | 135 ms                                                          | 100.0 ms: 1.35x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.73 sec: 1.34x faster                                                          |
| chaos                      | 84.4 ms                                                         | 63.1 ms: 1.34x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.19 ms: 1.33x faster                                                           |
| nbody                      | 126 ms                                                          | 95.8 ms: 1.31x faster                                                           |
| logging_simple             | 10.8 us                                                         | 8.24 us: 1.31x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.17 ms: 1.31x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 604 ms: 1.30x faster                                                            |
| sympy_str                  | 283 ms                                                          | 218 ms: 1.30x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.81 us: 1.30x faster                                                           |
| regex_compile              | 148 ms                                                          | 114 ms: 1.30x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 180 us: 1.29x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 61.8 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| pyflate                    | 471 ms                                                          | 370 ms: 1.27x faster                                                            |
| deepcopy                   | 381 us                                                          | 300 us: 1.27x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 43.7 ms: 1.26x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 48.6 ms: 1.26x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.64 us: 1.26x faster                                                           |
| fannkuch                   | 399 ms                                                          | 319 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| tornado_http               | 118 ms                                                          | 96.1 ms: 1.23x faster                                                           |
| scimark_fft                | 291 ms                                                          | 237 ms: 1.23x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.4 ms: 1.22x faster                                                           |
| sympy_expand               | 462 ms                                                          | 381 ms: 1.21x faster                                                            |
| nqueens                    | 111 ms                                                          | 92.1 ms: 1.21x faster                                                           |
| raytrace                   | 327 ms                                                          | 273 ms: 1.20x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.28 ms: 1.20x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 872 ms: 1.20x faster                                                            |
| go                         | 147 ms                                                          | 123 ms: 1.19x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 46.5 ms: 1.17x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.78 sec: 1.16x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 61.5 ms: 1.15x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.85 us: 1.15x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 62.4 ms: 1.15x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.13x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.51 sec: 1.12x faster                                                          |
| django_template            | 37.4 ms                                                         | 33.4 ms: 1.12x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 46.5 ms: 1.11x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 742 ms: 1.10x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 93.0 ms: 1.10x faster                                                           |
| 2to3                       | 282 ms                                                          | 257 ms: 1.10x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.93 sec: 1.09x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 83.9 ms: 1.08x faster                                                           |
| json                       | 4.78 ms                                                         | 4.45 ms: 1.07x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.07x faster                                                            |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.02x faster                                                            |
| pickle_dict                | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| json_loads                 | 20.0 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list                | 3.27 us                                                         | 3.25 us: 1.00x faster                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 72.2 ms: 1.02x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 86.3 ms: 1.08x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.0 us: 1.09x slower                                                           |
| async_generators           | 260 ms                                                          | 285 ms: 1.10x slower                                                            |
| python_startup             | 22.0 ms                                                         | 24.3 ms: 1.10x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 21.9 ms: 1.17x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 737 us: 1.19x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.50 ms: 1.23x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 241 ms: 2.13x slower                                                            |
| coverage                   | 58.0 ms                                                         | 487 ms: 8.39x slower                                                            |
| thrift                     | 801 us                                                          | 10.9 ms: 13.66x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.16x faster                                                                    |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown