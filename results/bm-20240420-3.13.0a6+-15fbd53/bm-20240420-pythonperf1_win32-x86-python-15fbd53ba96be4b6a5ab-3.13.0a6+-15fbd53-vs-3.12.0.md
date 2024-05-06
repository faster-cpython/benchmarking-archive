# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 229 ms: 1.22x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.69 ms: 1.36x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.79 sec: 1.11x faster                                                          |
| tornado_http   | 105 ms                                                          | 92.8 ms: 1.13x faster                                                           |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 251 ms: 1.40x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 270 ms: 1.35x faster                                                            |
| async_tree_io              | 693 ms                                                          | 523 ms: 1.33x faster                                                            |
| async_tree_none            | 298 ms                                                          | 225 ms: 1.32x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 523 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 470 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 488 ms: 1.16x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.29x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 80.7 ms: 1.57x faster                                                           |
| float          | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                           |
| pidigits       | 199 ms                                                          | 196 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.31x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 94.7 ms: 1.36x faster                                                           |
| regex_effbot   | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                           |
| regex_dna      | 127 ms                                                          | 124 ms: 1.03x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 15.8 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 137 us: 1.53x faster                                                            |
| pickle_pure_python   | 286 us                                                          | 199 us: 1.44x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.61 sec: 1.37x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 42.2 ms: 1.26x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 60.6 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.76 ms: 1.10x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.20 us: 1.05x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| json_loads           | 20.4 us                                                         | 19.9 us: 1.02x faster                                                           |
| pickle               | 7.79 us                                                         | 7.84 us: 1.01x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.77 us: 1.01x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (2): unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.1 ms: 1.06x faster                                                           |
| python_startup         | 22.4 ms                                                         | 21.8 ms: 1.03x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.73 ms: 1.48x faster                                                           |
| django_template | 36.9 ms                                                         | 28.8 ms: 1.28x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.38x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 58.0 ns: 1.74x faster                                                           |
| generators                 | 38.5 ms                                                         | 22.4 ms: 1.72x faster                                                           |
| raytrace                   | 308 ms                                                          | 182 ms: 1.69x faster                                                            |
| deepcopy_memo              | 38.4 us                                                         | 22.8 us: 1.68x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.13 ms: 1.68x faster                                                           |
| comprehensions             | 19.2 us                                                         | 11.6 us: 1.66x faster                                                           |
| scimark_sor                | 130 ms                                                          | 79.5 ms: 1.63x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 4.29 ms: 1.59x faster                                                           |
| nbody                      | 127 ms                                                          | 80.7 ms: 1.57x faster                                                           |
| spectral_norm              | 104 ms                                                          | 66.8 ms: 1.55x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 60.2 ms: 1.55x faster                                                           |
| chaos                      | 69.4 ms                                                         | 45.0 ms: 1.54x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 137 us: 1.53x faster                                                            |
| mako                       | 9.96 ms                                                         | 6.73 ms: 1.48x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 46.0 ms: 1.44x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.5 ms: 1.44x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 199 us: 1.44x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 873 us: 1.43x faster                                                            |
| richards_super             | 46.5 ms                                                         | 32.7 ms: 1.42x faster                                                           |
| float                      | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                           |
| go                         | 137 ms                                                          | 97.2 ms: 1.41x faster                                                           |
| richards                   | 41.3 ms                                                         | 29.4 ms: 1.41x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 89.8 us: 1.41x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.30 us: 1.40x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 251 ms: 1.40x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.10 ms: 1.39x faster                                                           |
| pyflate                    | 424 ms                                                          | 308 ms: 1.38x faster                                                            |
| deepcopy                   | 360 us                                                          | 263 us: 1.37x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.61 sec: 1.37x faster                                                          |
| regex_compile              | 129 ms                                                          | 94.7 ms: 1.36x faster                                                           |
| chameleon                  | 7.75 ms                                                         | 5.69 ms: 1.36x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 270 ms: 1.35x faster                                                            |
| nqueens                    | 93.7 ms                                                         | 69.4 ms: 1.35x faster                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.13 sec: 1.33x faster                                                          |
| async_tree_io              | 693 ms                                                          | 523 ms: 1.33x faster                                                            |
| async_tree_none            | 298 ms                                                          | 225 ms: 1.32x faster                                                            |
| scimark_fft                | 271 ms                                                          | 206 ms: 1.32x faster                                                            |
| logging_simple             | 9.75 us                                                         | 7.48 us: 1.30x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 553 ms: 1.30x faster                                                            |
| fannkuch                   | 354 ms                                                          | 273 ms: 1.30x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 523 ms: 1.30x faster                                                            |
| logging_format             | 10.4 us                                                         | 8.04 us: 1.29x faster                                                           |
| pycparser                  | 978 ms                                                          | 758 ms: 1.29x faster                                                            |
| django_template            | 36.9 ms                                                         | 28.8 ms: 1.28x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 42.2 ms: 1.26x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.07 ms: 1.26x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 38.7 ms: 1.25x faster                                                           |
| crypto_pyaes               | 69.2 ms                                                         | 55.5 ms: 1.25x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 14.2 ms: 1.24x faster                                                           |
| 2to3                       | 280 ms                                                          | 229 ms: 1.22x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 101 ms: 1.22x faster                                                            |
| sympy_str                  | 240 ms                                                          | 200 ms: 1.20x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 60.6 ms: 1.19x faster                                                           |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 470 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 488 ms: 1.16x faster                                                            |
| meteor_contest             | 86.9 ms                                                         | 75.5 ms: 1.15x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.67 sec: 1.15x faster                                                          |
| sympy_expand               | 398 ms                                                          | 348 ms: 1.14x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 971 us: 1.14x faster                                                            |
| tornado_http               | 105 ms                                                          | 92.8 ms: 1.13x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 68.1 ms: 1.11x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.79 sec: 1.11x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.76 ms: 1.10x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 84.2 ms: 1.09x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.92 us: 1.08x faster                                                           |
| regex_effbot               | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 18.1 ms: 1.06x faster                                                           |
| async_generators           | 313 ms                                                          | 298 ms: 1.05x faster                                                            |
| pickle_list                | 3.37 us                                                         | 3.20 us: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| python_startup             | 22.4 ms                                                         | 21.8 ms: 1.03x faster                                                           |
| regex_dna                  | 127 ms                                                          | 124 ms: 1.03x faster                                                            |
| json                       | 4.15 ms                                                         | 4.07 ms: 1.02x faster                                                           |
| json_loads                 | 20.4 us                                                         | 19.9 us: 1.02x faster                                                           |
| pidigits                   | 199 ms                                                          | 196 ms: 1.02x faster                                                            |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.02x faster                                                           |
| pickle                     | 7.79 us                                                         | 7.84 us: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.77 us: 1.01x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 15.8 ms: 1.05x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 728 us: 1.12x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.25 ms: 1.13x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 201 ms: 2.00x slower                                                            |
| coverage                   | 48.4 ms                                                         | 489 ms: 10.09x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                    |

Benchmark hidden because not significant (3): asyncio_tcp, unpickle_list, pickle_dict
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown