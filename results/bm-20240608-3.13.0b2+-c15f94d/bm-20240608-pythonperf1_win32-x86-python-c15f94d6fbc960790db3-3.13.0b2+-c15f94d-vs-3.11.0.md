# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-x86
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 235 ms: 1.20x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.74 ms: 1.41x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.0 ms: 1.26x faster                                                           |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.47x faster                                                            |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 528 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 452 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 474 ms: 1.24x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 74.7 ms: 1.69x faster                                                           |
| float          | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                           |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 98.6 ms: 1.50x faster                                                           |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 146 us: 1.59x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 215 us: 1.43x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.94 ms: 1.41x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 42.2 ms: 1.30x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 59.5 ms: 1.20x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.6 ms: 1.19x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| pickle               | 7.99 us                                                         | 8.09 us: 1.01x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.5 us: 1.02x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.9 us: 1.04x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.82 us: 1.06x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.71 us: 1.13x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| python_startup         | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.86 ms: 1.50x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 44.5 ms: 1.38x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 19.5 ms: 1.37x faster                                                           |
| django_template | 37.4 ms                                                         | 30.2 ms: 1.24x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.37x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 136 us: 3.53x faster                                                            |
| generators                 | 52.2 ms                                                         | 21.4 ms: 2.43x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.2 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 217 ms: 1.93x faster                                                            |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.89x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.23 ms: 1.83x faster                                                           |
| spectral_norm              | 122 ms                                                          | 68.1 ms: 1.79x faster                                                           |
| chaos                      | 84.4 ms                                                         | 47.6 ms: 1.77x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.27 ms: 1.76x faster                                                           |
| raytrace                   | 327 ms                                                          | 190 ms: 1.73x faster                                                            |
| richards_super             | 58.7 ms                                                         | 34.6 ms: 1.70x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 60.3 ms: 1.70x faster                                                           |
| nqueens                    | 111 ms                                                          | 65.9 ms: 1.69x faster                                                           |
| nbody                      | 126 ms                                                          | 74.7 ms: 1.69x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 23.9 us: 1.67x faster                                                           |
| scimark_sor                | 135 ms                                                          | 81.6 ms: 1.66x faster                                                           |
| richards                   | 48.8 ms                                                         | 30.4 ms: 1.60x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 932 us: 1.60x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 146 us: 1.59x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.16 ms: 1.53x faster                                                           |
| pyflate                    | 471 ms                                                          | 307 ms: 1.53x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.5 ms: 1.53x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.4 ms: 1.53x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.79 ms: 1.52x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.86 ms: 1.50x faster                                                           |
| regex_compile              | 148 ms                                                          | 98.6 ms: 1.50x faster                                                           |
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                            |
| scimark_fft                | 291 ms                                                          | 198 ms: 1.47x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.47x faster                                                            |
| go                         | 147 ms                                                          | 102 ms: 1.45x faster                                                            |
| float                      | 76.1 ms                                                         | 52.7 ms: 1.44x faster                                                           |
| fannkuch                   | 399 ms                                                          | 277 ms: 1.44x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 55.3 ms: 1.44x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 215 us: 1.43x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.54 us: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 105 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 528 ms: 1.41x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.94 ms: 1.41x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.74 ms: 1.41x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.15 us: 1.40x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 44.5 ms: 1.38x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 19.5 ms: 1.37x faster                                                           |
| sympy_str                  | 283 ms                                                          | 207 ms: 1.37x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.6 ms: 1.36x faster                                                           |
| deepcopy                   | 381 us                                                          | 283 us: 1.35x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.27 sec: 1.34x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 617 ms: 1.33x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 39.2 ms: 1.32x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 42.2 ms: 1.30x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 802 ms: 1.30x faster                                                            |
| sympy_expand               | 462 ms                                                          | 362 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 452 ms: 1.28x faster                                                            |
| tornado_http               | 118 ms                                                          | 94.0 ms: 1.26x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 72.5 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 474 ms: 1.24x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.66 sec: 1.24x faster                                                          |
| django_template            | 37.4 ms                                                         | 30.2 ms: 1.24x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.72 us: 1.22x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 59.5 ms: 1.20x faster                                                           |
| 2to3                       | 282 ms                                                          | 235 ms: 1.20x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 658 ms: 1.20x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.6 ms: 1.19x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 966 us: 1.18x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| json                       | 4.78 ms                                                         | 4.22 ms: 1.13x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| sqlite_synth               | 2.15 us                                                         | 1.95 us: 1.10x faster                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 69.9 ms: 1.02x faster                                                           |
| pickle                     | 7.99 us                                                         | 8.09 us: 1.01x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.5 us: 1.02x slower                                                           |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| async_generators           | 260 ms                                                          | 270 ms: 1.04x slower                                                            |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.9 us: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.6 ms: 1.05x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.82 us: 1.06x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.71 us: 1.13x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.07 ms: 1.15x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 747 us: 1.21x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 202 ms: 1.79x slower                                                            |
| coverage                   | 58.0 ms                                                         | 305 ms: 5.25x slower                                                            |
| thrift                     | 801 us                                                          | 9.72 ms: 12.14x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                                    |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown