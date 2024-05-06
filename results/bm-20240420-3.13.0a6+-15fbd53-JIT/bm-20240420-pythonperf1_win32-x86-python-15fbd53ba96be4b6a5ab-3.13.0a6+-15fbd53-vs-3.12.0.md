# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 253 ms: 1.11x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.02 ms: 1.29x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| tornado_http   | 105 ms                                                          | 95.0 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                           | 1.13x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 266 ms: 1.32x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 215 ms: 1.29x faster                                                            |
| async_tree_io              | 693 ms                                                          | 540 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 289 ms: 1.26x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 542 ms: 1.25x faster                                                            |
| async_tree_none            | 298 ms                                                          | 240 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 456 ms: 1.20x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 484 ms: 1.16x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 52.2 ms: 1.47x faster                                                           |
| nbody          | 127 ms                                                          | 92.0 ms: 1.38x faster                                                           |
| pidigits       | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 110 ms: 1.18x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| regex_dna      | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 222 us: 1.29x faster                                                            |
| unpickle_pure_python | 210 us                                                          | 164 us: 1.28x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.73 sec: 1.27x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.7 ms: 1.22x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 66.4 ms: 1.17x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 62.6 ms: 1.15x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.19 us: 1.06x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 109 ms: 1.04x faster                                                            |
| json_loads           | 20.4 us                                                         | 19.8 us: 1.03x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.87 us: 1.03x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| pickle               | 7.79 us                                                         | 7.96 us: 1.02x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 20.7 ms: 1.09x slower                                                           |
| python_startup         | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.88 ms: 1.45x faster                                                           |
| django_template | 36.9 ms                                                         | 33.3 ms: 1.11x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.27x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.5 ms: 1.71x faster                                                           |
| logging_silent             | 101 ns                                                          | 59.9 ns: 1.69x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 24.9 us: 1.54x faster                                                           |
| spectral_norm              | 104 ms                                                          | 70.6 ms: 1.47x faster                                                           |
| float                      | 76.7 ms                                                         | 52.2 ms: 1.47x faster                                                           |
| mako                       | 9.96 ms                                                         | 6.88 ms: 1.45x faster                                                           |
| nbody                      | 127 ms                                                          | 92.0 ms: 1.38x faster                                                           |
| raytrace                   | 308 ms                                                          | 223 ms: 1.38x faster                                                            |
| scimark_sor                | 130 ms                                                          | 97.3 ms: 1.33x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.6 ms: 1.33x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 95.5 us: 1.32x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.71 ms: 1.32x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 266 ms: 1.32x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 215 ms: 1.29x faster                                                            |
| pickle_pure_python         | 286 us                                                          | 222 us: 1.29x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 6.02 ms: 1.29x faster                                                           |
| async_tree_io              | 693 ms                                                          | 540 ms: 1.28x faster                                                            |
| unpickle_pure_python       | 210 us                                                          | 164 us: 1.28x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.73 sec: 1.27x faster                                                          |
| comprehensions             | 19.2 us                                                         | 15.2 us: 1.27x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 289 ms: 1.26x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 994 us: 1.26x faster                                                            |
| richards                   | 41.3 ms                                                         | 33.0 ms: 1.25x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 542 ms: 1.25x faster                                                            |
| async_tree_none            | 298 ms                                                          | 240 ms: 1.24x faster                                                            |
| richards_super             | 46.5 ms                                                         | 37.5 ms: 1.24x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.25 ms: 1.23x faster                                                           |
| deepcopy                   | 360 us                                                          | 295 us: 1.22x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 43.7 ms: 1.22x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.65 us: 1.22x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.17 ms: 1.22x faster                                                           |
| logging_simple             | 9.75 us                                                         | 8.09 us: 1.21x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.66 us: 1.20x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 456 ms: 1.20x faster                                                            |
| chaos                      | 69.4 ms                                                         | 58.0 ms: 1.20x faster                                                           |
| regex_compile              | 129 ms                                                          | 110 ms: 1.18x faster                                                            |
| pycparser                  | 978 ms                                                          | 835 ms: 1.17x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 66.4 ms: 1.17x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 484 ms: 1.16x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 5.86 ms: 1.16x faster                                                           |
| pyflate                    | 424 ms                                                          | 366 ms: 1.16x faster                                                            |
| go                         | 137 ms                                                          | 119 ms: 1.16x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 62.6 ms: 1.15x faster                                                           |
| scimark_fft                | 271 ms                                                          | 241 ms: 1.12x faster                                                            |
| fannkuch                   | 354 ms                                                          | 317 ms: 1.11x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 110 ms: 1.11x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.72 sec: 1.11x faster                                                          |
| 2to3                       | 280 ms                                                          | 253 ms: 1.11x faster                                                            |
| django_template            | 36.9 ms                                                         | 33.3 ms: 1.11x faster                                                           |
| tornado_http               | 105 ms                                                          | 95.0 ms: 1.11x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 60.4 ms: 1.10x faster                                                           |
| sympy_str                  | 240 ms                                                          | 218 ms: 1.10x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 63.2 ms: 1.09x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 83.9 ms: 1.09x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 1.01 ms: 1.09x faster                                                           |
| async_generators           | 313 ms                                                          | 289 ms: 1.08x faster                                                            |
| sympy_integrate            | 17.5 ms                                                         | 16.3 ms: 1.08x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 80.7 ms: 1.08x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.93 us: 1.07x faster                                                           |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 45.7 ms: 1.06x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 88.0 ms: 1.06x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.19 us: 1.06x faster                                                           |
| sympy_expand               | 398 ms                                                          | 377 ms: 1.06x faster                                                            |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| regex_dna                  | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| xml_etree_parse            | 113 ms                                                          | 109 ms: 1.04x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| nqueens                    | 93.7 ms                                                         | 90.7 ms: 1.03x faster                                                           |
| json_loads                 | 20.4 us                                                         | 19.8 us: 1.03x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.87 us: 1.03x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 74.2 ms: 1.02x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.50 sec: 1.00x slower                                                          |
| pickle_dict                | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| pprint_safe_repr           | 721 ms                                                          | 735 ms: 1.02x slower                                                            |
| pickle                     | 7.79 us                                                         | 7.96 us: 1.02x slower                                                           |
| unpickle                   | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 20.7 ms: 1.09x slower                                                           |
| python_startup             | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 727 us: 1.11x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.36 ms: 1.15x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 234 ms: 2.34x slower                                                            |
| coverage                   | 48.4 ms                                                         | 499 ms: 10.29x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.11x faster                                                                    |

Benchmark hidden because not significant (2): asyncio_tcp, json
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: unknown