# Results vs. 3.12.0

- fork: python
- ref: v3.12.3
- machine: windows-x86
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.01x faster
- HPT reliability: 99.38%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 269 ms: 1.04x faster                                            |
| chameleon      | 7.75 ms                                                         | 7.39 ms: 1.05x faster                                           |
| docutils       | 1.98 sec                                                        | 1.94 sec: 1.02x faster                                          |
| Geometric mean | (ref)                                                           | 1.03x faster                                                    |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 338 ms: 1.04x faster                                            |
| async_tree_none_tg         | 278 ms                                                          | 269 ms: 1.03x faster                                            |
| async_tree_io_tg           | 677 ms                                                          | 662 ms: 1.02x faster                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 534 ms: 1.02x faster                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 553 ms: 1.02x faster                                            |
| async_tree_memoization     | 364 ms                                                          | 358 ms: 1.02x faster                                            |
| async_tree_io              | 693 ms                                                          | 683 ms: 1.01x faster                                            |
| async_tree_none            | 298 ms                                                          | 296 ms: 1.01x faster                                            |
| Geometric mean             | (ref)                                                           | 1.02x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 125 ms: 1.02x faster                                            |
| Geometric mean | (ref)                                                           | 1.01x faster                                                    |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 130 ms: 1.01x slower                                            |
| regex_dna      | 127 ms                                                          | 129 ms: 1.02x slower                                            |
| regex_v8       | 15.0 ms                                                         | 15.3 ms: 1.02x slower                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                    |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| pickle_list          | 3.37 us                                                         | 3.23 us: 1.04x faster                                           |
| unpickle             | 9.71 us                                                         | 9.53 us: 1.02x faster                                           |
| xml_etree_process    | 53.2 ms                                                         | 53.5 ms: 1.01x slower                                           |
| pickle_dict          | 19.9 us                                                         | 20.1 us: 1.01x slower                                           |
| pickle               | 7.79 us                                                         | 7.85 us: 1.01x slower                                           |
| json_dumps           | 7.40 ms                                                         | 7.49 ms: 1.01x slower                                           |
| xml_etree_generate   | 72.1 ms                                                         | 73.6 ms: 1.02x slower                                           |
| json_loads           | 20.4 us                                                         | 20.9 us: 1.03x slower                                           |
| unpickle_pure_python | 210 us                                                          | 217 us: 1.03x slower                                            |
| pickle_pure_python   | 286 us                                                          | 299 us: 1.04x slower                                            |
| unpickle_list        | 2.95 us                                                         | 3.27 us: 1.11x slower                                           |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                    |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.1 ms: 1.06x faster                                           |
| python_startup         | 22.4 ms                                                         | 21.3 ms: 1.05x faster                                           |
| Geometric mean         | (ref)                                                           | 1.05x faster                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 36.9 ms                                                         | 36.7 ms: 1.01x faster                                           |
| Geometric mean  | (ref)                                                           | 1.00x faster                                                    |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| comprehensions             | 19.2 us                                                         | 15.7 us: 1.22x faster                                           |
| typing_runtime_protocols   | 126 us                                                          | 114 us: 1.10x faster                                            |
| pathlib                    | 91.4 ms                                                         | 85.6 ms: 1.07x faster                                           |
| sympy_sum                  | 123 ms                                                          | 116 ms: 1.06x faster                                            |
| python_startup_no_site     | 19.1 ms                                                         | 18.1 ms: 1.06x faster                                           |
| telco                      | 5.51 ms                                                         | 5.22 ms: 1.06x faster                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.7 sec: 1.05x faster                                          |
| python_startup             | 22.4 ms                                                         | 21.3 ms: 1.05x faster                                           |
| mdp                        | 1.91 sec                                                        | 1.82 sec: 1.05x faster                                          |
| bench_mp_pool              | 75.4 ms                                                         | 71.9 ms: 1.05x faster                                           |
| chameleon                  | 7.75 ms                                                         | 7.39 ms: 1.05x faster                                           |
| pickle_list                | 3.37 us                                                         | 3.23 us: 1.04x faster                                           |
| 2to3                       | 280 ms                                                          | 269 ms: 1.04x faster                                            |
| sympy_integrate            | 17.5 ms                                                         | 16.9 ms: 1.04x faster                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 338 ms: 1.04x faster                                            |
| async_tree_none_tg         | 278 ms                                                          | 269 ms: 1.03x faster                                            |
| dulwich_log                | 58.5 ms                                                         | 56.7 ms: 1.03x faster                                           |
| sympy_str                  | 240 ms                                                          | 232 ms: 1.03x faster                                            |
| aiohttp                    | 1.06 ms                                                         | 1.03 ms: 1.03x faster                                           |
| gc_traversal               | 1.44 ms                                                         | 1.41 ms: 1.02x faster                                           |
| meteor_contest             | 86.9 ms                                                         | 84.8 ms: 1.02x faster                                           |
| async_tree_io_tg           | 677 ms                                                          | 662 ms: 1.02x faster                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 534 ms: 1.02x faster                                            |
| docutils                   | 1.98 sec                                                        | 1.94 sec: 1.02x faster                                          |
| bench_thread_pool          | 1.10 ms                                                         | 1.08 ms: 1.02x faster                                           |
| deepcopy_reduce            | 3.23 us                                                         | 3.16 us: 1.02x faster                                           |
| deepcopy                   | 360 us                                                          | 353 us: 1.02x faster                                            |
| nbody                      | 127 ms                                                          | 125 ms: 1.02x faster                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 553 ms: 1.02x faster                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 47.6 ms: 1.02x faster                                           |
| chaos                      | 69.4 ms                                                         | 68.1 ms: 1.02x faster                                           |
| unpickle                   | 9.71 us                                                         | 9.53 us: 1.02x faster                                           |
| sqlalchemy_imperative      | 12.3 ms                                                         | 12.1 ms: 1.02x faster                                           |
| deepcopy_memo              | 38.4 us                                                         | 37.7 us: 1.02x faster                                           |
| async_tree_memoization     | 364 ms                                                          | 358 ms: 1.02x faster                                            |
| logging_simple             | 9.75 us                                                         | 9.61 us: 1.02x faster                                           |
| go                         | 137 ms                                                          | 135 ms: 1.02x faster                                            |
| raytrace                   | 308 ms                                                          | 304 ms: 1.01x faster                                            |
| async_tree_io              | 693 ms                                                          | 683 ms: 1.01x faster                                            |
| logging_format             | 10.4 us                                                         | 10.3 us: 1.01x faster                                           |
| nqueens                    | 93.7 ms                                                         | 92.6 ms: 1.01x faster                                           |
| pycparser                  | 978 ms                                                          | 970 ms: 1.01x faster                                            |
| async_tree_none            | 298 ms                                                          | 296 ms: 1.01x faster                                            |
| django_template            | 36.9 ms                                                         | 36.7 ms: 1.01x faster                                           |
| dask                       | 323 ms                                                          | 322 ms: 1.01x faster                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.54 ms: 1.00x slower                                           |
| xml_etree_process          | 53.2 ms                                                         | 53.5 ms: 1.01x slower                                           |
| pickle_dict                | 19.9 us                                                         | 20.1 us: 1.01x slower                                           |
| pickle                     | 7.79 us                                                         | 7.85 us: 1.01x slower                                           |
| regex_compile              | 129 ms                                                          | 130 ms: 1.01x slower                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 67.0 ms: 1.01x slower                                           |
| sympy_expand               | 398 ms                                                          | 402 ms: 1.01x slower                                            |
| sqlglot_parse              | 1.25 ms                                                         | 1.26 ms: 1.01x slower                                           |
| json_dumps                 | 7.40 ms                                                         | 7.49 ms: 1.01x slower                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.52 sec: 1.02x slower                                          |
| hexiom                     | 6.82 ms                                                         | 6.93 ms: 1.02x slower                                           |
| regex_dna                  | 127 ms                                                          | 129 ms: 1.02x slower                                            |
| regex_v8                   | 15.0 ms                                                         | 15.3 ms: 1.02x slower                                           |
| xml_etree_generate         | 72.1 ms                                                         | 73.6 ms: 1.02x slower                                           |
| spectral_norm              | 104 ms                                                          | 106 ms: 1.02x slower                                            |
| pyflate                    | 424 ms                                                          | 433 ms: 1.02x slower                                            |
| sqlglot_normalize          | 100 ms                                                          | 102 ms: 1.02x slower                                            |
| fannkuch                   | 354 ms                                                          | 363 ms: 1.03x slower                                            |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.96 ms: 1.03x slower                                           |
| json_loads                 | 20.4 us                                                         | 20.9 us: 1.03x slower                                           |
| pprint_safe_repr           | 721 ms                                                          | 742 ms: 1.03x slower                                            |
| sqlite_synth               | 2.07 us                                                         | 2.13 us: 1.03x slower                                           |
| unpickle_pure_python       | 210 us                                                          | 217 us: 1.03x slower                                            |
| crypto_pyaes               | 69.2 ms                                                         | 71.7 ms: 1.04x slower                                           |
| scimark_lu                 | 93.2 ms                                                         | 96.6 ms: 1.04x slower                                           |
| richards_super             | 46.5 ms                                                         | 48.2 ms: 1.04x slower                                           |
| generators                 | 38.5 ms                                                         | 39.9 ms: 1.04x slower                                           |
| logging_silent             | 101 ns                                                          | 105 ns: 1.04x slower                                            |
| coverage                   | 48.4 ms                                                         | 50.4 ms: 1.04x slower                                           |
| pickle_pure_python         | 286 us                                                          | 299 us: 1.04x slower                                            |
| richards                   | 41.3 ms                                                         | 43.5 ms: 1.05x slower                                           |
| json                       | 4.15 ms                                                         | 4.42 ms: 1.06x slower                                           |
| unpickle_list              | 2.95 us                                                         | 3.27 us: 1.11x slower                                           |
| Geometric mean             | (ref)                                                           | 1.01x faster                                                    |

Benchmark hidden because not significant (17): asyncio_tcp, mypy2, regex_effbot, create_gc_cycles, tornado_http, sqlalchemy_declarative, tomli_loads, float, async_generators, pidigits, scimark_sor, mako, coroutines, xml_etree_iterparse, xml_etree_parse, scimark_fft, deltablue
Ignored benchmarks (1) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: unpack_sequence
Ignored benchmarks (5) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown