# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.01x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                          | 255 ms: 1.01x faster                                                            |
| chameleon      | 6.41 ms                                                                         | 6.27 ms: 1.02x faster                                                           |
| html5lib       | 46.6 ms                                                                         | 45.4 ms: 1.03x faster                                                           |
| tornado_http   | 96.5 ms                                                                         | 95.5 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none         | 241 ms                                                                          | 238 ms: 1.01x faster                                                            |
| async_tree_io_tg        | 551 ms                                                                          | 547 ms: 1.01x faster                                                            |
| async_tree_cpu_io_mixed | 486 ms                                                                          | 491 ms: 1.01x slower                                                            |
| Geometric mean          | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 98.1 ms                                                                         | 96.9 ms: 1.01x faster                                                           |
| pidigits       | 199 ms                                                                          | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 113 ms                                                                          | 110 ms: 1.02x faster                                                            |
| regex_dna      | 123 ms                                                                          | 122 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_list        | 3.07 us                                                                         | 2.82 us: 1.09x faster                                                           |
| pickle_pure_python   | 227 us                                                                          | 216 us: 1.05x faster                                                            |
| xml_etree_iterparse  | 67.5 ms                                                                         | 65.7 ms: 1.03x faster                                                           |
| unpickle_pure_python | 178 us                                                                          | 174 us: 1.02x faster                                                            |
| xml_etree_process    | 44.0 ms                                                                         | 43.0 ms: 1.02x faster                                                           |
| pickle_list          | 3.24 us                                                                         | 3.17 us: 1.02x faster                                                           |
| xml_etree_generate   | 61.9 ms                                                                         | 60.7 ms: 1.02x faster                                                           |
| xml_etree_parse      | 110 ms                                                                          | 108 ms: 1.02x faster                                                            |
| pickle_dict          | 19.8 us                                                                         | 19.8 us: 1.00x slower                                                           |
| json_loads           | 19.7 us                                                                         | 20.1 us: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                                         | 10.2 us: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (3): pickle, json_dumps, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 24.2 ms                                                                         | 23.9 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text    | 21.8 ms                                                                         | 20.7 ms: 1.05x faster                                                           |
| genshi_xml     | 47.0 ms                                                                         | 46.6 ms: 1.01x faster                                                           |
| mako           | 7.03 ms                                                                         | 7.13 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                                           | 1.02x faster                                                                    |

All benchmarks:
===============

| Benchmark               | bm-20240405-pythonperf1_win32-x86-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_list           | 3.07 us                                                                         | 2.82 us: 1.09x faster                                                           |
| async_generators        | 310 ms                                                                          | 286 ms: 1.09x faster                                                            |
| raytrace                | 232 ms                                                                          | 220 ms: 1.06x faster                                                            |
| genshi_text             | 21.8 ms                                                                         | 20.7 ms: 1.05x faster                                                           |
| pickle_pure_python      | 227 us                                                                          | 216 us: 1.05x faster                                                            |
| sqlglot_parse           | 1.03 ms                                                                         | 988 us: 1.05x faster                                                            |
| asyncio_tcp             | 634 ms                                                                          | 607 ms: 1.04x faster                                                            |
| scimark_monte_carlo     | 61.6 ms                                                                         | 59.4 ms: 1.04x faster                                                           |
| sqlglot_transpile       | 1.29 ms                                                                         | 1.24 ms: 1.04x faster                                                           |
| bench_thread_pool       | 1.01 ms                                                                         | 981 us: 1.03x faster                                                            |
| sqlglot_optimize        | 46.8 ms                                                                         | 45.4 ms: 1.03x faster                                                           |
| coverage                | 513 ms                                                                          | 499 ms: 1.03x faster                                                            |
| sqlglot_normalize       | 238 ms                                                                          | 232 ms: 1.03x faster                                                            |
| thrift                  | 10.8 ms                                                                         | 10.5 ms: 1.03x faster                                                           |
| html5lib                | 46.6 ms                                                                         | 45.4 ms: 1.03x faster                                                           |
| xml_etree_iterparse     | 67.5 ms                                                                         | 65.7 ms: 1.03x faster                                                           |
| pathlib                 | 86.6 ms                                                                         | 84.6 ms: 1.02x faster                                                           |
| unpickle_pure_python    | 178 us                                                                          | 174 us: 1.02x faster                                                            |
| logging_silent          | 60.8 ns                                                                         | 59.4 ns: 1.02x faster                                                           |
| pycparser               | 860 ms                                                                          | 841 ms: 1.02x faster                                                            |
| xml_etree_process       | 44.0 ms                                                                         | 43.0 ms: 1.02x faster                                                           |
| sympy_expand            | 381 ms                                                                          | 373 ms: 1.02x faster                                                            |
| chameleon               | 6.41 ms                                                                         | 6.27 ms: 1.02x faster                                                           |
| pickle_list             | 3.24 us                                                                         | 3.17 us: 1.02x faster                                                           |
| regex_compile           | 113 ms                                                                          | 110 ms: 1.02x faster                                                            |
| xml_etree_generate      | 61.9 ms                                                                         | 60.7 ms: 1.02x faster                                                           |
| xml_etree_parse         | 110 ms                                                                          | 108 ms: 1.02x faster                                                            |
| meteor_contest          | 83.4 ms                                                                         | 82.0 ms: 1.02x faster                                                           |
| sympy_str               | 220 ms                                                                          | 217 ms: 1.02x faster                                                            |
| nbody                   | 98.1 ms                                                                         | 96.9 ms: 1.01x faster                                                           |
| mdp                     | 1.75 sec                                                                        | 1.73 sec: 1.01x faster                                                          |
| async_tree_none         | 241 ms                                                                          | 238 ms: 1.01x faster                                                            |
| tornado_http            | 96.5 ms                                                                         | 95.5 ms: 1.01x faster                                                           |
| regex_dna               | 123 ms                                                                          | 122 ms: 1.01x faster                                                            |
| python_startup          | 24.2 ms                                                                         | 23.9 ms: 1.01x faster                                                           |
| gc_traversal            | 1.46 ms                                                                         | 1.45 ms: 1.01x faster                                                           |
| genshi_xml              | 47.0 ms                                                                         | 46.6 ms: 1.01x faster                                                           |
| sympy_sum               | 111 ms                                                                          | 110 ms: 1.01x faster                                                            |
| coroutines              | 15.2 ms                                                                         | 15.1 ms: 1.01x faster                                                           |
| pidigits                | 199 ms                                                                          | 197 ms: 1.01x faster                                                            |
| bench_mp_pool           | 72.4 ms                                                                         | 71.8 ms: 1.01x faster                                                           |
| async_tree_io_tg        | 551 ms                                                                          | 547 ms: 1.01x faster                                                            |
| pyflate                 | 364 ms                                                                          | 361 ms: 1.01x faster                                                            |
| 2to3                    | 256 ms                                                                          | 255 ms: 1.01x faster                                                            |
| pylint                  | 222 ms                                                                          | 220 ms: 1.01x faster                                                            |
| spectral_norm           | 71.3 ms                                                                         | 71.0 ms: 1.00x faster                                                           |
| scimark_sor             | 97.2 ms                                                                         | 97.4 ms: 1.00x slower                                                           |
| logging_format          | 8.49 us                                                                         | 8.53 us: 1.00x slower                                                           |
| pickle_dict             | 19.8 us                                                                         | 19.8 us: 1.00x slower                                                           |
| sqlite_synth            | 1.93 us                                                                         | 1.95 us: 1.01x slower                                                           |
| scimark_sparse_mat_mult | 3.20 ms                                                                         | 3.23 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed | 486 ms                                                                          | 491 ms: 1.01x slower                                                            |
| pprint_safe_repr        | 740 ms                                                                          | 749 ms: 1.01x slower                                                            |
| deepcopy_reduce         | 2.66 us                                                                         | 2.69 us: 1.01x slower                                                           |
| mako                    | 7.03 ms                                                                         | 7.13 ms: 1.01x slower                                                           |
| pprint_pformat          | 1.51 sec                                                                        | 1.53 sec: 1.01x slower                                                          |
| richards                | 34.3 ms                                                                         | 34.8 ms: 1.01x slower                                                           |
| deepcopy                | 290 us                                                                          | 294 us: 1.01x slower                                                            |
| scimark_fft             | 241 ms                                                                          | 245 ms: 1.02x slower                                                            |
| comprehensions          | 15.4 us                                                                         | 15.6 us: 1.02x slower                                                           |
| scimark_lu              | 86.1 ms                                                                         | 87.5 ms: 1.02x slower                                                           |
| richards_super          | 38.8 ms                                                                         | 39.5 ms: 1.02x slower                                                           |
| deepcopy_memo           | 24.9 us                                                                         | 25.3 us: 1.02x slower                                                           |
| json_loads              | 19.7 us                                                                         | 20.1 us: 1.02x slower                                                           |
| json                    | 4.03 ms                                                                         | 4.12 ms: 1.02x slower                                                           |
| chaos                   | 60.5 ms                                                                         | 61.9 ms: 1.02x slower                                                           |
| crypto_pyaes            | 62.1 ms                                                                         | 63.5 ms: 1.02x slower                                                           |
| unpickle                | 9.82 us                                                                         | 10.2 us: 1.03x slower                                                           |
| fannkuch                | 315 ms                                                                          | 329 ms: 1.05x slower                                                            |
| telco                   | 6.30 ms                                                                         | 6.84 ms: 1.09x slower                                                           |
| Geometric mean          | (ref)                                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (23): async_tree_memoization, async_tree_memoization_tg, regex_effbot, async_tree_none_tg, regex_v8, go, deltablue, float, asyncio_tcp_ssl, logging_simple, generators, typing_runtime_protocols, create_gc_cycles, nqueens, docutils, pickle, hexiom, json_dumps, sympy_integrate, python_startup_no_site, tomli_loads, async_tree_io, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown