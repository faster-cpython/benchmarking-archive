# Results vs. 3.11.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 226 ms: 1.25x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.65 ms: 1.43x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| html5lib       | 54.3 ms                                                         | 41.7 ms: 1.30x faster                                                           |
| tornado_http   | 118 ms                                                          | 92.5 ms: 1.28x faster                                                           |
| Geometric mean | (ref)                                                           | 1.28x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 222 ms: 1.55x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 265 ms: 1.54x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 249 ms: 1.52x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.48x faster                                                            |
| async_tree_io              | 754 ms                                                          | 519 ms: 1.45x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 522 ms: 1.43x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 449 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 464 ms: 1.27x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.44x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 78.4 ms: 1.61x faster                                                           |
| float          | 76.1 ms                                                         | 53.4 ms: 1.43x faster                                                           |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.33x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 95.9 ms: 1.54x faster                                                           |
| regex_dna      | 122 ms                                                          | 117 ms: 1.04x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 137 us: 1.69x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 203 us: 1.52x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.60 ms: 1.49x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.58 sec: 1.47x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.78 us: 1.18x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.9 ms: 1.15x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.24 us: 1.01x faster                                                           |
| pickle               | 7.99 us                                                         | 8.02 us: 1.00x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.19x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.0 ms: 1.04x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 6.74 ms: 1.53x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 41.8 ms: 1.46x faster                                                           |
| genshi_text    | 26.8 ms                                                         | 18.5 ms: 1.44x faster                                                           |
| Geometric mean | (ref)                                                           | 1.48x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 93.0 us: 5.14x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.2 ms: 2.35x faster                                                           |
| pylint                     | 418 ms                                                          | 206 ms: 2.03x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.12 ms: 1.94x faster                                                           |
| logging_silent             | 119 ns                                                          | 61.7 ns: 1.93x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.7 us: 1.88x faster                                                           |
| chaos                      | 84.4 ms                                                         | 45.3 ms: 1.86x faster                                                           |
| raytrace                   | 327 ms                                                          | 180 ms: 1.82x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 4.19 ms: 1.79x faster                                                           |
| richards_super             | 58.7 ms                                                         | 32.8 ms: 1.79x faster                                                           |
| spectral_norm              | 122 ms                                                          | 68.5 ms: 1.78x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 22.7 us: 1.77x faster                                                           |
| scimark_sor                | 135 ms                                                          | 77.9 ms: 1.74x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 862 us: 1.73x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 137 us: 1.69x faster                                                            |
| richards                   | 48.8 ms                                                         | 29.0 ms: 1.68x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.3 ms: 1.66x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 61.9 ms: 1.65x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.09 ms: 1.64x faster                                                           |
| nqueens                    | 111 ms                                                          | 69.3 ms: 1.61x faster                                                           |
| nbody                      | 126 ms                                                          | 78.4 ms: 1.61x faster                                                           |
| async_tree_none            | 343 ms                                                          | 222 ms: 1.55x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 265 ms: 1.54x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.0 ms: 1.54x faster                                                           |
| regex_compile              | 148 ms                                                          | 95.9 ms: 1.54x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.74 ms: 1.53x faster                                                           |
| pyflate                    | 471 ms                                                          | 309 ms: 1.52x faster                                                            |
| go                         | 147 ms                                                          | 96.6 ms: 1.52x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 203 us: 1.52x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 249 ms: 1.52x faster                                                            |
| fannkuch                   | 399 ms                                                          | 266 ms: 1.50x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.14 sec: 1.49x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.60 ms: 1.49x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.48x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 101 ms: 1.47x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 558 ms: 1.47x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.58 sec: 1.47x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 41.8 ms: 1.46x faster                                                           |
| async_tree_io              | 754 ms                                                          | 519 ms: 1.45x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 18.5 ms: 1.44x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.49 us: 1.44x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 55.1 ms: 1.44x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 522 ms: 1.43x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.65 ms: 1.43x faster                                                           |
| float                      | 76.1 ms                                                         | 53.4 ms: 1.43x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.04 us: 1.43x faster                                                           |
| sympy_str                  | 283 ms                                                          | 199 ms: 1.42x faster                                                            |
| deepcopy                   | 381 us                                                          | 269 us: 1.41x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.2 ms: 1.40x faster                                                           |
| scimark_fft                | 291 ms                                                          | 211 ms: 1.38x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.07 ms: 1.38x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 760 ms: 1.37x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 38.4 ms: 1.35x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.48 us: 1.34x faster                                                           |
| sympy_expand               | 462 ms                                                          | 349 ms: 1.32x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.57 sec: 1.31x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 41.7 ms: 1.30x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 449 ms: 1.28x faster                                                            |
| tornado_http               | 118 ms                                                          | 92.5 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 464 ms: 1.27x faster                                                            |
| 2to3                       | 282 ms                                                          | 226 ms: 1.25x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 639 ms: 1.23x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 76.7 ms: 1.19x faster                                                           |
| json                       | 4.78 ms                                                         | 4.04 ms: 1.18x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.78 us: 1.18x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 986 us: 1.15x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.9 ms: 1.15x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.91 us: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 67.9 ms: 1.04x faster                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.0 ms: 1.04x faster                                                           |
| regex_dna                  | 122 ms                                                          | 117 ms: 1.04x faster                                                            |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| pickle_dict                | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list                | 3.27 us                                                         | 3.24 us: 1.01x faster                                                           |
| pickle                     | 7.99 us                                                         | 8.02 us: 1.00x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.4 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| async_generators           | 260 ms                                                          | 287 ms: 1.10x slower                                                            |
| telco                      | 5.29 ms                                                         | 5.93 ms: 1.12x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 723 us: 1.17x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 200 ms: 1.77x slower                                                            |
| coverage                   | 58.0 ms                                                         | 503 ms: 8.66x slower                                                            |
| thrift                     | 801 us                                                          | 9.72 ms: 12.14x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.29x faster                                                                    |

Benchmark hidden because not significant (2): python_startup, json_loads
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.34x
- 95% likely to have a speedup of 1.32x
- 99% likely to have a speedup of 1.30x

# Memory
- memory change: unknown