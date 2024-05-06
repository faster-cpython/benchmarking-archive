# Results vs. 3.11.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.22 ms: 1.30x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.2 ms: 1.26x faster                                                           |
| Geometric mean | (ref)                                                           | 1.19x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.44x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 211 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 537 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 481 ms: 1.23x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.38x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| nbody          | 126 ms                                                          | 97.3 ms: 1.29x faster                                                           |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.4 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                    |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.62 ms: 1.48x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 220 us: 1.40x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 166 us: 1.40x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.66 sec: 1.39x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 44.3 ms: 1.24x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.83 us: 1.16x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 63.2 ms: 1.13x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.9 ms: 1.13x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 111 ms: 1.03x faster                                                            |
| pickle_list          | 3.27 us                                                         | 3.19 us: 1.02x faster                                                           |
| pickle               | 7.99 us                                                         | 8.01 us: 1.00x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.1 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmark hidden because not significant (2): pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.1 ms: 1.07x slower                                                           |
| python_startup         | 22.0 ms                                                         | 23.7 ms: 1.08x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 7.03 ms: 1.46x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                                           |
| genshi_text    | 26.8 ms                                                         | 22.5 ms: 1.19x faster                                                           |
| Geometric mean | (ref)                                                           | 1.30x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 93.8 us: 5.10x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.1 ms: 2.37x faster                                                           |
| logging_silent             | 119 ns                                                          | 60.3 ns: 1.98x faster                                                           |
| pylint                     | 418 ms                                                          | 220 ms: 1.90x faster                                                            |
| spectral_norm              | 122 ms                                                          | 70.0 ms: 1.74x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.9 ms: 1.60x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 25.5 us: 1.57x faster                                                           |
| richards_super             | 58.7 ms                                                         | 38.3 ms: 1.53x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.68 ms: 1.53x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 990 us: 1.51x faster                                                            |
| raytrace                   | 327 ms                                                          | 221 ms: 1.48x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.62 ms: 1.48x faster                                                           |
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                            |
| chaos                      | 84.4 ms                                                         | 57.3 ms: 1.47x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.03 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| comprehensions             | 22.1 us                                                         | 15.3 us: 1.45x faster                                                           |
| richards                   | 48.8 ms                                                         | 33.8 ms: 1.44x faster                                                           |
| scimark_sor                | 135 ms                                                          | 93.7 ms: 1.44x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.44x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.44x faster                                                           |
| float                      | 76.1 ms                                                         | 53.3 ms: 1.43x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 211 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 537 ms: 1.40x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 220 us: 1.40x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 166 us: 1.40x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.66 sec: 1.39x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 109 ms: 1.37x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.98 us: 1.35x faster                                                           |
| regex_compile              | 148 ms                                                          | 110 ms: 1.34x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.58 us: 1.34x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.20 ms: 1.32x faster                                                           |
| sympy_str                  | 283 ms                                                          | 215 ms: 1.32x faster                                                            |
| pyflate                    | 471 ms                                                          | 361 ms: 1.30x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 6.22 ms: 1.30x faster                                                           |
| nbody                      | 126 ms                                                          | 97.3 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                                           |
| tornado_http               | 118 ms                                                          | 94.2 ms: 1.26x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 626 ms: 1.26x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 5.98 ms: 1.26x faster                                                           |
| fannkuch                   | 399 ms                                                          | 319 ms: 1.25x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 63.5 ms: 1.25x faster                                                           |
| deepcopy                   | 381 us                                                          | 305 us: 1.25x faster                                                            |
| sympy_expand               | 462 ms                                                          | 371 ms: 1.25x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 44.3 ms: 1.24x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.1 ms: 1.24x faster                                                           |
| scimark_fft                | 291 ms                                                          | 236 ms: 1.23x faster                                                            |
| nqueens                    | 111 ms                                                          | 90.8 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 481 ms: 1.23x faster                                                            |
| go                         | 147 ms                                                          | 120 ms: 1.22x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.71 us: 1.22x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 859 ms: 1.21x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 84.2 ms: 1.21x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 59.4 ms: 1.19x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.74 sec: 1.19x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 22.5 ms: 1.19x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.83 us: 1.16x faster                                                           |
| json                       | 4.78 ms                                                         | 4.13 ms: 1.16x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 44.9 ms: 1.15x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 991 us: 1.15x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 63.2 ms: 1.13x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.9 ms: 1.13x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.51 sec: 1.12x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 736 ms: 1.11x faster                                                            |
| 2to3                       | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.97 us: 1.09x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 83.5 ms: 1.09x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 111 ms: 1.03x faster                                                            |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| pickle_list                | 3.27 us                                                         | 3.19 us: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| pickle                     | 7.99 us                                                         | 8.01 us: 1.00x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 71.8 ms: 1.01x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.1 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 20.1 ms: 1.07x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.4 ms: 1.08x slower                                                           |
| python_startup             | 22.0 ms                                                         | 23.7 ms: 1.08x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.1 us: 1.10x slower                                                           |
| async_generators           | 260 ms                                                          | 291 ms: 1.12x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 733 us: 1.19x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.42 ms: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 228 ms: 2.02x slower                                                            |
| coverage                   | 58.0 ms                                                         | 504 ms: 8.68x slower                                                            |
| thrift                     | 801 us                                                          | 10.6 ms: 13.26x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.18x faster                                                                    |

Benchmark hidden because not significant (3): pickle_dict, json_loads, regex_dna
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown