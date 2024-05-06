# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 266 ms: 1.05x faster                                                              |
| chameleon      | 7.75 ms                                                         | 6.35 ms: 1.22x faster                                                             |
| docutils       | 1.98 sec                                                        | 1.97 sec: 1.01x faster                                                            |
| tornado_http   | 105 ms                                                          | 97.5 ms: 1.08x faster                                                             |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 269 ms: 1.30x faster                                                              |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                              |
| async_tree_io              | 693 ms                                                          | 549 ms: 1.26x faster                                                              |
| async_tree_memoization     | 364 ms                                                          | 294 ms: 1.24x faster                                                              |
| async_tree_io_tg           | 677 ms                                                          | 550 ms: 1.23x faster                                                              |
| async_tree_none            | 298 ms                                                          | 244 ms: 1.22x faster                                                              |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 460 ms: 1.19x faster                                                              |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 491 ms: 1.15x faster                                                              |
| Geometric mean             | (ref)                                                           | 1.23x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                             |
| nbody          | 127 ms                                                          | 96.6 ms: 1.31x faster                                                             |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 110 ms: 1.17x faster                                                              |
| regex_dna      | 127 ms                                                          | 116 ms: 1.09x faster                                                              |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                             |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                           | 1.06x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.70 sec: 1.29x faster                                                            |
| pickle_pure_python   | 286 us                                                          | 226 us: 1.27x faster                                                              |
| unpickle_pure_python | 210 us                                                          | 172 us: 1.22x faster                                                              |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.2 ms: 1.19x faster                                                             |
| xml_etree_process    | 53.2 ms                                                         | 44.9 ms: 1.19x faster                                                             |
| xml_etree_generate   | 72.1 ms                                                         | 62.3 ms: 1.16x faster                                                             |
| json_dumps           | 7.40 ms                                                         | 6.96 ms: 1.06x faster                                                             |
| pickle_list          | 3.37 us                                                         | 3.19 us: 1.05x faster                                                             |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                              |
| unpickle_list        | 2.95 us                                                         | 2.82 us: 1.04x faster                                                             |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                             |
| pickle_dict          | 19.9 us                                                         | 19.8 us: 1.01x faster                                                             |
| pickle               | 7.79 us                                                         | 7.90 us: 1.01x slower                                                             |
| unpickle             | 9.71 us                                                         | 9.93 us: 1.02x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                             |
| python_startup_no_site | 19.1 ms                                                         | 22.1 ms: 1.16x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-----------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.00 ms: 1.42x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 21.9 ms: 1.75x faster                                                             |
| logging_silent             | 101 ns                                                          | 61.2 ns: 1.65x faster                                                             |
| deepcopy_memo              | 38.4 us                                                         | 25.8 us: 1.49x faster                                                             |
| spectral_norm              | 104 ms                                                          | 70.5 ms: 1.47x faster                                                             |
| float                      | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                             |
| mako                       | 9.96 ms                                                         | 7.00 ms: 1.42x faster                                                             |
| coroutines                 | 20.9 ms                                                         | 14.9 ms: 1.40x faster                                                             |
| raytrace                   | 308 ms                                                          | 222 ms: 1.39x faster                                                              |
| scimark_sor                | 130 ms                                                          | 97.2 ms: 1.34x faster                                                             |
| nbody                      | 127 ms                                                          | 96.6 ms: 1.31x faster                                                             |
| async_tree_memoization_tg  | 350 ms                                                          | 269 ms: 1.30x faster                                                              |
| tomli_loads                | 2.20 sec                                                        | 1.70 sec: 1.29x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.80 ms: 1.28x faster                                                             |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                              |
| pickle_pure_python         | 286 us                                                          | 226 us: 1.27x faster                                                              |
| async_tree_io              | 693 ms                                                          | 549 ms: 1.26x faster                                                              |
| async_tree_memoization     | 364 ms                                                          | 294 ms: 1.24x faster                                                              |
| async_tree_io_tg           | 677 ms                                                          | 550 ms: 1.23x faster                                                              |
| sqlglot_parse              | 1.25 ms                                                         | 1.02 ms: 1.23x faster                                                             |
| async_tree_none            | 298 ms                                                          | 244 ms: 1.22x faster                                                              |
| chameleon                  | 7.75 ms                                                         | 6.35 ms: 1.22x faster                                                             |
| unpickle_pure_python       | 210 us                                                          | 172 us: 1.22x faster                                                              |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.20 ms: 1.21x faster                                                             |
| go                         | 137 ms                                                          | 114 ms: 1.20x faster                                                              |
| logging_simple             | 9.75 us                                                         | 8.13 us: 1.20x faster                                                             |
| typing_runtime_protocols   | 126 us                                                          | 105 us: 1.20x faster                                                              |
| deepcopy                   | 360 us                                                          | 302 us: 1.19x faster                                                              |
| logging_format             | 10.4 us                                                         | 8.72 us: 1.19x faster                                                             |
| sqlglot_transpile          | 1.53 ms                                                         | 1.28 ms: 1.19x faster                                                             |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.2 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 460 ms: 1.19x faster                                                              |
| xml_etree_process          | 53.2 ms                                                         | 44.9 ms: 1.19x faster                                                             |
| deepcopy_reduce            | 3.23 us                                                         | 2.72 us: 1.19x faster                                                             |
| richards                   | 41.3 ms                                                         | 34.9 ms: 1.18x faster                                                             |
| richards_super             | 46.5 ms                                                         | 39.6 ms: 1.17x faster                                                             |
| regex_compile              | 129 ms                                                          | 110 ms: 1.17x faster                                                              |
| pyflate                    | 424 ms                                                          | 362 ms: 1.17x faster                                                              |
| pycparser                  | 978 ms                                                          | 837 ms: 1.17x faster                                                              |
| comprehensions             | 19.2 us                                                         | 16.5 us: 1.16x faster                                                             |
| xml_etree_generate         | 72.1 ms                                                         | 62.3 ms: 1.16x faster                                                             |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 491 ms: 1.15x faster                                                              |
| chaos                      | 69.4 ms                                                         | 61.0 ms: 1.14x faster                                                             |
| scimark_fft                | 271 ms                                                          | 241 ms: 1.12x faster                                                              |
| async_generators           | 313 ms                                                          | 280 ms: 1.12x faster                                                              |
| bench_thread_pool          | 1.10 ms                                                         | 994 us: 1.11x faster                                                              |
| crypto_pyaes               | 69.2 ms                                                         | 63.0 ms: 1.10x faster                                                             |
| regex_dna                  | 127 ms                                                          | 116 ms: 1.09x faster                                                              |
| fannkuch                   | 354 ms                                                          | 324 ms: 1.09x faster                                                              |
| sympy_sum                  | 123 ms                                                          | 114 ms: 1.08x faster                                                              |
| tornado_http               | 105 ms                                                          | 97.5 ms: 1.08x faster                                                             |
| asyncio_tcp                | 662 ms                                                          | 616 ms: 1.07x faster                                                              |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                             |
| sympy_str                  | 240 ms                                                          | 224 ms: 1.07x faster                                                              |
| scimark_lu                 | 93.2 ms                                                         | 87.3 ms: 1.07x faster                                                             |
| json_dumps                 | 7.40 ms                                                         | 6.96 ms: 1.06x faster                                                             |
| sqlite_synth               | 2.07 us                                                         | 1.95 us: 1.06x faster                                                             |
| scimark_monte_carlo        | 66.4 ms                                                         | 62.7 ms: 1.06x faster                                                             |
| mdp                        | 1.91 sec                                                        | 1.81 sec: 1.06x faster                                                            |
| pathlib                    | 91.4 ms                                                         | 86.6 ms: 1.06x faster                                                             |
| pickle_list                | 3.37 us                                                         | 3.19 us: 1.05x faster                                                             |
| 2to3                       | 280 ms                                                          | 266 ms: 1.05x faster                                                              |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                              |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.05x faster                                                            |
| unpickle_list              | 2.95 us                                                         | 2.82 us: 1.04x faster                                                             |
| meteor_contest             | 86.9 ms                                                         | 83.4 ms: 1.04x faster                                                             |
| bench_mp_pool              | 75.4 ms                                                         | 72.8 ms: 1.04x faster                                                             |
| hexiom                     | 6.82 ms                                                         | 6.60 ms: 1.03x faster                                                             |
| sympy_expand               | 398 ms                                                          | 387 ms: 1.03x faster                                                              |
| sympy_integrate            | 17.5 ms                                                         | 17.1 ms: 1.03x faster                                                             |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                             |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                              |
| sqlglot_optimize           | 48.5 ms                                                         | 48.1 ms: 1.01x faster                                                             |
| docutils                   | 1.98 sec                                                        | 1.97 sec: 1.01x faster                                                            |
| pickle_dict                | 19.9 us                                                         | 19.8 us: 1.01x faster                                                             |
| pprint_pformat             | 1.50 sec                                                        | 1.52 sec: 1.01x slower                                                            |
| pickle                     | 7.79 us                                                         | 7.90 us: 1.01x slower                                                             |
| nqueens                    | 93.7 ms                                                         | 95.1 ms: 1.02x slower                                                             |
| pprint_safe_repr           | 721 ms                                                          | 735 ms: 1.02x slower                                                              |
| unpickle                   | 9.71 us                                                         | 9.93 us: 1.02x slower                                                             |
| json                       | 4.15 ms                                                         | 4.32 ms: 1.04x slower                                                             |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                             |
| python_startup             | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                             |
| create_gc_cycles           | 652 us                                                          | 748 us: 1.15x slower                                                              |
| python_startup_no_site     | 19.1 ms                                                         | 22.1 ms: 1.16x slower                                                             |
| telco                      | 5.51 ms                                                         | 6.40 ms: 1.16x slower                                                             |
| sqlglot_normalize          | 100 ms                                                          | 250 ms: 2.49x slower                                                              |
| coverage                   | 48.4 ms                                                         | 503 ms: 10.38x slower                                                             |
| Geometric mean             | (ref)                                                           | 1.09x faster                                                                      |

Benchmark hidden because not significant (1): gc_traversal
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown