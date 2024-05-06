# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.00x slower
- HPT reliability: 97.02%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                          | 258 ms: 1.01x slower                                                            |
| chameleon      | 6.41 ms                                                                         | 6.25 ms: 1.03x faster                                                           |
| docutils       | 1.93 sec                                                                        | 1.95 sec: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 98.1 ms                                                                         | 94.8 ms: 1.04x faster                                                           |
| pidigits       | 199 ms                                                                          | 198 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 123 ms                                                                          | 121 ms: 1.02x faster                                                            |
| regex_effbot   | 1.93 ms                                                                         | 1.91 ms: 1.01x faster                                                           |
| regex_compile  | 113 ms                                                                          | 112 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_list        | 3.07 us                                                                         | 2.82 us: 1.09x faster                                                           |
| xml_etree_iterparse  | 67.5 ms                                                                         | 65.0 ms: 1.04x faster                                                           |
| xml_etree_parse      | 110 ms                                                                          | 106 ms: 1.04x faster                                                            |
| unpickle_pure_python | 178 us                                                                          | 172 us: 1.03x faster                                                            |
| pickle_pure_python   | 227 us                                                                          | 222 us: 1.02x faster                                                            |
| xml_etree_generate   | 61.9 ms                                                                         | 61.6 ms: 1.00x faster                                                           |
| xml_etree_process    | 44.0 ms                                                                         | 44.2 ms: 1.00x slower                                                           |
| pickle_dict          | 19.8 us                                                                         | 20.0 us: 1.01x slower                                                           |
| json_loads           | 19.7 us                                                                         | 20.0 us: 1.02x slower                                                           |
| pickle               | 7.93 us                                                                         | 8.13 us: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                                         | 10.1 us: 1.03x slower                                                           |
| pickle_list          | 3.24 us                                                                         | 3.33 us: 1.03x slower                                                           |
| tomli_loads          | 1.70 sec                                                                        | 1.80 sec: 1.06x slower                                                          |
| Geometric mean       | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 21.8 ms                                                                         | 22.0 ms: 1.01x slower                                                           |
| Geometric mean         | (ref)                                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 7.03 ms                                                                         | 6.99 ms: 1.01x faster                                                           |
| genshi_xml     | 47.0 ms                                                                         | 48.4 ms: 1.03x slower                                                           |
| genshi_text    | 21.8 ms                                                                         | 22.8 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                                           | 1.02x slower                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_list            | 3.07 us                                                                         | 2.82 us: 1.09x faster                                                           |
| async_generators         | 310 ms                                                                          | 288 ms: 1.08x faster                                                            |
| xml_etree_iterparse      | 67.5 ms                                                                         | 65.0 ms: 1.04x faster                                                           |
| xml_etree_parse          | 110 ms                                                                          | 106 ms: 1.04x faster                                                            |
| sqlglot_parse            | 1.03 ms                                                                         | 997 us: 1.04x faster                                                            |
| nbody                    | 98.1 ms                                                                         | 94.8 ms: 1.04x faster                                                           |
| unpickle_pure_python     | 178 us                                                                          | 172 us: 1.03x faster                                                            |
| sqlglot_transpile        | 1.29 ms                                                                         | 1.25 ms: 1.03x faster                                                           |
| chameleon                | 6.41 ms                                                                         | 6.25 ms: 1.03x faster                                                           |
| pickle_pure_python       | 227 us                                                                          | 222 us: 1.02x faster                                                            |
| sqlglot_normalize        | 238 ms                                                                          | 233 ms: 1.02x faster                                                            |
| regex_dna                | 123 ms                                                                          | 121 ms: 1.02x faster                                                            |
| deepcopy_reduce          | 2.66 us                                                                         | 2.61 us: 1.02x faster                                                           |
| gc_traversal             | 1.46 ms                                                                         | 1.44 ms: 1.02x faster                                                           |
| sqlglot_optimize         | 46.8 ms                                                                         | 46.2 ms: 1.01x faster                                                           |
| pycparser                | 860 ms                                                                          | 850 ms: 1.01x faster                                                            |
| generators               | 22.3 ms                                                                         | 22.0 ms: 1.01x faster                                                           |
| regex_effbot             | 1.93 ms                                                                         | 1.91 ms: 1.01x faster                                                           |
| meteor_contest           | 83.4 ms                                                                         | 82.6 ms: 1.01x faster                                                           |
| thrift                   | 10.8 ms                                                                         | 10.7 ms: 1.01x faster                                                           |
| pyflate                  | 364 ms                                                                          | 362 ms: 1.01x faster                                                            |
| regex_compile            | 113 ms                                                                          | 112 ms: 1.01x faster                                                            |
| mako                     | 7.03 ms                                                                         | 6.99 ms: 1.01x faster                                                           |
| raytrace                 | 232 ms                                                                          | 231 ms: 1.01x faster                                                            |
| deepcopy_memo            | 24.9 us                                                                         | 24.8 us: 1.00x faster                                                           |
| xml_etree_generate       | 61.9 ms                                                                         | 61.6 ms: 1.00x faster                                                           |
| coroutines               | 15.2 ms                                                                         | 15.1 ms: 1.00x faster                                                           |
| pidigits                 | 199 ms                                                                          | 198 ms: 1.00x faster                                                            |
| hexiom                   | 6.12 ms                                                                         | 6.10 ms: 1.00x faster                                                           |
| sympy_expand             | 381 ms                                                                          | 382 ms: 1.00x slower                                                            |
| sympy_str                | 220 ms                                                                          | 221 ms: 1.00x slower                                                            |
| logging_silent           | 60.8 ns                                                                         | 61.0 ns: 1.00x slower                                                           |
| xml_etree_process        | 44.0 ms                                                                         | 44.2 ms: 1.00x slower                                                           |
| crypto_pyaes             | 62.1 ms                                                                         | 62.4 ms: 1.01x slower                                                           |
| scimark_sparse_mat_mult  | 3.20 ms                                                                         | 3.22 ms: 1.01x slower                                                           |
| pathlib                  | 86.6 ms                                                                         | 87.1 ms: 1.01x slower                                                           |
| 2to3                     | 256 ms                                                                          | 258 ms: 1.01x slower                                                            |
| go                       | 123 ms                                                                          | 124 ms: 1.01x slower                                                            |
| docutils                 | 1.93 sec                                                                        | 1.95 sec: 1.01x slower                                                          |
| sympy_sum                | 111 ms                                                                          | 112 ms: 1.01x slower                                                            |
| pylint                   | 222 ms                                                                          | 224 ms: 1.01x slower                                                            |
| python_startup_no_site   | 21.8 ms                                                                         | 22.0 ms: 1.01x slower                                                           |
| chaos                    | 60.5 ms                                                                         | 61.2 ms: 1.01x slower                                                           |
| comprehensions           | 15.4 us                                                                         | 15.6 us: 1.01x slower                                                           |
| pickle_dict              | 19.8 us                                                                         | 20.0 us: 1.01x slower                                                           |
| sympy_integrate          | 16.3 ms                                                                         | 16.6 ms: 1.02x slower                                                           |
| nqueens                  | 92.8 ms                                                                         | 94.2 ms: 1.02x slower                                                           |
| json_loads               | 19.7 us                                                                         | 20.0 us: 1.02x slower                                                           |
| scimark_fft              | 241 ms                                                                          | 245 ms: 1.02x slower                                                            |
| richards_super           | 38.8 ms                                                                         | 39.5 ms: 1.02x slower                                                           |
| bench_mp_pool            | 72.4 ms                                                                         | 73.8 ms: 1.02x slower                                                           |
| fannkuch                 | 315 ms                                                                          | 321 ms: 1.02x slower                                                            |
| telco                    | 6.30 ms                                                                         | 6.43 ms: 1.02x slower                                                           |
| logging_simple           | 7.93 us                                                                         | 8.11 us: 1.02x slower                                                           |
| pickle                   | 7.93 us                                                                         | 8.13 us: 1.02x slower                                                           |
| richards                 | 34.3 ms                                                                         | 35.2 ms: 1.03x slower                                                           |
| json                     | 4.03 ms                                                                         | 4.13 ms: 1.03x slower                                                           |
| scimark_monte_carlo      | 61.6 ms                                                                         | 63.3 ms: 1.03x slower                                                           |
| unpickle                 | 9.82 us                                                                         | 10.1 us: 1.03x slower                                                           |
| sqlite_synth             | 1.93 us                                                                         | 1.98 us: 1.03x slower                                                           |
| pickle_list              | 3.24 us                                                                         | 3.33 us: 1.03x slower                                                           |
| genshi_xml               | 47.0 ms                                                                         | 48.4 ms: 1.03x slower                                                           |
| logging_format           | 8.49 us                                                                         | 8.76 us: 1.03x slower                                                           |
| mdp                      | 1.75 sec                                                                        | 1.80 sec: 1.03x slower                                                          |
| spectral_norm            | 71.3 ms                                                                         | 73.6 ms: 1.03x slower                                                           |
| coverage                 | 513 ms                                                                          | 531 ms: 1.03x slower                                                            |
| scimark_sor              | 97.2 ms                                                                         | 101 ms: 1.03x slower                                                            |
| pprint_safe_repr         | 740 ms                                                                          | 769 ms: 1.04x slower                                                            |
| pprint_pformat           | 1.51 sec                                                                        | 1.58 sec: 1.04x slower                                                          |
| genshi_text              | 21.8 ms                                                                         | 22.8 ms: 1.04x slower                                                           |
| typing_runtime_protocols | 96.0 us                                                                         | 101 us: 1.05x slower                                                            |
| tomli_loads              | 1.70 sec                                                                        | 1.80 sec: 1.06x slower                                                          |
| Geometric mean           | (ref)                                                                           | 1.00x slower                                                                    |

Benchmark hidden because not significant (21): bench_thread_pool, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, create_gc_cycles, float, regex_v8, html5lib, scimark_lu, async_tree_memoization, asyncio_tcp_ssl, async_tree_none, python_startup, deepcopy, tornado_http, deltablue, json_dumps, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, asyncio_tcp

# HPT report

- Reliability score: 97.02% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown