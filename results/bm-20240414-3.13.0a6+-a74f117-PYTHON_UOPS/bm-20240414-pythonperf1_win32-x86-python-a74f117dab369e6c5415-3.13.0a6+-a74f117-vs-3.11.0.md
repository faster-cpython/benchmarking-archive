# Results vs. 3.11.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 245 ms: 1.15x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| html5lib       | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                           |
| tornado_http   | 118 ms                                                          | 97.7 ms: 1.21x faster                                                           |
| Geometric mean | (ref)                                                           | 1.21x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 226 ms: 1.52x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 274 ms: 1.49x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 82.9 ms: 1.52x faster                                                           |
| float          | 76.1 ms                                                         | 61.1 ms: 1.24x faster                                                           |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 125 ms: 1.18x faster                                                            |
| regex_dna      | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.64 ms: 1.48x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 211 us: 1.46x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 176 us: 1.32x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 42.8 ms: 1.29x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 61.0 ms: 1.17x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.79 us: 1.17x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 67.9 ms: 1.11x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.05x faster                                                            |
| pickle               | 7.99 us                                                         | 7.78 us: 1.03x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.29 us: 1.01x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.84 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 26.8 ms                                                         | 19.6 ms: 1.37x faster                                                           |
| genshi_xml     | 61.2 ms                                                         | 45.0 ms: 1.36x faster                                                           |
| mako           | 10.3 ms                                                         | 7.60 ms: 1.35x faster                                                           |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 94.5 us: 5.06x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.8 ms: 2.29x faster                                                           |
| logging_silent             | 119 ns                                                          | 60.5 ns: 1.97x faster                                                           |
| pylint                     | 418 ms                                                          | 219 ms: 1.91x faster                                                            |
| richards_super             | 58.7 ms                                                         | 34.4 ms: 1.70x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 14.5 ms: 1.64x faster                                                           |
| richards                   | 48.8 ms                                                         | 30.7 ms: 1.59x faster                                                           |
| chaos                      | 84.4 ms                                                         | 53.4 ms: 1.58x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 25.6 us: 1.57x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 965 us: 1.55x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.67 ms: 1.53x faster                                                           |
| raytrace                   | 327 ms                                                          | 215 ms: 1.53x faster                                                            |
| nbody                      | 126 ms                                                          | 82.9 ms: 1.52x faster                                                           |
| comprehensions             | 22.1 us                                                         | 14.5 us: 1.52x faster                                                           |
| async_tree_none            | 343 ms                                                          | 226 ms: 1.52x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 274 ms: 1.49x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.20 ms: 1.48x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.64 ms: 1.48x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 211 us: 1.46x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| scimark_sor                | 135 ms                                                          | 94.4 ms: 1.43x faster                                                           |
| nqueens                    | 111 ms                                                          | 78.2 ms: 1.43x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| deepcopy                   | 381 us                                                          | 269 us: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| spectral_norm              | 122 ms                                                          | 86.7 ms: 1.40x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.75 us: 1.40x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.41 us: 1.38x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 19.6 ms: 1.37x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.40 us: 1.36x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 45.0 ms: 1.36x faster                                                           |
| fannkuch                   | 399 ms                                                          | 295 ms: 1.35x faster                                                            |
| mako                       | 10.3 ms                                                         | 7.60 ms: 1.35x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 59.0 ms: 1.35x faster                                                           |
| pyflate                    | 471 ms                                                          | 355 ms: 1.33x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 113 ms: 1.32x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 53.8 ms: 1.32x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 176 us: 1.32x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.23 ms: 1.31x faster                                                           |
| scimark_fft                | 291 ms                                                          | 223 ms: 1.31x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.31 sec: 1.30x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 635 ms: 1.29x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 42.8 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 5.89 ms: 1.28x faster                                                           |
| sympy_str                  | 283 ms                                                          | 224 ms: 1.27x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.27x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 827 ms: 1.26x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 628 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.0 ms: 1.25x faster                                                           |
| float                      | 76.1 ms                                                         | 61.1 ms: 1.24x faster                                                           |
| go                         | 147 ms                                                          | 120 ms: 1.23x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                           |
| tornado_http               | 118 ms                                                          | 97.7 ms: 1.21x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 85.1 ms: 1.20x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 43.3 ms: 1.20x faster                                                           |
| sympy_expand               | 462 ms                                                          | 390 ms: 1.18x faster                                                            |
| regex_compile              | 148 ms                                                          | 125 ms: 1.18x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 61.0 ms: 1.17x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.79 us: 1.17x faster                                                           |
| json                       | 4.78 ms                                                         | 4.12 ms: 1.16x faster                                                           |
| 2to3                       | 282 ms                                                          | 245 ms: 1.15x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 79.2 ms: 1.15x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.00 ms: 1.14x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 67.9 ms: 1.11x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.05x faster                                                            |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                            |
| pickle                     | 7.99 us                                                         | 7.78 us: 1.03x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| pickle_dict                | 20.1 us                                                         | 19.9 us: 1.01x faster                                                           |
| pickle_list                | 3.27 us                                                         | 3.29 us: 1.01x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 71.6 ms: 1.01x slower                                                           |
| regex_dna                  | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.6 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.84 us: 1.07x slower                                                           |
| async_generators           | 260 ms                                                          | 301 ms: 1.16x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 735 us: 1.19x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.34 ms: 1.20x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 225 ms: 1.99x slower                                                            |
| coverage                   | 58.0 ms                                                         | 507 ms: 8.74x slower                                                            |
| thrift                     | 801 us                                                          | 11.3 ms: 14.08x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.20x faster                                                                    |

Benchmark hidden because not significant (2): python_startup_no_site, json_loads
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: unknown