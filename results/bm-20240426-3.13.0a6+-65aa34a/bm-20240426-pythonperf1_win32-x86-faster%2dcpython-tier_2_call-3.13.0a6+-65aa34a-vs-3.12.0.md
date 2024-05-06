# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-x86
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 235 ms: 1.19x faster                                                             |
| chameleon      | 7.75 ms                                                         | 5.69 ms: 1.36x faster                                                            |
| docutils       | 1.98 sec                                                        | 1.80 sec: 1.10x faster                                                           |
| tornado_http   | 105 ms                                                          | 102 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                           | 1.16x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 255 ms: 1.37x faster                                                             |
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                             |
| async_tree_memoization     | 364 ms                                                          | 275 ms: 1.32x faster                                                             |
| async_tree_io              | 693 ms                                                          | 529 ms: 1.31x faster                                                             |
| async_tree_none            | 298 ms                                                          | 228 ms: 1.31x faster                                                             |
| async_tree_io_tg           | 677 ms                                                          | 539 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 458 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 480 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 80.3 ms: 1.58x faster                                                            |
| float          | 76.7 ms                                                         | 53.0 ms: 1.45x faster                                                            |
| pidigits       | 199 ms                                                          | 200 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                           | 1.32x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 96.3 ms: 1.34x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.87 ms: 1.09x faster                                                            |
| regex_dna      | 127 ms                                                          | 121 ms: 1.05x faster                                                             |
| regex_v8       | 15.0 ms                                                         | 15.8 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 140 us: 1.50x faster                                                             |
| tomli_loads          | 2.20 sec                                                        | 1.58 sec: 1.39x faster                                                           |
| pickle_pure_python   | 286 us                                                          | 209 us: 1.37x faster                                                             |
| xml_etree_process    | 53.2 ms                                                         | 41.8 ms: 1.27x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 58.8 ms: 1.23x faster                                                            |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.2 ms: 1.19x faster                                                            |
| json_dumps           | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                            |
| xml_etree_parse      | 113 ms                                                          | 106 ms: 1.07x faster                                                             |
| pickle_list          | 3.37 us                                                         | 3.26 us: 1.04x faster                                                            |
| json_loads           | 20.4 us                                                         | 19.9 us: 1.02x faster                                                            |
| unpickle_list        | 2.95 us                                                         | 2.90 us: 1.02x faster                                                            |
| pickle               | 7.79 us                                                         | 7.90 us: 1.01x slower                                                            |
| pickle_dict          | 19.9 us                                                         | 20.3 us: 1.02x slower                                                            |
| unpickle             | 9.71 us                                                         | 9.97 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.4 ms: 1.03x faster                                                            |
| python_startup         | 22.4 ms                                                         | 22.6 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.94 ms: 1.43x faster                                                            |
| django_template | 36.9 ms                                                         | 29.8 ms: 1.24x faster                                                            |
| Geometric mean  | (ref)                                                           | 1.33x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 56.1 ns: 1.80x faster                                                            |
| generators                 | 38.5 ms                                                         | 22.6 ms: 1.70x faster                                                            |
| raytrace                   | 308 ms                                                          | 182 ms: 1.70x faster                                                             |
| deltablue                  | 3.58 ms                                                         | 2.16 ms: 1.66x faster                                                            |
| deepcopy_memo              | 38.4 us                                                         | 23.3 us: 1.65x faster                                                            |
| scimark_sor                | 130 ms                                                          | 79.1 ms: 1.64x faster                                                            |
| comprehensions             | 19.2 us                                                         | 11.7 us: 1.64x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 4.24 ms: 1.61x faster                                                            |
| nbody                      | 127 ms                                                          | 80.3 ms: 1.58x faster                                                            |
| scimark_lu                 | 93.2 ms                                                         | 60.7 ms: 1.53x faster                                                            |
| spectral_norm              | 104 ms                                                          | 67.9 ms: 1.53x faster                                                            |
| unpickle_pure_python       | 210 us                                                          | 140 us: 1.50x faster                                                             |
| chaos                      | 69.4 ms                                                         | 47.5 ms: 1.46x faster                                                            |
| float                      | 76.7 ms                                                         | 53.0 ms: 1.45x faster                                                            |
| mako                       | 9.96 ms                                                         | 6.94 ms: 1.43x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 46.8 ms: 1.42x faster                                                            |
| richards_super             | 46.5 ms                                                         | 33.0 ms: 1.41x faster                                                            |
| richards                   | 41.3 ms                                                         | 29.5 ms: 1.40x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.58 sec: 1.39x faster                                                           |
| go                         | 137 ms                                                          | 99.6 ms: 1.38x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 907 us: 1.38x faster                                                             |
| nqueens                    | 93.7 ms                                                         | 68.2 ms: 1.37x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 255 ms: 1.37x faster                                                             |
| pickle_pure_python         | 286 us                                                          | 209 us: 1.37x faster                                                             |
| logging_simple             | 9.75 us                                                         | 7.12 us: 1.37x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 5.69 ms: 1.36x faster                                                            |
| pyflate                    | 424 ms                                                          | 313 ms: 1.35x faster                                                             |
| sqlglot_transpile          | 1.53 ms                                                         | 1.13 ms: 1.35x faster                                                            |
| regex_compile              | 129 ms                                                          | 96.3 ms: 1.34x faster                                                            |
| logging_format             | 10.4 us                                                         | 7.80 us: 1.33x faster                                                            |
| coroutines                 | 20.9 ms                                                         | 15.7 ms: 1.33x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                             |
| async_tree_memoization     | 364 ms                                                          | 275 ms: 1.32x faster                                                             |
| deepcopy                   | 360 us                                                          | 272 us: 1.32x faster                                                             |
| async_tree_io              | 693 ms                                                          | 529 ms: 1.31x faster                                                             |
| async_tree_none            | 298 ms                                                          | 228 ms: 1.31x faster                                                             |
| scimark_fft                | 271 ms                                                          | 208 ms: 1.30x faster                                                             |
| fannkuch                   | 354 ms                                                          | 273 ms: 1.30x faster                                                             |
| pprint_pformat             | 1.50 sec                                                        | 1.17 sec: 1.28x faster                                                           |
| pycparser                  | 978 ms                                                          | 766 ms: 1.28x faster                                                             |
| xml_etree_process          | 53.2 ms                                                         | 41.8 ms: 1.27x faster                                                            |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.06 ms: 1.26x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 54.9 ms: 1.26x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 539 ms: 1.26x faster                                                             |
| deepcopy_reduce            | 3.23 us                                                         | 2.58 us: 1.25x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 38.7 ms: 1.25x faster                                                            |
| pprint_safe_repr           | 721 ms                                                          | 576 ms: 1.25x faster                                                             |
| django_template            | 36.9 ms                                                         | 29.8 ms: 1.24x faster                                                            |
| sympy_integrate            | 17.5 ms                                                         | 14.2 ms: 1.23x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 58.8 ms: 1.23x faster                                                            |
| sympy_str                  | 240 ms                                                          | 199 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 458 ms: 1.19x faster                                                             |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.2 ms: 1.19x faster                                                            |
| 2to3                       | 280 ms                                                          | 235 ms: 1.19x faster                                                             |
| mdp                        | 1.91 sec                                                        | 1.61 sec: 1.19x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 104 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 480 ms: 1.18x faster                                                             |
| sympy_expand               | 398 ms                                                          | 347 ms: 1.15x faster                                                             |
| meteor_contest             | 86.9 ms                                                         | 76.9 ms: 1.13x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 992 us: 1.11x faster                                                             |
| docutils                   | 1.98 sec                                                        | 1.80 sec: 1.10x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.87 ms: 1.09x faster                                                            |
| async_generators           | 313 ms                                                          | 289 ms: 1.08x faster                                                             |
| bench_mp_pool              | 75.4 ms                                                         | 69.8 ms: 1.08x faster                                                            |
| sqlite_synth               | 2.07 us                                                         | 1.93 us: 1.07x faster                                                            |
| xml_etree_parse            | 113 ms                                                          | 106 ms: 1.07x faster                                                             |
| regex_dna                  | 127 ms                                                          | 121 ms: 1.05x faster                                                             |
| pickle_list                | 3.37 us                                                         | 3.26 us: 1.04x faster                                                            |
| python_startup_no_site     | 19.1 ms                                                         | 18.4 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 17.2 sec: 1.03x faster                                                           |
| tornado_http               | 105 ms                                                          | 102 ms: 1.02x faster                                                             |
| json_loads                 | 20.4 us                                                         | 19.9 us: 1.02x faster                                                            |
| unpickle_list              | 2.95 us                                                         | 2.90 us: 1.02x faster                                                            |
| pathlib                    | 91.4 ms                                                         | 90.2 ms: 1.01x faster                                                            |
| pidigits                   | 199 ms                                                          | 200 ms: 1.00x slower                                                             |
| gc_traversal               | 1.44 ms                                                         | 1.45 ms: 1.01x slower                                                            |
| python_startup             | 22.4 ms                                                         | 22.6 ms: 1.01x slower                                                            |
| pickle                     | 7.79 us                                                         | 7.90 us: 1.01x slower                                                            |
| pickle_dict                | 19.9 us                                                         | 20.3 us: 1.02x slower                                                            |
| unpickle                   | 9.71 us                                                         | 9.97 us: 1.03x slower                                                            |
| typing_runtime_protocols   | 126 us                                                          | 131 us: 1.03x slower                                                             |
| regex_v8                   | 15.0 ms                                                         | 15.8 ms: 1.05x slower                                                            |
| telco                      | 5.51 ms                                                         | 5.87 ms: 1.07x slower                                                            |
| create_gc_cycles           | 652 us                                                          | 740 us: 1.14x slower                                                             |
| asyncio_tcp                | 662 ms                                                          | 878 ms: 1.33x slower                                                             |
| sqlglot_normalize          | 100 ms                                                          | 200 ms: 1.99x slower                                                             |
| coverage                   | 48.4 ms                                                         | 498 ms: 10.29x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.19x faster                                                                     |

Benchmark hidden because not significant (1): json
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown