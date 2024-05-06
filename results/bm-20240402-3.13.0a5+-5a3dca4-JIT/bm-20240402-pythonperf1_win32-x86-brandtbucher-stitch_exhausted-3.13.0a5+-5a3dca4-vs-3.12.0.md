# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 264 ms: 1.06x faster                                                              |
| chameleon      | 7.75 ms                                                         | 6.24 ms: 1.24x faster                                                             |
| tornado_http   | 105 ms                                                          | 97.6 ms: 1.08x faster                                                             |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                      |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 212 ms: 1.31x faster                                                              |
| async_tree_memoization_tg  | 350 ms                                                          | 267 ms: 1.31x faster                                                              |
| async_tree_memoization     | 364 ms                                                          | 289 ms: 1.26x faster                                                              |
| async_tree_none            | 298 ms                                                          | 237 ms: 1.25x faster                                                              |
| async_tree_io              | 693 ms                                                          | 553 ms: 1.25x faster                                                              |
| async_tree_io_tg           | 677 ms                                                          | 552 ms: 1.23x faster                                                              |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 457 ms: 1.19x faster                                                              |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 480 ms: 1.17x faster                                                              |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                             |
| nbody          | 127 ms                                                          | 98.7 ms: 1.29x faster                                                             |
| pidigits       | 199 ms                                                          | 198 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                           | 1.23x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 115 ms: 1.12x faster                                                              |
| regex_effbot   | 2.04 ms                                                         | 1.89 ms: 1.08x faster                                                             |
| regex_dna      | 127 ms                                                          | 122 ms: 1.04x faster                                                              |
| regex_v8       | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 224 us: 1.28x faster                                                              |
| tomli_loads          | 2.20 sec                                                        | 1.75 sec: 1.26x faster                                                            |
| unpickle_pure_python | 210 us                                                          | 178 us: 1.18x faster                                                              |
| xml_etree_iterparse  | 77.6 ms                                                         | 66.6 ms: 1.17x faster                                                             |
| xml_etree_process    | 53.2 ms                                                         | 46.0 ms: 1.16x faster                                                             |
| xml_etree_generate   | 72.1 ms                                                         | 64.4 ms: 1.12x faster                                                             |
| json_dumps           | 7.40 ms                                                         | 6.91 ms: 1.07x faster                                                             |
| unpickle_list        | 2.95 us                                                         | 2.76 us: 1.07x faster                                                             |
| pickle_list          | 3.37 us                                                         | 3.26 us: 1.03x faster                                                             |
| xml_etree_parse      | 113 ms                                                          | 110 ms: 1.03x faster                                                              |
| json_loads           | 20.4 us                                                         | 19.8 us: 1.03x faster                                                             |
| pickle_dict          | 19.9 us                                                         | 20.1 us: 1.01x slower                                                             |
| unpickle             | 9.71 us                                                         | 9.89 us: 1.02x slower                                                             |
| pickle               | 7.79 us                                                         | 8.24 us: 1.06x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                             |
| python_startup_no_site | 19.1 ms                                                         | 22.0 ms: 1.15x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.18 ms: 1.39x faster                                                             |
| django_template | 36.9 ms                                                         | 35.3 ms: 1.05x faster                                                             |
| Geometric mean  | (ref)                                                           | 1.21x faster                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.4 ms: 1.72x faster                                                             |
| logging_silent             | 101 ns                                                          | 59.9 ns: 1.69x faster                                                             |
| spectral_norm              | 104 ms                                                          | 70.5 ms: 1.47x faster                                                             |
| deepcopy_memo              | 38.4 us                                                         | 26.6 us: 1.44x faster                                                             |
| coroutines                 | 20.9 ms                                                         | 14.5 ms: 1.44x faster                                                             |
| float                      | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                             |
| mako                       | 9.96 ms                                                         | 7.18 ms: 1.39x faster                                                             |
| unpack_sequence            | 62.5 ns                                                         | 45.5 ns: 1.37x faster                                                             |
| deltablue                  | 3.58 ms                                                         | 2.61 ms: 1.37x faster                                                             |
| scimark_sor                | 130 ms                                                          | 97.9 ms: 1.33x faster                                                             |
| async_tree_none_tg         | 278 ms                                                          | 212 ms: 1.31x faster                                                              |
| async_tree_memoization_tg  | 350 ms                                                          | 267 ms: 1.31x faster                                                              |
| nbody                      | 127 ms                                                          | 98.7 ms: 1.29x faster                                                             |
| pickle_pure_python         | 286 us                                                          | 224 us: 1.28x faster                                                              |
| async_tree_memoization     | 364 ms                                                          | 289 ms: 1.26x faster                                                              |
| tomli_loads                | 2.20 sec                                                        | 1.75 sec: 1.26x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.57 us: 1.26x faster                                                             |
| async_tree_none            | 298 ms                                                          | 237 ms: 1.25x faster                                                              |
| async_tree_io              | 693 ms                                                          | 553 ms: 1.25x faster                                                              |
| typing_runtime_protocols   | 126 us                                                          | 101 us: 1.25x faster                                                              |
| sqlglot_parse              | 1.25 ms                                                         | 1.00 ms: 1.24x faster                                                             |
| chameleon                  | 7.75 ms                                                         | 6.24 ms: 1.24x faster                                                             |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.14 ms: 1.23x faster                                                             |
| async_tree_io_tg           | 677 ms                                                          | 552 ms: 1.23x faster                                                              |
| sqlglot_transpile          | 1.53 ms                                                         | 1.26 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 457 ms: 1.19x faster                                                              |
| deepcopy                   | 360 us                                                          | 302 us: 1.19x faster                                                              |
| comprehensions             | 19.2 us                                                         | 16.3 us: 1.18x faster                                                             |
| unpickle_pure_python       | 210 us                                                          | 178 us: 1.18x faster                                                              |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 480 ms: 1.17x faster                                                              |
| raytrace                   | 308 ms                                                          | 264 ms: 1.17x faster                                                              |
| xml_etree_iterparse        | 77.6 ms                                                         | 66.6 ms: 1.17x faster                                                             |
| xml_etree_process          | 53.2 ms                                                         | 46.0 ms: 1.16x faster                                                             |
| richards_super             | 46.5 ms                                                         | 40.4 ms: 1.15x faster                                                             |
| richards                   | 41.3 ms                                                         | 36.0 ms: 1.15x faster                                                             |
| pyflate                    | 424 ms                                                          | 372 ms: 1.14x faster                                                              |
| logging_simple             | 9.75 us                                                         | 8.60 us: 1.13x faster                                                             |
| logging_format             | 10.4 us                                                         | 9.18 us: 1.13x faster                                                             |
| scimark_fft                | 271 ms                                                          | 240 ms: 1.13x faster                                                              |
| pycparser                  | 978 ms                                                          | 869 ms: 1.13x faster                                                              |
| regex_compile              | 129 ms                                                          | 115 ms: 1.12x faster                                                              |
| xml_etree_generate         | 72.1 ms                                                         | 64.4 ms: 1.12x faster                                                             |
| chaos                      | 69.4 ms                                                         | 62.5 ms: 1.11x faster                                                             |
| crypto_pyaes               | 69.2 ms                                                         | 62.7 ms: 1.10x faster                                                             |
| sympy_sum                  | 123 ms                                                          | 112 ms: 1.10x faster                                                              |
| fannkuch                   | 354 ms                                                          | 324 ms: 1.09x faster                                                              |
| asyncio_tcp                | 662 ms                                                          | 608 ms: 1.09x faster                                                              |
| mdp                        | 1.91 sec                                                        | 1.76 sec: 1.08x faster                                                            |
| sympy_str                  | 240 ms                                                          | 222 ms: 1.08x faster                                                              |
| scimark_monte_carlo        | 66.4 ms                                                         | 61.7 ms: 1.08x faster                                                             |
| tornado_http               | 105 ms                                                          | 97.6 ms: 1.08x faster                                                             |
| regex_effbot               | 2.04 ms                                                         | 1.89 ms: 1.08x faster                                                             |
| bench_thread_pool          | 1.10 ms                                                         | 1.03 ms: 1.07x faster                                                             |
| json_dumps                 | 7.40 ms                                                         | 6.91 ms: 1.07x faster                                                             |
| unpickle_list              | 2.95 us                                                         | 2.76 us: 1.07x faster                                                             |
| sqlite_synth               | 2.07 us                                                         | 1.94 us: 1.07x faster                                                             |
| async_generators           | 313 ms                                                          | 294 ms: 1.07x faster                                                              |
| 2to3                       | 280 ms                                                          | 264 ms: 1.06x faster                                                              |
| go                         | 137 ms                                                          | 130 ms: 1.06x faster                                                              |
| pathlib                    | 91.4 ms                                                         | 86.4 ms: 1.06x faster                                                             |
| scimark_lu                 | 93.2 ms                                                         | 88.2 ms: 1.06x faster                                                             |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                            |
| django_template            | 36.9 ms                                                         | 35.3 ms: 1.05x faster                                                             |
| regex_dna                  | 127 ms                                                          | 122 ms: 1.04x faster                                                              |
| sympy_integrate            | 17.5 ms                                                         | 16.9 ms: 1.04x faster                                                             |
| bench_mp_pool              | 75.4 ms                                                         | 72.7 ms: 1.04x faster                                                             |
| pickle_list                | 3.37 us                                                         | 3.26 us: 1.03x faster                                                             |
| sympy_expand               | 398 ms                                                          | 386 ms: 1.03x faster                                                              |
| xml_etree_parse            | 113 ms                                                          | 110 ms: 1.03x faster                                                              |
| hexiom                     | 6.82 ms                                                         | 6.65 ms: 1.03x faster                                                             |
| json_loads                 | 20.4 us                                                         | 19.8 us: 1.03x faster                                                             |
| sqlglot_optimize           | 48.5 ms                                                         | 47.5 ms: 1.02x faster                                                             |
| pprint_pformat             | 1.50 sec                                                        | 1.48 sec: 1.01x faster                                                            |
| gc_traversal               | 1.44 ms                                                         | 1.43 ms: 1.01x faster                                                             |
| pidigits                   | 199 ms                                                          | 198 ms: 1.01x faster                                                              |
| meteor_contest             | 86.9 ms                                                         | 87.2 ms: 1.00x slower                                                             |
| pickle_dict                | 19.9 us                                                         | 20.1 us: 1.01x slower                                                             |
| pprint_safe_repr           | 721 ms                                                          | 732 ms: 1.02x slower                                                              |
| unpickle                   | 9.71 us                                                         | 9.89 us: 1.02x slower                                                             |
| nqueens                    | 93.7 ms                                                         | 96.7 ms: 1.03x slower                                                             |
| pickle                     | 7.79 us                                                         | 8.24 us: 1.06x slower                                                             |
| regex_v8                   | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                             |
| python_startup             | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                             |
| create_gc_cycles           | 652 us                                                          | 737 us: 1.13x slower                                                              |
| telco                      | 5.51 ms                                                         | 6.32 ms: 1.15x slower                                                             |
| python_startup_no_site     | 19.1 ms                                                         | 22.0 ms: 1.15x slower                                                             |
| sqlglot_normalize          | 100 ms                                                          | 247 ms: 2.46x slower                                                              |
| coverage                   | 48.4 ms                                                         | 490 ms: 10.12x slower                                                             |
| Geometric mean             | (ref)                                                           | 1.09x faster                                                                      |

Benchmark hidden because not significant (2): docutils, json
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown