# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-x86
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 244 ms: 1.16x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.95 ms: 1.36x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.2 ms: 1.20x faster                                                           |
| tornado_http   | 118 ms                                                          | 97.4 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.21x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 281 ms: 1.46x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                            |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 53.7 ms: 2.35x faster                                                           |
| float          | 76.1 ms                                                         | 41.3 ms: 1.84x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.65x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 92.7 ms: 1.59x faster                                                           |
| regex_dna      | 122 ms                                                          | 117 ms: 1.04x faster                                                            |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 136 us: 1.71x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.38 sec: 1.68x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 198 us: 1.56x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.69 ms: 1.47x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 40.5 ms: 1.36x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 56.0 ms: 1.28x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 60.0 ms: 1.26x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.89 us: 1.13x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| pickle               | 7.99 us                                                         | 8.21 us: 1.03x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.8 us: 1.03x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.64 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 21.3 ms: 1.13x slower                                                           |
| python_startup         | 22.0 ms                                                         | 25.2 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.31 ms: 1.94x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 50.9 ms: 1.20x faster                                                           |
| django_template | 37.4 ms                                                         | 32.2 ms: 1.16x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 140 us: 3.41x faster                                                            |
| spectral_norm              | 122 ms                                                          | 47.9 ms: 2.54x faster                                                           |
| nbody                      | 126 ms                                                          | 53.7 ms: 2.35x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.3 ms: 2.24x faster                                                           |
| logging_silent             | 119 ns                                                          | 54.6 ns: 2.18x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.1 us: 1.99x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 20.2 us: 1.99x faster                                                           |
| mako                       | 10.3 ms                                                         | 5.31 ms: 1.94x faster                                                           |
| float                      | 76.1 ms                                                         | 41.3 ms: 1.84x faster                                                           |
| fannkuch                   | 399 ms                                                          | 219 ms: 1.82x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.38 ms: 1.78x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 39.9 ms: 1.78x faster                                                           |
| pylint                     | 418 ms                                                          | 238 ms: 1.75x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 136 us: 1.71x faster                                                            |
| richards_super             | 58.7 ms                                                         | 34.7 ms: 1.69x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 887 us: 1.68x faster                                                            |
| chaos                      | 84.4 ms                                                         | 50.2 ms: 1.68x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.38 sec: 1.68x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.49 ms: 1.67x faster                                                           |
| scimark_fft                | 291 ms                                                          | 176 ms: 1.66x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.51 ms: 1.63x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 49.2 ms: 1.61x faster                                                           |
| richards                   | 48.8 ms                                                         | 30.5 ms: 1.60x faster                                                           |
| regex_compile              | 148 ms                                                          | 92.7 ms: 1.59x faster                                                           |
| nqueens                    | 111 ms                                                          | 70.6 ms: 1.58x faster                                                           |
| raytrace                   | 327 ms                                                          | 208 ms: 1.57x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 198 us: 1.56x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.14 ms: 1.56x faster                                                           |
| pyflate                    | 471 ms                                                          | 305 ms: 1.54x faster                                                            |
| scimark_sor                | 135 ms                                                          | 88.1 ms: 1.54x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.8 ms: 1.50x faster                                                           |
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.15 sec: 1.48x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 555 ms: 1.48x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.36 us: 1.47x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.69 ms: 1.47x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 281 ms: 1.46x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                            |
| logging_format             | 11.5 us                                                         | 7.97 us: 1.44x faster                                                           |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 107 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 74.7 ms: 1.37x faster                                                           |
| go                         | 147 ms                                                          | 108 ms: 1.36x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 40.5 ms: 1.36x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.95 ms: 1.36x faster                                                           |
| sympy_str                  | 283 ms                                                          | 209 ms: 1.35x faster                                                            |
| pycparser                  | 1.04 sec                                                        | 778 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 56.0 ms: 1.28x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 15.6 ms: 1.28x faster                                                           |
| deepcopy                   | 381 us                                                          | 299 us: 1.27x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 71.4 ms: 1.27x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 40.7 ms: 1.27x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.27x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 60.0 ms: 1.26x faster                                                           |
| sympy_expand               | 462 ms                                                          | 370 ms: 1.25x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.66 us: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                            |
| tornado_http               | 118 ms                                                          | 97.4 ms: 1.22x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 50.9 ms: 1.20x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.2 ms: 1.20x faster                                                           |
| django_template            | 37.4 ms                                                         | 32.2 ms: 1.16x faster                                                           |
| 2to3                       | 282 ms                                                          | 244 ms: 1.16x faster                                                            |
| bench_thread_pool          | 1.14 ms                                                         | 990 us: 1.15x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.89 us: 1.13x faster                                                           |
| json                       | 4.78 ms                                                         | 4.25 ms: 1.12x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 705 ms: 1.12x faster                                                            |
| regex_dna                  | 122 ms                                                          | 117 ms: 1.04x faster                                                            |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| pickle                     | 7.99 us                                                         | 8.21 us: 1.03x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.8 us: 1.03x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 75.3 ms: 1.06x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 86.9 ms: 1.09x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.76 ms: 1.09x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.64 us: 1.12x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 21.3 ms: 1.13x slower                                                           |
| async_generators           | 260 ms                                                          | 297 ms: 1.14x slower                                                            |
| python_startup             | 22.0 ms                                                         | 25.2 ms: 1.15x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 755 us: 1.22x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 211 ms: 1.87x slower                                                            |
| coverage                   | 58.0 ms                                                         | 325 ms: 5.59x slower                                                            |
| thrift                     | 801 us                                                          | 10.6 ms: 13.18x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                    |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown