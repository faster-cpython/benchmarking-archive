# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 255 ms: 1.11x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.13 ms: 1.32x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| html5lib       | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.4 ms: 1.23x faster                                                           |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 231 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 544 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 481 ms: 1.23x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.37x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| nbody          | 126 ms                                                          | 98.8 ms: 1.27x faster                                                           |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.23x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 113 ms: 1.30x faster                                                            |
| regex_dna      | 122 ms                                                          | 125 ms: 1.02x slower                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.93 ms: 1.06x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.78 ms: 1.45x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 227 us: 1.36x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 171 us: 1.35x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.72 sec: 1.35x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.80 us: 1.17x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 61.7 ms: 1.16x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.25 us: 1.01x faster                                                           |
| json_loads           | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| pickle               | 7.99 us                                                         | 8.18 us: 1.02x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.88 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 21.9 ms: 1.17x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.24 ms: 1.42x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 47.7 ms: 1.28x faster                                                           |
| django_template | 37.4 ms                                                         | 33.2 ms: 1.13x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.29x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 98.2 us: 4.87x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.27x faster                                                           |
| logging_silent             | 119 ns                                                          | 60.7 ns: 1.96x faster                                                           |
| pylint                     | 418 ms                                                          | 223 ms: 1.88x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.3 ms: 1.71x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.8 ms: 1.61x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.59 ms: 1.58x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 26.5 us: 1.51x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 996 us: 1.50x faster                                                            |
| async_tree_none            | 343 ms                                                          | 231 ms: 1.49x faster                                                            |
| unpack_sequence            | 65.2 ns                                                         | 44.0 ns: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.78 ms: 1.45x faster                                                           |
| richards_super             | 58.7 ms                                                         | 40.6 ms: 1.44x faster                                                           |
| comprehensions             | 22.1 us                                                         | 15.3 us: 1.44x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.43x faster                                                            |
| float                      | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.24 ms: 1.42x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.26 ms: 1.41x faster                                                           |
| async_tree_io              | 754 ms                                                          | 544 ms: 1.39x faster                                                            |
| chaos                      | 84.4 ms                                                         | 61.8 ms: 1.37x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                            |
| scimark_sor                | 135 ms                                                          | 99.1 ms: 1.36x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 109 ms: 1.36x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 227 us: 1.36x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 171 us: 1.35x faster                                                            |
| richards                   | 48.8 ms                                                         | 36.1 ms: 1.35x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.72 sec: 1.35x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.18 ms: 1.33x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.13 ms: 1.32x faster                                                           |
| sympy_str                  | 283 ms                                                          | 217 ms: 1.30x faster                                                            |
| regex_compile              | 148 ms                                                          | 113 ms: 1.30x faster                                                            |
| deepcopy                   | 381 us                                                          | 295 us: 1.29x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 47.7 ms: 1.28x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 62.0 ms: 1.28x faster                                                           |
| pyflate                    | 471 ms                                                          | 369 ms: 1.28x faster                                                            |
| fannkuch                   | 399 ms                                                          | 313 ms: 1.27x faster                                                            |
| nbody                      | 126 ms                                                          | 98.8 ms: 1.27x faster                                                           |
| logging_simple             | 10.8 us                                                         | 8.50 us: 1.27x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                           |
| logging_format             | 11.5 us                                                         | 9.05 us: 1.27x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.63 us: 1.26x faster                                                           |
| raytrace                   | 327 ms                                                          | 260 ms: 1.26x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 632 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                            |
| tornado_http               | 118 ms                                                          | 96.4 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 481 ms: 1.23x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.3 ms: 1.22x faster                                                           |
| sympy_expand               | 462 ms                                                          | 378 ms: 1.22x faster                                                            |
| go                         | 147 ms                                                          | 122 ms: 1.20x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.24 ms: 1.20x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 871 ms: 1.20x faster                                                            |
| nqueens                    | 111 ms                                                          | 93.0 ms: 1.20x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                           |
| scimark_fft                | 291 ms                                                          | 247 ms: 1.18x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.80 us: 1.17x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.78 sec: 1.16x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 61.7 ms: 1.16x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.49 sec: 1.14x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 62.4 ms: 1.13x faster                                                           |
| django_template            | 37.4 ms                                                         | 33.2 ms: 1.13x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 46.3 ms: 1.12x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 81.2 ms: 1.12x faster                                                           |
| 2to3                       | 282 ms                                                          | 255 ms: 1.11x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 741 ms: 1.11x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.95 us: 1.10x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| json                       | 4.78 ms                                                         | 4.50 ms: 1.06x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 96.7 ms: 1.06x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| pickle_dict                | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list                | 3.27 us                                                         | 3.25 us: 1.01x faster                                                           |
| json_loads                 | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 72.3 ms: 1.02x slower                                                           |
| pickle                     | 7.99 us                                                         | 8.18 us: 1.02x slower                                                           |
| regex_dna                  | 122 ms                                                          | 125 ms: 1.02x slower                                                            |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.93 ms: 1.06x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.88 us: 1.07x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 86.0 ms: 1.08x slower                                                           |
| python_startup             | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| async_generators           | 260 ms                                                          | 295 ms: 1.14x slower                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 21.9 ms: 1.17x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.33 ms: 1.19x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 740 us: 1.20x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 238 ms: 2.11x slower                                                            |
| coverage                   | 58.0 ms                                                         | 482 ms: 8.30x slower                                                            |
| thrift                     | 801 us                                                          | 11.0 ms: 13.70x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.16x faster                                                                    |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown