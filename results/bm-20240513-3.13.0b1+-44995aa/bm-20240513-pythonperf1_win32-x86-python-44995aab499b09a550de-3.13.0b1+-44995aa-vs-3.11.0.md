# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-x86
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 236 ms: 1.19x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.72 ms: 1.41x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| html5lib       | 54.3 ms                                                         | 44.9 ms: 1.21x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.6 ms: 1.25x faster                                                           |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 200 ms: 1.50x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                            |
| async_tree_io              | 754 ms                                                          | 533 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 445 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.42x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 76.2 ms: 1.65x faster                                                           |
| float          | 76.1 ms                                                         | 52.4 ms: 1.45x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 101 ms: 1.46x faster                                                            |
| regex_dna      | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 151 us: 1.53x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 218 us: 1.42x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 41.4 ms: 1.33x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 58.5 ms: 1.22x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.2 ms: 1.20x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| unpickle_list        | 3.28 us                                                         | 3.07 us: 1.07x faster                                                           |
| pickle               | 7.99 us                                                         | 8.12 us: 1.02x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.6 us: 1.03x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.52 us: 1.08x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.6 us: 1.15x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.2 ms: 1.03x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.99 ms: 1.47x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 44.3 ms: 1.38x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.3 ms: 1.32x faster                                                           |
| django_template | 37.4 ms                                                         | 31.0 ms: 1.21x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.34x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 138 us: 3.47x faster                                                            |
| generators                 | 52.2 ms                                                         | 21.2 ms: 2.46x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.0 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 220 ms: 1.90x faster                                                            |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.89x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.22 ms: 1.85x faster                                                           |
| raytrace                   | 327 ms                                                          | 182 ms: 1.80x faster                                                            |
| spectral_norm              | 122 ms                                                          | 68.0 ms: 1.79x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 59.2 ms: 1.73x faster                                                           |
| chaos                      | 84.4 ms                                                         | 49.2 ms: 1.72x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 23.5 us: 1.70x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.43 ms: 1.70x faster                                                           |
| nbody                      | 126 ms                                                          | 76.2 ms: 1.65x faster                                                           |
| richards_super             | 58.7 ms                                                         | 35.7 ms: 1.64x faster                                                           |
| scimark_sor                | 135 ms                                                          | 82.6 ms: 1.64x faster                                                           |
| nqueens                    | 111 ms                                                          | 69.2 ms: 1.61x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 959 us: 1.55x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 45.6 ms: 1.55x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.7 ms: 1.54x faster                                                           |
| pyflate                    | 471 ms                                                          | 307 ms: 1.54x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 151 us: 1.53x faster                                                            |
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                            |
| fannkuch                   | 399 ms                                                          | 265 ms: 1.51x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.82 ms: 1.50x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 200 ms: 1.50x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 16.0 ms: 1.48x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.99 ms: 1.47x faster                                                           |
| regex_compile              | 148 ms                                                          | 101 ms: 1.46x faster                                                            |
| float                      | 76.1 ms                                                         | 52.4 ms: 1.45x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 54.9 ms: 1.45x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 105 ms: 1.42x faster                                                            |
| go                         | 147 ms                                                          | 104 ms: 1.42x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 218 us: 1.42x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.63 us: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 533 ms: 1.42x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.72 ms: 1.41x faster                                                           |
| scimark_fft                | 291 ms                                                          | 207 ms: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 44.3 ms: 1.38x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.30 us: 1.38x faster                                                           |
| sympy_str                  | 283 ms                                                          | 208 ms: 1.36x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.24 sec: 1.36x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 14.7 ms: 1.36x faster                                                           |
| deepcopy                   | 381 us                                                          | 282 us: 1.35x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 610 ms: 1.34x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 41.4 ms: 1.33x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.3 ms: 1.32x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 798 ms: 1.31x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 445 ms: 1.30x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 40.2 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 468 ms: 1.26x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.65 sec: 1.25x faster                                                          |
| tornado_http               | 118 ms                                                          | 94.6 ms: 1.25x faster                                                           |
| sympy_expand               | 462 ms                                                          | 370 ms: 1.25x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 73.3 ms: 1.24x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.70 us: 1.23x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 58.5 ms: 1.22x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 44.9 ms: 1.21x faster                                                           |
| django_template            | 37.4 ms                                                         | 31.0 ms: 1.21x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.2 ms: 1.20x faster                                                           |
| 2to3                       | 282 ms                                                          | 236 ms: 1.19x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 987 us: 1.15x faster                                                            |
| json                       | 4.78 ms                                                         | 4.17 ms: 1.15x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.96 us: 1.10x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 734 ms: 1.07x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 3.07 us: 1.07x faster                                                           |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 18.2 ms: 1.03x faster                                                           |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| async_generators           | 260 ms                                                          | 261 ms: 1.00x slower                                                            |
| pickle                     | 7.99 us                                                         | 8.12 us: 1.02x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.6 us: 1.03x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.05x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.52 us: 1.08x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 88.7 ms: 1.11x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.01 ms: 1.13x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.6 us: 1.15x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 737 us: 1.19x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 209 ms: 1.85x slower                                                            |
| coverage                   | 58.0 ms                                                         | 310 ms: 5.33x slower                                                            |
| thrift                     | 801 us                                                          | 10.1 ms: 12.60x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                    |

Benchmark hidden because not significant (3): flaskblogging, bench_mp_pool, python_startup
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown