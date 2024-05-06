# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 266 ms: 1.06x faster                                                              |
| chameleon      | 8.08 ms                                                         | 6.35 ms: 1.27x faster                                                             |
| docutils       | 2.10 sec                                                        | 1.97 sec: 1.07x faster                                                            |
| html5lib       | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                             |
| tornado_http   | 118 ms                                                          | 97.5 ms: 1.21x faster                                                             |
| Geometric mean | (ref)                                                           | 1.15x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 244 ms: 1.41x faster                                                              |
| async_tree_memoization_tg  | 378 ms                                                          | 269 ms: 1.40x faster                                                              |
| async_tree_memoization     | 408 ms                                                          | 294 ms: 1.39x faster                                                              |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.38x faster                                                              |
| async_tree_io              | 754 ms                                                          | 549 ms: 1.37x faster                                                              |
| async_tree_io_tg           | 746 ms                                                          | 550 ms: 1.36x faster                                                              |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 460 ms: 1.25x faster                                                              |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 491 ms: 1.20x faster                                                              |
| Geometric mean             | (ref)                                                           | 1.34x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                             |
| nbody          | 126 ms                                                          | 96.6 ms: 1.30x faster                                                             |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                              |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 110 ms: 1.34x faster                                                              |
| regex_dna      | 122 ms                                                          | 116 ms: 1.05x faster                                                              |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                             |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                           | 1.06x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.96 ms: 1.41x faster                                                             |
| pickle_pure_python   | 309 us                                                          | 226 us: 1.37x faster                                                              |
| tomli_loads          | 2.31 sec                                                        | 1.70 sec: 1.36x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 172 us: 1.34x faster                                                              |
| xml_etree_process    | 55.0 ms                                                         | 44.9 ms: 1.23x faster                                                             |
| unpickle_list        | 3.28 us                                                         | 2.82 us: 1.16x faster                                                             |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.2 ms: 1.16x faster                                                             |
| xml_etree_generate   | 71.6 ms                                                         | 62.3 ms: 1.15x faster                                                             |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                              |
| pickle_list          | 3.27 us                                                         | 3.19 us: 1.02x faster                                                             |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                                             |
| pickle               | 7.99 us                                                         | 7.90 us: 1.01x faster                                                             |
| json_loads           | 20.0 us                                                         | 20.1 us: 1.00x slower                                                             |
| unpickle             | 9.23 us                                                         | 9.93 us: 1.08x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.3 ms: 1.11x slower                                                             |
| python_startup_no_site | 18.8 ms                                                         | 22.1 ms: 1.17x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 10.3 ms                                                         | 7.00 ms: 1.47x faster                                                             |
| genshi_xml     | 61.2 ms                                                         | 48.5 ms: 1.26x faster                                                             |
| genshi_text    | 26.8 ms                                                         | 23.8 ms: 1.12x faster                                                             |
| Geometric mean | (ref)                                                           | 1.28x faster                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 105 us: 4.54x faster                                                              |
| generators                 | 52.2 ms                                                         | 21.9 ms: 2.38x faster                                                             |
| logging_silent             | 119 ns                                                          | 61.2 ns: 1.95x faster                                                             |
| pylint                     | 418 ms                                                          | 228 ms: 1.84x faster                                                              |
| spectral_norm              | 122 ms                                                          | 70.5 ms: 1.72x faster                                                             |
| coroutines                 | 23.7 ms                                                         | 14.9 ms: 1.60x faster                                                             |
| deepcopy_memo              | 40.0 us                                                         | 25.8 us: 1.55x faster                                                             |
| richards_super             | 58.7 ms                                                         | 39.6 ms: 1.48x faster                                                             |
| raytrace                   | 327 ms                                                          | 222 ms: 1.47x faster                                                              |
| mako                       | 10.3 ms                                                         | 7.00 ms: 1.47x faster                                                             |
| sqlglot_parse              | 1.49 ms                                                         | 1.02 ms: 1.47x faster                                                             |
| deltablue                  | 4.10 ms                                                         | 2.80 ms: 1.46x faster                                                             |
| float                      | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                             |
| json_dumps                 | 9.80 ms                                                         | 6.96 ms: 1.41x faster                                                             |
| async_tree_none            | 343 ms                                                          | 244 ms: 1.41x faster                                                              |
| async_tree_memoization_tg  | 378 ms                                                          | 269 ms: 1.40x faster                                                              |
| richards                   | 48.8 ms                                                         | 34.9 ms: 1.40x faster                                                             |
| scimark_sor                | 135 ms                                                          | 97.2 ms: 1.39x faster                                                             |
| async_tree_memoization     | 408 ms                                                          | 294 ms: 1.39x faster                                                              |
| sqlglot_transpile          | 1.78 ms                                                         | 1.28 ms: 1.39x faster                                                             |
| async_tree_none_tg         | 301 ms                                                          | 217 ms: 1.38x faster                                                              |
| chaos                      | 84.4 ms                                                         | 61.0 ms: 1.38x faster                                                             |
| async_tree_io              | 754 ms                                                          | 549 ms: 1.37x faster                                                              |
| pickle_pure_python         | 309 us                                                          | 226 us: 1.37x faster                                                              |
| tomli_loads                | 2.31 sec                                                        | 1.70 sec: 1.36x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 550 ms: 1.36x faster                                                              |
| unpickle_pure_python       | 231 us                                                          | 172 us: 1.34x faster                                                              |
| regex_compile              | 148 ms                                                          | 110 ms: 1.34x faster                                                              |
| comprehensions             | 22.1 us                                                         | 16.5 us: 1.34x faster                                                             |
| logging_simple             | 10.8 us                                                         | 8.13 us: 1.33x faster                                                             |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.20 ms: 1.32x faster                                                             |
| logging_format             | 11.5 us                                                         | 8.72 us: 1.31x faster                                                             |
| sympy_sum                  | 149 ms                                                          | 114 ms: 1.31x faster                                                              |
| nbody                      | 126 ms                                                          | 96.6 ms: 1.30x faster                                                             |
| pyflate                    | 471 ms                                                          | 362 ms: 1.30x faster                                                              |
| go                         | 147 ms                                                          | 114 ms: 1.29x faster                                                              |
| asyncio_tcp                | 787 ms                                                          | 616 ms: 1.28x faster                                                              |
| chameleon                  | 8.08 ms                                                         | 6.35 ms: 1.27x faster                                                             |
| deepcopy                   | 381 us                                                          | 302 us: 1.26x faster                                                              |
| genshi_xml                 | 61.2 ms                                                         | 48.5 ms: 1.26x faster                                                             |
| sympy_str                  | 283 ms                                                          | 224 ms: 1.26x faster                                                              |
| crypto_pyaes               | 79.4 ms                                                         | 63.0 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 460 ms: 1.25x faster                                                              |
| pycparser                  | 1.04 sec                                                        | 837 ms: 1.25x faster                                                              |
| fannkuch                   | 399 ms                                                          | 324 ms: 1.23x faster                                                              |
| xml_etree_process          | 55.0 ms                                                         | 44.9 ms: 1.23x faster                                                             |
| deepcopy_reduce            | 3.32 us                                                         | 2.72 us: 1.22x faster                                                             |
| tornado_http               | 118 ms                                                          | 97.5 ms: 1.21x faster                                                             |
| scimark_fft                | 291 ms                                                          | 241 ms: 1.21x faster                                                              |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 491 ms: 1.20x faster                                                              |
| sympy_expand               | 462 ms                                                          | 387 ms: 1.20x faster                                                              |
| html5lib                   | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                             |
| nqueens                    | 111 ms                                                          | 95.1 ms: 1.17x faster                                                             |
| scimark_lu                 | 102 ms                                                          | 87.3 ms: 1.17x faster                                                             |
| sympy_integrate            | 19.9 ms                                                         | 17.1 ms: 1.17x faster                                                             |
| unpickle_list              | 3.28 us                                                         | 2.82 us: 1.16x faster                                                             |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.2 ms: 1.16x faster                                                             |
| xml_etree_generate         | 71.6 ms                                                         | 62.3 ms: 1.15x faster                                                             |
| bench_thread_pool          | 1.14 ms                                                         | 994 us: 1.14x faster                                                              |
| mdp                        | 2.07 sec                                                        | 1.81 sec: 1.14x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.60 ms: 1.14x faster                                                             |
| scimark_monte_carlo        | 70.8 ms                                                         | 62.7 ms: 1.13x faster                                                             |
| genshi_text                | 26.8 ms                                                         | 23.8 ms: 1.12x faster                                                             |
| pprint_pformat             | 1.70 sec                                                        | 1.52 sec: 1.12x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 735 ms: 1.11x faster                                                              |
| json                       | 4.78 ms                                                         | 4.32 ms: 1.11x faster                                                             |
| sqlite_synth               | 2.15 us                                                         | 1.95 us: 1.10x faster                                                             |
| meteor_contest             | 90.9 ms                                                         | 83.4 ms: 1.09x faster                                                             |
| sqlglot_optimize           | 51.8 ms                                                         | 48.1 ms: 1.08x faster                                                             |
| docutils                   | 2.10 sec                                                        | 1.97 sec: 1.07x faster                                                            |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                              |
| 2to3                       | 282 ms                                                          | 266 ms: 1.06x faster                                                              |
| regex_dna                  | 122 ms                                                          | 116 ms: 1.05x faster                                                              |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                              |
| pickle_list                | 3.27 us                                                         | 3.19 us: 1.02x faster                                                             |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                                             |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                            |
| pickle                     | 7.99 us                                                         | 7.90 us: 1.01x faster                                                             |
| json_loads                 | 20.0 us                                                         | 20.1 us: 1.00x slower                                                             |
| bench_mp_pool              | 70.9 ms                                                         | 72.8 ms: 1.03x slower                                                             |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                             |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                             |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                             |
| unpickle                   | 9.23 us                                                         | 9.93 us: 1.08x slower                                                             |
| async_generators           | 260 ms                                                          | 280 ms: 1.08x slower                                                              |
| pathlib                    | 79.9 ms                                                         | 86.6 ms: 1.08x slower                                                             |
| python_startup             | 22.0 ms                                                         | 24.3 ms: 1.11x slower                                                             |
| python_startup_no_site     | 18.8 ms                                                         | 22.1 ms: 1.17x slower                                                             |
| telco                      | 5.29 ms                                                         | 6.40 ms: 1.21x slower                                                             |
| create_gc_cycles           | 618 us                                                          | 748 us: 1.21x slower                                                              |
| sqlglot_normalize          | 113 ms                                                          | 250 ms: 2.21x slower                                                              |
| coverage                   | 58.0 ms                                                         | 503 ms: 8.66x slower                                                              |
| thrift                     | 801 us                                                          | 10.7 ms: 13.38x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.16x faster                                                                      |
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown