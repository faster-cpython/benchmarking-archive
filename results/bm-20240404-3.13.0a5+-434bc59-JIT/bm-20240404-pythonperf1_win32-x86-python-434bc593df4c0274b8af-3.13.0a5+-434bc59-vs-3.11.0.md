# Results vs. 3.11.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-x86
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 258 ms: 1.09x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.05 ms: 1.33x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.3 ms: 1.24x faster                                                           |
| Geometric mean | (ref)                                                           | 1.19x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 539 ms: 1.40x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 215 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 543 ms: 1.37x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 483 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.37x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| nbody          | 126 ms                                                          | 101 ms: 1.25x faster                                                            |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.22x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 112 ms: 1.32x faster                                                            |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.82 ms: 1.44x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 223 us: 1.39x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 170 us: 1.36x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 43.0 ms: 1.28x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.91 us: 1.12x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_list          | 3.27 us                                                         | 3.17 us: 1.03x faster                                                           |
| pickle               | 7.99 us                                                         | 7.87 us: 1.01x faster                                                           |
| json_loads           | 20.0 us                                                         | 19.8 us: 1.01x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.0 us: 1.01x faster                                                           |
| unpickle             | 9.23 us                                                         | 9.86 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.6 ms: 1.12x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 22.4 ms: 1.19x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.16x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 7.13 ms: 1.44x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 47.6 ms: 1.29x faster                                                           |
| genshi_text    | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                           |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 99.8 us: 4.80x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.8 ms: 2.29x faster                                                           |
| logging_silent             | 119 ns                                                          | 60.1 ns: 1.98x faster                                                           |
| pylint                     | 418 ms                                                          | 222 ms: 1.88x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.5 ms: 1.70x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 24.9 us: 1.61x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.0 ms: 1.58x faster                                                           |
| richards_super             | 58.7 ms                                                         | 38.2 ms: 1.54x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.70 ms: 1.52x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 990 us: 1.51x faster                                                            |
| raytrace                   | 327 ms                                                          | 222 ms: 1.47x faster                                                            |
| richards                   | 48.8 ms                                                         | 33.4 ms: 1.46x faster                                                           |
| async_tree_none            | 343 ms                                                          | 238 ms: 1.44x faster                                                            |
| mako                       | 10.3 ms                                                         | 7.13 ms: 1.44x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.44x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.82 ms: 1.44x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 265 ms: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 286 ms: 1.43x faster                                                            |
| float                      | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| comprehensions             | 22.1 us                                                         | 15.6 us: 1.42x faster                                                           |
| chaos                      | 84.4 ms                                                         | 60.2 ms: 1.40x faster                                                           |
| async_tree_io              | 754 ms                                                          | 539 ms: 1.40x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 215 ms: 1.40x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 223 us: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 543 ms: 1.37x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 170 us: 1.36x faster                                                            |
| logging_simple             | 10.8 us                                                         | 8.02 us: 1.35x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.05 ms: 1.33x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 112 ms: 1.33x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.65 us: 1.32x faster                                                           |
| regex_compile              | 148 ms                                                          | 112 ms: 1.32x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                          |
| deepcopy                   | 381 us                                                          | 290 us: 1.32x faster                                                            |
| scimark_sor                | 135 ms                                                          | 103 ms: 1.32x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.22 ms: 1.31x faster                                                           |
| pyflate                    | 471 ms                                                          | 364 ms: 1.29x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 47.6 ms: 1.29x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 43.0 ms: 1.28x faster                                                           |
| sympy_str                  | 283 ms                                                          | 222 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 626 ms: 1.26x faster                                                            |
| nbody                      | 126 ms                                                          | 101 ms: 1.25x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 63.6 ms: 1.25x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 839 ms: 1.24x faster                                                            |
| tornado_http               | 118 ms                                                          | 95.3 ms: 1.24x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.68 us: 1.24x faster                                                           |
| go                         | 147 ms                                                          | 119 ms: 1.23x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.09 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 483 ms: 1.22x faster                                                            |
| fannkuch                   | 399 ms                                                          | 327 ms: 1.22x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.4 ms: 1.21x faster                                                           |
| nqueens                    | 111 ms                                                          | 92.2 ms: 1.21x faster                                                           |
| sympy_expand               | 462 ms                                                          | 383 ms: 1.21x faster                                                            |
| json                       | 4.78 ms                                                         | 4.01 ms: 1.19x faster                                                           |
| scimark_fft                | 291 ms                                                          | 244 ms: 1.19x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.77 sec: 1.17x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 60.9 ms: 1.16x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 88.9 ms: 1.15x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.50 sec: 1.13x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.91 us: 1.12x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 732 ms: 1.12x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 46.8 ms: 1.11x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 82.5 ms: 1.10x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| 2to3                       | 282 ms                                                          | 258 ms: 1.09x faster                                                            |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_list                | 3.27 us                                                         | 3.17 us: 1.03x faster                                                           |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| pickle                     | 7.99 us                                                         | 7.87 us: 1.01x faster                                                           |
| json_loads                 | 20.0 us                                                         | 19.8 us: 1.01x faster                                                           |
| pickle_dict                | 20.1 us                                                         | 20.0 us: 1.01x faster                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 72.5 ms: 1.02x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.46 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.86 us: 1.07x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 85.9 ms: 1.07x slower                                                           |
| async_generators           | 260 ms                                                          | 287 ms: 1.10x slower                                                            |
| python_startup             | 22.0 ms                                                         | 24.6 ms: 1.12x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 22.4 ms: 1.19x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 740 us: 1.20x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.40 ms: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 235 ms: 2.08x slower                                                            |
| coverage                   | 58.0 ms                                                         | 514 ms: 8.85x slower                                                            |
| thrift                     | 801 us                                                          | 10.6 ms: 13.23x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.17x faster                                                                    |
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown