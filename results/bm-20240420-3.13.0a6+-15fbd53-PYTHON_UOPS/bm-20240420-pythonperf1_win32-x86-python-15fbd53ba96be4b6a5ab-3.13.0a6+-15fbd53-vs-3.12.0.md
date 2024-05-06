# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.14x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 242 ms: 1.16x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.74 ms: 1.35x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.90 sec: 1.04x faster                                                          |
| tornado_http   | 105 ms                                                          | 96.6 ms: 1.09x faster                                                           |
| Geometric mean | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 259 ms: 1.36x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 210 ms: 1.32x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 278 ms: 1.31x faster                                                            |
| async_tree_io              | 693 ms                                                          | 535 ms: 1.30x faster                                                            |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 533 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 446 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 473 ms: 1.19x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 79.1 ms: 1.61x faster                                                           |
| float          | 76.7 ms                                                         | 55.1 ms: 1.39x faster                                                           |
| pidigits       | 199 ms                                                          | 200 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                           | 1.30x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 119 ms: 1.08x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| regex_dna      | 127 ms                                                          | 120 ms: 1.06x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| pickle_pure_python   | 286 us                                                          | 218 us: 1.31x faster                                                            |
| unpickle_pure_python | 210 us                                                          | 164 us: 1.28x faster                                                            |
| xml_etree_process    | 53.2 ms                                                         | 43.4 ms: 1.23x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 60.1 ms: 1.20x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 67.1 ms: 1.16x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.70 us: 1.09x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 106 ms: 1.06x faster                                                            |
| json_dumps           | 7.40 ms                                                         | 7.02 ms: 1.05x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.33 us: 1.01x faster                                                           |
| pickle               | 7.79 us                                                         | 7.76 us: 1.00x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 20.3 us: 1.02x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.94 us: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.1 ms: 1.05x faster                                                           |
| python_startup         | 22.4 ms                                                         | 21.9 ms: 1.02x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.01 ms: 1.42x faster                                                           |
| django_template | 36.9 ms                                                         | 31.9 ms: 1.16x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.28x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 59.7 ns: 1.69x faster                                                           |
| generators                 | 38.5 ms                                                         | 23.4 ms: 1.65x faster                                                           |
| nbody                      | 127 ms                                                          | 79.1 ms: 1.61x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 25.0 us: 1.53x faster                                                           |
| raytrace                   | 308 ms                                                          | 203 ms: 1.51x faster                                                            |
| mako                       | 9.96 ms                                                         | 7.01 ms: 1.42x faster                                                           |
| comprehensions             | 19.2 us                                                         | 13.7 us: 1.40x faster                                                           |
| richards                   | 41.3 ms                                                         | 29.7 ms: 1.39x faster                                                           |
| float                      | 76.7 ms                                                         | 55.1 ms: 1.39x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.58 ms: 1.39x faster                                                           |
| richards_super             | 46.5 ms                                                         | 33.7 ms: 1.38x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.2 ms: 1.37x faster                                                           |
| scimark_sor                | 130 ms                                                          | 95.3 ms: 1.36x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 92.9 us: 1.36x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 259 ms: 1.36x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| chameleon                  | 7.75 ms                                                         | 5.74 ms: 1.35x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 210 ms: 1.32x faster                                                            |
| chaos                      | 69.4 ms                                                         | 52.6 ms: 1.32x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 218 us: 1.31x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 50.8 ms: 1.31x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 278 ms: 1.31x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 955 us: 1.31x faster                                                            |
| spectral_norm              | 104 ms                                                          | 79.5 ms: 1.31x faster                                                           |
| async_tree_io              | 693 ms                                                          | 535 ms: 1.30x faster                                                            |
| scimark_fft                | 271 ms                                                          | 209 ms: 1.29x faster                                                            |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                            |
| deepcopy                   | 360 us                                                          | 281 us: 1.28x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.20 ms: 1.28x faster                                                           |
| pyflate                    | 424 ms                                                          | 332 ms: 1.28x faster                                                            |
| unpickle_pure_python       | 210 us                                                          | 164 us: 1.28x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 533 ms: 1.27x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 5.39 ms: 1.27x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.57 us: 1.26x faster                                                           |
| fannkuch                   | 354 ms                                                          | 282 ms: 1.25x faster                                                            |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.10 ms: 1.25x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.92 us: 1.23x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 43.4 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 446 ms: 1.22x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.23 sec: 1.22x faster                                                          |
| nqueens                    | 93.7 ms                                                         | 77.3 ms: 1.21x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.60 us: 1.21x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 60.1 ms: 1.20x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 603 ms: 1.20x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 473 ms: 1.19x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 58.4 ms: 1.19x faster                                                           |
| go                         | 137 ms                                                          | 116 ms: 1.18x faster                                                            |
| pycparser                  | 978 ms                                                          | 842 ms: 1.16x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 67.1 ms: 1.16x faster                                                           |
| django_template            | 36.9 ms                                                         | 31.9 ms: 1.16x faster                                                           |
| 2to3                       | 280 ms                                                          | 242 ms: 1.16x faster                                                            |
| scimark_lu                 | 93.2 ms                                                         | 80.9 ms: 1.15x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 42.9 ms: 1.13x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 77.5 ms: 1.12x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 15.8 ms: 1.11x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.72 sec: 1.11x faster                                                          |
| bench_thread_pool          | 1.10 ms                                                         | 1.00 ms: 1.10x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.70 us: 1.09x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 69.3 ms: 1.09x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 113 ms: 1.09x faster                                                            |
| tornado_http               | 105 ms                                                          | 96.6 ms: 1.09x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 84.4 ms: 1.08x faster                                                           |
| regex_compile              | 129 ms                                                          | 119 ms: 1.08x faster                                                            |
| sqlite_synth               | 2.07 us                                                         | 1.93 us: 1.08x faster                                                           |
| async_generators           | 313 ms                                                          | 291 ms: 1.08x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| sympy_str                  | 240 ms                                                          | 224 ms: 1.07x faster                                                            |
| xml_etree_parse            | 113 ms                                                          | 106 ms: 1.06x faster                                                            |
| asyncio_tcp                | 662 ms                                                          | 627 ms: 1.06x faster                                                            |
| regex_dna                  | 127 ms                                                          | 120 ms: 1.06x faster                                                            |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.7 sec: 1.05x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 7.02 ms: 1.05x faster                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 18.1 ms: 1.05x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.90 sec: 1.04x faster                                                          |
| python_startup             | 22.4 ms                                                         | 21.9 ms: 1.02x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.33 us: 1.01x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.43 ms: 1.01x faster                                                           |
| sympy_expand               | 398 ms                                                          | 394 ms: 1.01x faster                                                            |
| pickle                     | 7.79 us                                                         | 7.76 us: 1.00x faster                                                           |
| pidigits                   | 199 ms                                                          | 200 ms: 1.01x slower                                                            |
| pickle_dict                | 19.9 us                                                         | 20.3 us: 1.02x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.94 us: 1.02x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| telco                      | 5.51 ms                                                         | 6.08 ms: 1.10x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 731 us: 1.12x slower                                                            |
| sqlglot_normalize          | 100 ms                                                          | 224 ms: 2.23x slower                                                            |
| coverage                   | 48.4 ms                                                         | 512 ms: 10.57x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (2): json, json_loads
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: unknown