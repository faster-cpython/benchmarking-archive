# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 264 ms: 1.07x faster                                                              |
| chameleon      | 8.08 ms                                                         | 6.24 ms: 1.29x faster                                                             |
| docutils       | 2.10 sec                                                        | 1.98 sec: 1.06x faster                                                            |
| html5lib       | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                                             |
| tornado_http   | 118 ms                                                          | 97.6 ms: 1.21x faster                                                             |
| Geometric mean | (ref)                                                           | 1.16x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 237 ms: 1.44x faster                                                              |
| async_tree_none_tg         | 301 ms                                                          | 212 ms: 1.42x faster                                                              |
| async_tree_memoization     | 408 ms                                                          | 289 ms: 1.41x faster                                                              |
| async_tree_memoization_tg  | 378 ms                                                          | 267 ms: 1.41x faster                                                              |
| async_tree_io              | 754 ms                                                          | 553 ms: 1.36x faster                                                              |
| async_tree_io_tg           | 746 ms                                                          | 552 ms: 1.35x faster                                                              |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 457 ms: 1.26x faster                                                              |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 480 ms: 1.23x faster                                                              |
| Geometric mean             | (ref)                                                           | 1.36x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                             |
| nbody          | 126 ms                                                          | 98.7 ms: 1.28x faster                                                             |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                              |
| Geometric mean | (ref)                                                           | 1.23x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 115 ms: 1.28x faster                                                              |
| regex_effbot   | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                             |
| regex_v8       | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                      |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.91 ms: 1.42x faster                                                             |
| pickle_pure_python   | 309 us                                                          | 224 us: 1.38x faster                                                              |
| tomli_loads          | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 178 us: 1.30x faster                                                              |
| xml_etree_process    | 55.0 ms                                                         | 46.0 ms: 1.20x faster                                                             |
| unpickle_list        | 3.28 us                                                         | 2.76 us: 1.19x faster                                                             |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.6 ms: 1.13x faster                                                             |
| xml_etree_generate   | 71.6 ms                                                         | 64.4 ms: 1.11x faster                                                             |
| xml_etree_parse      | 114 ms                                                          | 110 ms: 1.04x faster                                                              |
| json_loads           | 20.0 us                                                         | 19.8 us: 1.01x faster                                                             |
| pickle               | 7.99 us                                                         | 8.24 us: 1.03x slower                                                             |
| unpickle             | 9.23 us                                                         | 9.89 us: 1.07x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                      |

Benchmark hidden because not significant (2): pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                             |
| python_startup_no_site | 18.8 ms                                                         | 22.0 ms: 1.17x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.18 ms: 1.43x faster                                                             |
| genshi_xml      | 61.2 ms                                                         | 49.9 ms: 1.23x faster                                                             |
| genshi_text     | 26.8 ms                                                         | 23.3 ms: 1.15x faster                                                             |
| django_template | 37.4 ms                                                         | 35.3 ms: 1.06x faster                                                             |
| Geometric mean  | (ref)                                                           | 1.21x faster                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 101 us: 4.73x faster                                                              |
| generators                 | 52.2 ms                                                         | 22.4 ms: 2.33x faster                                                             |
| logging_silent             | 119 ns                                                          | 59.9 ns: 1.99x faster                                                             |
| pylint                     | 418 ms                                                          | 228 ms: 1.83x faster                                                              |
| spectral_norm              | 122 ms                                                          | 70.5 ms: 1.72x faster                                                             |
| coroutines                 | 23.7 ms                                                         | 14.5 ms: 1.63x faster                                                             |
| deltablue                  | 4.10 ms                                                         | 2.61 ms: 1.57x faster                                                             |
| deepcopy_memo              | 40.0 us                                                         | 26.6 us: 1.50x faster                                                             |
| sqlglot_parse              | 1.49 ms                                                         | 1.00 ms: 1.48x faster                                                             |
| richards_super             | 58.7 ms                                                         | 40.4 ms: 1.45x faster                                                             |
| async_tree_none            | 343 ms                                                          | 237 ms: 1.44x faster                                                              |
| unpack_sequence            | 65.2 ns                                                         | 45.5 ns: 1.43x faster                                                             |
| mako                       | 10.3 ms                                                         | 7.18 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 301 ms                                                          | 212 ms: 1.42x faster                                                              |
| json_dumps                 | 9.80 ms                                                         | 6.91 ms: 1.42x faster                                                             |
| float                      | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                             |
| sqlglot_transpile          | 1.78 ms                                                         | 1.26 ms: 1.42x faster                                                             |
| async_tree_memoization     | 408 ms                                                          | 289 ms: 1.41x faster                                                              |
| async_tree_memoization_tg  | 378 ms                                                          | 267 ms: 1.41x faster                                                              |
| scimark_sor                | 135 ms                                                          | 97.9 ms: 1.38x faster                                                             |
| pickle_pure_python         | 309 us                                                          | 224 us: 1.38x faster                                                              |
| async_tree_io              | 754 ms                                                          | 553 ms: 1.36x faster                                                              |
| comprehensions             | 22.1 us                                                         | 16.3 us: 1.36x faster                                                             |
| richards                   | 48.8 ms                                                         | 36.0 ms: 1.36x faster                                                             |
| async_tree_io_tg           | 746 ms                                                          | 552 ms: 1.35x faster                                                              |
| chaos                      | 84.4 ms                                                         | 62.5 ms: 1.35x faster                                                             |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.14 ms: 1.35x faster                                                             |
| sympy_sum                  | 149 ms                                                          | 112 ms: 1.33x faster                                                              |
| tomli_loads                | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 178 us: 1.30x faster                                                              |
| chameleon                  | 8.08 ms                                                         | 6.24 ms: 1.29x faster                                                             |
| asyncio_tcp                | 787 ms                                                          | 608 ms: 1.29x faster                                                              |
| deepcopy_reduce            | 3.32 us                                                         | 2.57 us: 1.29x faster                                                             |
| regex_compile              | 148 ms                                                          | 115 ms: 1.28x faster                                                              |
| sympy_str                  | 283 ms                                                          | 222 ms: 1.28x faster                                                              |
| nbody                      | 126 ms                                                          | 98.7 ms: 1.28x faster                                                             |
| crypto_pyaes               | 79.4 ms                                                         | 62.7 ms: 1.27x faster                                                             |
| pyflate                    | 471 ms                                                          | 372 ms: 1.27x faster                                                              |
| deepcopy                   | 381 us                                                          | 302 us: 1.26x faster                                                              |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 457 ms: 1.26x faster                                                              |
| logging_simple             | 10.8 us                                                         | 8.60 us: 1.26x faster                                                             |
| logging_format             | 11.5 us                                                         | 9.18 us: 1.25x faster                                                             |
| raytrace                   | 327 ms                                                          | 264 ms: 1.24x faster                                                              |
| fannkuch                   | 399 ms                                                          | 324 ms: 1.23x faster                                                              |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 480 ms: 1.23x faster                                                              |
| genshi_xml                 | 61.2 ms                                                         | 49.9 ms: 1.23x faster                                                             |
| tornado_http               | 118 ms                                                          | 97.6 ms: 1.21x faster                                                             |
| scimark_fft                | 291 ms                                                          | 240 ms: 1.21x faster                                                              |
| pycparser                  | 1.04 sec                                                        | 869 ms: 1.20x faster                                                              |
| sympy_expand               | 462 ms                                                          | 386 ms: 1.20x faster                                                              |
| xml_etree_process          | 55.0 ms                                                         | 46.0 ms: 1.20x faster                                                             |
| unpickle_list              | 3.28 us                                                         | 2.76 us: 1.19x faster                                                             |
| html5lib                   | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                                             |
| sympy_integrate            | 19.9 ms                                                         | 16.9 ms: 1.18x faster                                                             |
| mdp                        | 2.07 sec                                                        | 1.76 sec: 1.17x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 88.2 ms: 1.16x faster                                                             |
| nqueens                    | 111 ms                                                          | 96.7 ms: 1.15x faster                                                             |
| json                       | 4.78 ms                                                         | 4.16 ms: 1.15x faster                                                             |
| genshi_text                | 26.8 ms                                                         | 23.3 ms: 1.15x faster                                                             |
| scimark_monte_carlo        | 70.8 ms                                                         | 61.7 ms: 1.15x faster                                                             |
| pprint_pformat             | 1.70 sec                                                        | 1.48 sec: 1.14x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.6 ms: 1.13x faster                                                             |
| go                         | 147 ms                                                          | 130 ms: 1.13x faster                                                              |
| hexiom                     | 7.51 ms                                                         | 6.65 ms: 1.13x faster                                                             |
| pprint_safe_repr           | 819 ms                                                          | 732 ms: 1.12x faster                                                              |
| xml_etree_generate         | 71.6 ms                                                         | 64.4 ms: 1.11x faster                                                             |
| bench_thread_pool          | 1.14 ms                                                         | 1.03 ms: 1.11x faster                                                             |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                             |
| sqlglot_optimize           | 51.8 ms                                                         | 47.5 ms: 1.09x faster                                                             |
| 2to3                       | 282 ms                                                          | 264 ms: 1.07x faster                                                              |
| django_template            | 37.4 ms                                                         | 35.3 ms: 1.06x faster                                                             |
| docutils                   | 2.10 sec                                                        | 1.98 sec: 1.06x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 87.2 ms: 1.04x faster                                                             |
| xml_etree_parse            | 114 ms                                                          | 110 ms: 1.04x faster                                                              |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                              |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                            |
| json_loads                 | 20.0 us                                                         | 19.8 us: 1.01x faster                                                             |
| bench_mp_pool              | 70.9 ms                                                         | 72.7 ms: 1.03x slower                                                             |
| pickle                     | 7.99 us                                                         | 8.24 us: 1.03x slower                                                             |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                             |
| regex_effbot               | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                             |
| unpickle                   | 9.23 us                                                         | 9.89 us: 1.07x slower                                                             |
| regex_v8                   | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                             |
| pathlib                    | 79.9 ms                                                         | 86.4 ms: 1.08x slower                                                             |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                             |
| async_generators           | 260 ms                                                          | 294 ms: 1.13x slower                                                              |
| python_startup_no_site     | 18.8 ms                                                         | 22.0 ms: 1.17x slower                                                             |
| create_gc_cycles           | 618 us                                                          | 737 us: 1.19x slower                                                              |
| telco                      | 5.29 ms                                                         | 6.32 ms: 1.19x slower                                                             |
| sqlglot_normalize          | 113 ms                                                          | 247 ms: 2.18x slower                                                              |
| coverage                   | 58.0 ms                                                         | 490 ms: 8.45x slower                                                              |
| thrift                     | 801 us                                                          | 11.0 ms: 13.71x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.15x faster                                                                      |

Benchmark hidden because not significant (3): pickle_dict, pickle_list, regex_dna
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: unknown