# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                          | 266 ms: 1.03x slower                                                              |
| chameleon      | 6.05 ms                                                                         | 6.35 ms: 1.05x slower                                                             |
| docutils       | 1.91 sec                                                                        | 1.97 sec: 1.03x slower                                                            |
| html5lib       | 45.7 ms                                                                         | 46.1 ms: 1.01x slower                                                             |
| tornado_http   | 95.3 ms                                                                         | 97.5 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.03x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg        | 543 ms                                                                          | 550 ms: 1.01x slower                                                              |
| async_tree_cpu_io_mixed | 483 ms                                                                          | 491 ms: 1.02x slower                                                              |
| async_tree_none         | 238 ms                                                                          | 244 ms: 1.03x slower                                                              |
| async_tree_memoization  | 286 ms                                                                          | 294 ms: 1.03x slower                                                              |
| Geometric mean          | (ref)                                                                           | 1.02x slower                                                                      |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 101 ms                                                                          | 96.6 ms: 1.04x faster                                                             |
| pidigits       | 199 ms                                                                          | 197 ms: 1.01x faster                                                              |
| float          | 53.3 ms                                                                         | 53.7 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                                          | 116 ms: 1.02x faster                                                              |
| regex_compile  | 112 ms                                                                          | 110 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                      |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| unpickle_list        | 2.91 us                                                                         | 2.82 us: 1.03x faster                                                             |
| tomli_loads          | 1.75 sec                                                                        | 1.70 sec: 1.03x faster                                                            |
| pickle_dict          | 20.0 us                                                                         | 19.8 us: 1.01x faster                                                             |
| unpickle             | 9.86 us                                                                         | 9.93 us: 1.01x slower                                                             |
| pickle_list          | 3.17 us                                                                         | 3.19 us: 1.01x slower                                                             |
| unpickle_pure_python | 170 us                                                                          | 172 us: 1.01x slower                                                              |
| pickle_pure_python   | 223 us                                                                          | 226 us: 1.01x slower                                                              |
| json_loads           | 19.8 us                                                                         | 20.1 us: 1.01x slower                                                             |
| json_dumps           | 6.82 ms                                                                         | 6.96 ms: 1.02x slower                                                             |
| xml_etree_generate   | 60.7 ms                                                                         | 62.3 ms: 1.03x slower                                                             |
| xml_etree_process    | 43.0 ms                                                                         | 44.9 ms: 1.04x slower                                                             |
| Geometric mean       | (ref)                                                                           | 1.01x slower                                                                      |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 22.4 ms                                                                         | 22.1 ms: 1.02x faster                                                             |
| python_startup         | 24.6 ms                                                                         | 24.3 ms: 1.01x faster                                                             |
| Geometric mean         | (ref)                                                                           | 1.01x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 7.13 ms                                                                         | 7.00 ms: 1.02x faster                                                             |
| genshi_xml     | 47.6 ms                                                                         | 48.5 ms: 1.02x slower                                                             |
| genshi_text    | 21.6 ms                                                                         | 23.8 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.03x slower                                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| scimark_sor              | 103 ms                                                                          | 97.2 ms: 1.06x faster                                                             |
| go                       | 119 ms                                                                          | 114 ms: 1.04x faster                                                              |
| nbody                    | 101 ms                                                                          | 96.6 ms: 1.04x faster                                                             |
| generators               | 22.8 ms                                                                         | 21.9 ms: 1.04x faster                                                             |
| unpickle_list            | 2.91 us                                                                         | 2.82 us: 1.03x faster                                                             |
| tomli_loads              | 1.75 sec                                                                        | 1.70 sec: 1.03x faster                                                            |
| async_generators         | 287 ms                                                                          | 280 ms: 1.02x faster                                                              |
| coverage                 | 514 ms                                                                          | 503 ms: 1.02x faster                                                              |
| regex_dna                | 118 ms                                                                          | 116 ms: 1.02x faster                                                              |
| mako                     | 7.13 ms                                                                         | 7.00 ms: 1.02x faster                                                             |
| python_startup_no_site   | 22.4 ms                                                                         | 22.1 ms: 1.02x faster                                                             |
| scimark_lu               | 88.9 ms                                                                         | 87.3 ms: 1.02x faster                                                             |
| gc_traversal             | 1.46 ms                                                                         | 1.44 ms: 1.02x faster                                                             |
| scimark_fft              | 244 ms                                                                          | 241 ms: 1.01x faster                                                              |
| regex_compile            | 112 ms                                                                          | 110 ms: 1.01x faster                                                              |
| spectral_norm            | 71.5 ms                                                                         | 70.5 ms: 1.01x faster                                                             |
| python_startup           | 24.6 ms                                                                         | 24.3 ms: 1.01x faster                                                             |
| crypto_pyaes             | 63.6 ms                                                                         | 63.0 ms: 1.01x faster                                                             |
| fannkuch                 | 327 ms                                                                          | 324 ms: 1.01x faster                                                              |
| pickle_dict              | 20.0 us                                                                         | 19.8 us: 1.01x faster                                                             |
| coroutines               | 15.0 ms                                                                         | 14.9 ms: 1.01x faster                                                             |
| pidigits                 | 199 ms                                                                          | 197 ms: 1.01x faster                                                              |
| bench_mp_pool            | 72.5 ms                                                                         | 72.8 ms: 1.00x slower                                                             |
| pprint_safe_repr         | 732 ms                                                                          | 735 ms: 1.00x slower                                                              |
| sqlite_synth             | 1.94 us                                                                         | 1.95 us: 1.00x slower                                                             |
| float                    | 53.3 ms                                                                         | 53.7 ms: 1.01x slower                                                             |
| unpickle                 | 9.86 us                                                                         | 9.93 us: 1.01x slower                                                             |
| pickle_list              | 3.17 us                                                                         | 3.19 us: 1.01x slower                                                             |
| pathlib                  | 85.9 ms                                                                         | 86.6 ms: 1.01x slower                                                             |
| logging_format           | 8.65 us                                                                         | 8.72 us: 1.01x slower                                                             |
| sympy_expand             | 383 ms                                                                          | 387 ms: 1.01x slower                                                              |
| html5lib                 | 45.7 ms                                                                         | 46.1 ms: 1.01x slower                                                             |
| pprint_pformat           | 1.50 sec                                                                        | 1.52 sec: 1.01x slower                                                            |
| sympy_str                | 222 ms                                                                          | 224 ms: 1.01x slower                                                              |
| meteor_contest           | 82.5 ms                                                                         | 83.4 ms: 1.01x slower                                                             |
| create_gc_cycles         | 740 us                                                                          | 748 us: 1.01x slower                                                              |
| thrift                   | 10.6 ms                                                                         | 10.7 ms: 1.01x slower                                                             |
| unpickle_pure_python     | 170 us                                                                          | 172 us: 1.01x slower                                                              |
| chaos                    | 60.2 ms                                                                         | 61.0 ms: 1.01x slower                                                             |
| async_tree_io_tg         | 543 ms                                                                          | 550 ms: 1.01x slower                                                              |
| logging_simple           | 8.02 us                                                                         | 8.13 us: 1.01x slower                                                             |
| pickle_pure_python       | 223 us                                                                          | 226 us: 1.01x slower                                                              |
| json_loads               | 19.8 us                                                                         | 20.1 us: 1.01x slower                                                             |
| deepcopy_reduce          | 2.68 us                                                                         | 2.72 us: 1.02x slower                                                             |
| sympy_sum                | 112 ms                                                                          | 114 ms: 1.02x slower                                                              |
| async_tree_cpu_io_mixed  | 483 ms                                                                          | 491 ms: 1.02x slower                                                              |
| logging_silent           | 60.1 ns                                                                         | 61.2 ns: 1.02x slower                                                             |
| genshi_xml               | 47.6 ms                                                                         | 48.5 ms: 1.02x slower                                                             |
| json_dumps               | 6.82 ms                                                                         | 6.96 ms: 1.02x slower                                                             |
| tornado_http             | 95.3 ms                                                                         | 97.5 ms: 1.02x slower                                                             |
| mdp                      | 1.77 sec                                                                        | 1.81 sec: 1.02x slower                                                            |
| async_tree_none          | 238 ms                                                                          | 244 ms: 1.03x slower                                                              |
| pylint                   | 222 ms                                                                          | 228 ms: 1.03x slower                                                              |
| xml_etree_generate       | 60.7 ms                                                                         | 62.3 ms: 1.03x slower                                                             |
| async_tree_memoization   | 286 ms                                                                          | 294 ms: 1.03x slower                                                              |
| sqlglot_parse            | 990 us                                                                          | 1.02 ms: 1.03x slower                                                             |
| sqlglot_optimize         | 46.8 ms                                                                         | 48.1 ms: 1.03x slower                                                             |
| scimark_monte_carlo      | 60.9 ms                                                                         | 62.7 ms: 1.03x slower                                                             |
| nqueens                  | 92.2 ms                                                                         | 95.1 ms: 1.03x slower                                                             |
| 2to3                     | 258 ms                                                                          | 266 ms: 1.03x slower                                                              |
| docutils                 | 1.91 sec                                                                        | 1.97 sec: 1.03x slower                                                            |
| sqlglot_transpile        | 1.24 ms                                                                         | 1.28 ms: 1.03x slower                                                             |
| richards_super           | 38.2 ms                                                                         | 39.6 ms: 1.04x slower                                                             |
| deepcopy_memo            | 24.9 us                                                                         | 25.8 us: 1.04x slower                                                             |
| deltablue                | 2.70 ms                                                                         | 2.80 ms: 1.04x slower                                                             |
| sympy_integrate          | 16.4 ms                                                                         | 17.1 ms: 1.04x slower                                                             |
| deepcopy                 | 290 us                                                                          | 302 us: 1.04x slower                                                              |
| xml_etree_process        | 43.0 ms                                                                         | 44.9 ms: 1.04x slower                                                             |
| richards                 | 33.4 ms                                                                         | 34.9 ms: 1.05x slower                                                             |
| chameleon                | 6.05 ms                                                                         | 6.35 ms: 1.05x slower                                                             |
| typing_runtime_protocols | 99.8 us                                                                         | 105 us: 1.06x slower                                                              |
| comprehensions           | 15.6 us                                                                         | 16.5 us: 1.06x slower                                                             |
| sqlglot_normalize        | 235 ms                                                                          | 250 ms: 1.06x slower                                                              |
| json                     | 4.01 ms                                                                         | 4.32 ms: 1.08x slower                                                             |
| hexiom                   | 6.09 ms                                                                         | 6.60 ms: 1.08x slower                                                             |
| genshi_text              | 21.6 ms                                                                         | 23.8 ms: 1.10x slower                                                             |
| Geometric mean           | (ref)                                                                           | 1.01x slower                                                                      |

Benchmark hidden because not significant (17): bench_thread_pool, asyncio_tcp, scimark_sparse_mat_mult, pyflate, regex_v8, xml_etree_parse, xml_etree_iterparse, pycparser, telco, raytrace, regex_effbot, pickle, asyncio_tcp_ssl, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io

# HPT report

- Reliability score: 99.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown