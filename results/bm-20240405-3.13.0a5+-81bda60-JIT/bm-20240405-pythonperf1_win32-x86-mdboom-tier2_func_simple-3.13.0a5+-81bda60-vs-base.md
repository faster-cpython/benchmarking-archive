# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-x86
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.01x faster
- HPT reliability: 97.84%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                          | 255 ms: 1.01x faster                                                         |
| chameleon      | 6.41 ms                                                                         | 6.16 ms: 1.04x faster                                                        |
| docutils       | 1.93 sec                                                                        | 1.94 sec: 1.00x slower                                                       |
| html5lib       | 46.6 ms                                                                         | 45.9 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg       | 551 ms                                                                          | 542 ms: 1.02x faster                                                         |
| async_tree_memoization | 290 ms                                                                          | 286 ms: 1.01x faster                                                         |
| async_tree_none        | 241 ms                                                                          | 238 ms: 1.01x faster                                                         |
| Geometric mean         | (ref)                                                                           | 1.01x faster                                                                 |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 98.1 ms                                                                         | 96.4 ms: 1.02x faster                                                        |
| pidigits       | 199 ms                                                                          | 198 ms: 1.01x faster                                                         |
| float          | 53.2 ms                                                                         | 54.0 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 1.93 ms                                                                         | 1.90 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                 |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list        | 3.07 us                                                                         | 2.75 us: 1.12x faster                                                        |
| xml_etree_iterparse  | 67.5 ms                                                                         | 65.4 ms: 1.03x faster                                                        |
| pickle_pure_python   | 227 us                                                                          | 221 us: 1.03x faster                                                         |
| unpickle_pure_python | 178 us                                                                          | 173 us: 1.03x faster                                                         |
| xml_etree_parse      | 110 ms                                                                          | 107 ms: 1.03x faster                                                         |
| xml_etree_generate   | 61.9 ms                                                                         | 60.4 ms: 1.02x faster                                                        |
| pickle_list          | 3.24 us                                                                         | 3.17 us: 1.02x faster                                                        |
| xml_etree_process    | 44.0 ms                                                                         | 43.2 ms: 1.02x faster                                                        |
| json_dumps           | 6.83 ms                                                                         | 6.76 ms: 1.01x faster                                                        |
| pickle_dict          | 19.8 us                                                                         | 19.8 us: 1.00x slower                                                        |
| unpickle             | 9.82 us                                                                         | 9.95 us: 1.01x slower                                                        |
| json_loads           | 19.7 us                                                                         | 20.1 us: 1.02x slower                                                        |
| tomli_loads          | 1.70 sec                                                                        | 1.75 sec: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                                           | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text    | 21.8 ms                                                                         | 21.6 ms: 1.01x faster                                                        |
| mako           | 7.03 ms                                                                         | 7.14 ms: 1.01x slower                                                        |
| genshi_xml     | 47.0 ms                                                                         | 47.8 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:-------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list            | 3.07 us                                                                         | 2.75 us: 1.12x faster                                                        |
| async_generators         | 310 ms                                                                          | 283 ms: 1.10x faster                                                         |
| raytrace                 | 232 ms                                                                          | 222 ms: 1.05x faster                                                         |
| sqlglot_transpile        | 1.29 ms                                                                         | 1.24 ms: 1.04x faster                                                        |
| chameleon                | 6.41 ms                                                                         | 6.16 ms: 1.04x faster                                                        |
| sympy_expand             | 381 ms                                                                          | 368 ms: 1.03x faster                                                         |
| xml_etree_iterparse      | 67.5 ms                                                                         | 65.4 ms: 1.03x faster                                                        |
| chaos                    | 60.5 ms                                                                         | 58.8 ms: 1.03x faster                                                        |
| pickle_pure_python       | 227 us                                                                          | 221 us: 1.03x faster                                                         |
| sqlglot_parse            | 1.03 ms                                                                         | 1.00 ms: 1.03x faster                                                        |
| unpickle_pure_python     | 178 us                                                                          | 173 us: 1.03x faster                                                         |
| bench_thread_pool        | 1.01 ms                                                                         | 985 us: 1.03x faster                                                         |
| xml_etree_parse          | 110 ms                                                                          | 107 ms: 1.03x faster                                                         |
| xml_etree_generate       | 61.9 ms                                                                         | 60.4 ms: 1.02x faster                                                        |
| sympy_sum                | 111 ms                                                                          | 109 ms: 1.02x faster                                                         |
| pycparser                | 860 ms                                                                          | 841 ms: 1.02x faster                                                         |
| coroutines               | 15.2 ms                                                                         | 14.9 ms: 1.02x faster                                                        |
| pickle_list              | 3.24 us                                                                         | 3.17 us: 1.02x faster                                                        |
| sqlite_synth             | 1.93 us                                                                         | 1.90 us: 1.02x faster                                                        |
| xml_etree_process        | 44.0 ms                                                                         | 43.2 ms: 1.02x faster                                                        |
| nbody                    | 98.1 ms                                                                         | 96.4 ms: 1.02x faster                                                        |
| async_tree_io_tg         | 551 ms                                                                          | 542 ms: 1.02x faster                                                         |
| sympy_str                | 220 ms                                                                          | 217 ms: 1.02x faster                                                         |
| go                       | 123 ms                                                                          | 121 ms: 1.02x faster                                                         |
| coverage                 | 513 ms                                                                          | 505 ms: 1.02x faster                                                         |
| scimark_fft              | 241 ms                                                                          | 237 ms: 1.02x faster                                                         |
| deepcopy_reduce          | 2.66 us                                                                         | 2.62 us: 1.02x faster                                                        |
| async_tree_memoization   | 290 ms                                                                          | 286 ms: 1.01x faster                                                         |
| regex_effbot             | 1.93 ms                                                                         | 1.90 ms: 1.01x faster                                                        |
| html5lib                 | 46.6 ms                                                                         | 45.9 ms: 1.01x faster                                                        |
| create_gc_cycles         | 748 us                                                                          | 738 us: 1.01x faster                                                         |
| logging_silent           | 60.8 ns                                                                         | 60.0 ns: 1.01x faster                                                        |
| async_tree_none          | 241 ms                                                                          | 238 ms: 1.01x faster                                                         |
| sqlglot_normalize        | 238 ms                                                                          | 235 ms: 1.01x faster                                                         |
| thrift                   | 10.8 ms                                                                         | 10.7 ms: 1.01x faster                                                        |
| json_dumps               | 6.83 ms                                                                         | 6.76 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult  | 3.20 ms                                                                         | 3.18 ms: 1.01x faster                                                        |
| genshi_text              | 21.8 ms                                                                         | 21.6 ms: 1.01x faster                                                        |
| sympy_integrate          | 16.3 ms                                                                         | 16.2 ms: 1.01x faster                                                        |
| sqlglot_optimize         | 46.8 ms                                                                         | 46.4 ms: 1.01x faster                                                        |
| scimark_monte_carlo      | 61.6 ms                                                                         | 61.2 ms: 1.01x faster                                                        |
| gc_traversal             | 1.46 ms                                                                         | 1.45 ms: 1.01x faster                                                        |
| pidigits                 | 199 ms                                                                          | 198 ms: 1.01x faster                                                         |
| 2to3                     | 256 ms                                                                          | 255 ms: 1.01x faster                                                         |
| pylint                   | 222 ms                                                                          | 222 ms: 1.00x slower                                                         |
| generators               | 22.3 ms                                                                         | 22.4 ms: 1.00x slower                                                        |
| pickle_dict              | 19.8 us                                                                         | 19.8 us: 1.00x slower                                                        |
| hexiom                   | 6.12 ms                                                                         | 6.14 ms: 1.00x slower                                                        |
| docutils                 | 1.93 sec                                                                        | 1.94 sec: 1.00x slower                                                       |
| mdp                      | 1.75 sec                                                                        | 1.76 sec: 1.01x slower                                                       |
| pyflate                  | 364 ms                                                                          | 368 ms: 1.01x slower                                                         |
| unpickle                 | 9.82 us                                                                         | 9.95 us: 1.01x slower                                                        |
| spectral_norm            | 71.3 ms                                                                         | 72.3 ms: 1.01x slower                                                        |
| mako                     | 7.03 ms                                                                         | 7.14 ms: 1.01x slower                                                        |
| float                    | 53.2 ms                                                                         | 54.0 ms: 1.02x slower                                                        |
| deepcopy_memo            | 24.9 us                                                                         | 25.3 us: 1.02x slower                                                        |
| deepcopy                 | 290 us                                                                          | 294 us: 1.02x slower                                                         |
| genshi_xml               | 47.0 ms                                                                         | 47.8 ms: 1.02x slower                                                        |
| logging_simple           | 7.93 us                                                                         | 8.06 us: 1.02x slower                                                        |
| comprehensions           | 15.4 us                                                                         | 15.7 us: 1.02x slower                                                        |
| telco                    | 6.30 ms                                                                         | 6.42 ms: 1.02x slower                                                        |
| json_loads               | 19.7 us                                                                         | 20.1 us: 1.02x slower                                                        |
| pprint_pformat           | 1.51 sec                                                                        | 1.54 sec: 1.02x slower                                                       |
| crypto_pyaes             | 62.1 ms                                                                         | 63.4 ms: 1.02x slower                                                        |
| pprint_safe_repr         | 740 ms                                                                          | 757 ms: 1.02x slower                                                         |
| richards                 | 34.3 ms                                                                         | 35.1 ms: 1.02x slower                                                        |
| logging_format           | 8.49 us                                                                         | 8.73 us: 1.03x slower                                                        |
| tomli_loads              | 1.70 sec                                                                        | 1.75 sec: 1.03x slower                                                       |
| typing_runtime_protocols | 96.0 us                                                                         | 98.7 us: 1.03x slower                                                        |
| richards_super           | 38.8 ms                                                                         | 40.0 ms: 1.03x slower                                                        |
| fannkuch                 | 315 ms                                                                          | 327 ms: 1.04x slower                                                         |
| Geometric mean           | (ref)                                                                           | 1.01x faster                                                                 |

Benchmark hidden because not significant (22): async_tree_memoization_tg, async_tree_io, asyncio_tcp, async_tree_none_tg, python_startup_no_site, regex_compile, python_startup, meteor_contest, asyncio_tcp_ssl, async_tree_cpu_io_mixed, scimark_lu, tornado_http, pathlib, bench_mp_pool, pickle, regex_dna, scimark_sor, nqueens, regex_v8, json, deltablue, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 97.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown