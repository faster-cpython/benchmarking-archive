# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-x86
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x slower
- HPT reliability: 71.74%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| docutils       | 1.84 sec                                                                        | 1.80 sec: 1.02x faster                                                           |
| html5lib       | 42.2 ms                                                                         | 43.1 ms: 1.02x slower                                                            |
| tornado_http   | 104 ms                                                                          | 102 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): 2to3, chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization  | 270 ms                                                                          | 275 ms: 1.02x slower                                                             |
| async_tree_none         | 224 ms                                                                          | 228 ms: 1.02x slower                                                             |
| async_tree_cpu_io_mixed | 470 ms                                                                          | 480 ms: 1.02x slower                                                             |
| async_tree_io_tg        | 525 ms                                                                          | 539 ms: 1.03x slower                                                             |
| async_tree_none_tg      | 202 ms                                                                          | 209 ms: 1.03x slower                                                             |
| Geometric mean          | (ref)                                                                           | 1.02x slower                                                                     |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 78.2 ms                                                                         | 80.3 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                     |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 16.7 ms                                                                         | 15.8 ms: 1.06x faster                                                            |
| regex_effbot   | 1.94 ms                                                                         | 1.87 ms: 1.03x faster                                                            |
| regex_compile  | 97.2 ms                                                                         | 96.3 ms: 1.01x faster                                                            |
| regex_dna      | 120 ms                                                                          | 121 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_process  | 43.6 ms                                                                         | 41.8 ms: 1.04x faster                                                            |
| xml_etree_generate | 61.0 ms                                                                         | 58.8 ms: 1.04x faster                                                            |
| tomli_loads        | 1.64 sec                                                                        | 1.58 sec: 1.04x faster                                                           |
| unpickle           | 10.0 us                                                                         | 9.97 us: 1.01x faster                                                            |
| pickle             | 7.83 us                                                                         | 7.90 us: 1.01x slower                                                            |
| pickle_pure_python | 205 us                                                                          | 209 us: 1.02x slower                                                             |
| xml_etree_parse    | 104 ms                                                                          | 106 ms: 1.02x slower                                                             |
| unpickle_list      | 2.81 us                                                                         | 2.90 us: 1.03x slower                                                            |
| Geometric mean     | (ref)                                                                           | 1.00x faster                                                                     |

Benchmark hidden because not significant (6): json_dumps, json_loads, pickle_list, pickle_dict, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 18.7 ms                                                                         | 18.4 ms: 1.01x faster                                                            |
| Geometric mean         | (ref)                                                                           | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 19.2 ms                                                                         | 18.9 ms: 1.02x faster                                                            |
| mako            | 6.88 ms                                                                         | 6.94 ms: 1.01x slower                                                            |
| django_template | 28.9 ms                                                                         | 29.8 ms: 1.03x slower                                                            |
| Geometric mean  | (ref)                                                                           | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240425-pythonperf1_win32-x86-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:-------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8                | 16.7 ms                                                                         | 15.8 ms: 1.06x faster                                                            |
| logging_simple          | 7.50 us                                                                         | 7.12 us: 1.05x faster                                                            |
| raytrace                | 190 ms                                                                          | 182 ms: 1.04x faster                                                             |
| xml_etree_process       | 43.6 ms                                                                         | 41.8 ms: 1.04x faster                                                            |
| spectral_norm           | 70.7 ms                                                                         | 67.9 ms: 1.04x faster                                                            |
| logging_silent          | 58.3 ns                                                                         | 56.1 ns: 1.04x faster                                                            |
| xml_etree_generate      | 61.0 ms                                                                         | 58.8 ms: 1.04x faster                                                            |
| tomli_loads             | 1.64 sec                                                                        | 1.58 sec: 1.04x faster                                                           |
| regex_effbot            | 1.94 ms                                                                         | 1.87 ms: 1.03x faster                                                            |
| telco                   | 6.07 ms                                                                         | 5.87 ms: 1.03x faster                                                            |
| crypto_pyaes            | 56.8 ms                                                                         | 54.9 ms: 1.03x faster                                                            |
| coroutines              | 16.1 ms                                                                         | 15.7 ms: 1.02x faster                                                            |
| scimark_sparse_mat_mult | 3.13 ms                                                                         | 3.06 ms: 1.02x faster                                                            |
| scimark_fft             | 213 ms                                                                          | 208 ms: 1.02x faster                                                             |
| scimark_monte_carlo     | 47.7 ms                                                                         | 46.8 ms: 1.02x faster                                                            |
| sympy_integrate         | 14.5 ms                                                                         | 14.2 ms: 1.02x faster                                                            |
| sqlglot_normalize       | 203 ms                                                                          | 200 ms: 1.02x faster                                                             |
| mdp                     | 1.64 sec                                                                        | 1.61 sec: 1.02x faster                                                           |
| docutils                | 1.84 sec                                                                        | 1.80 sec: 1.02x faster                                                           |
| genshi_text             | 19.2 ms                                                                         | 18.9 ms: 1.02x faster                                                            |
| sqlglot_optimize        | 39.3 ms                                                                         | 38.7 ms: 1.01x faster                                                            |
| sympy_str               | 202 ms                                                                          | 199 ms: 1.01x faster                                                             |
| sympy_expand            | 352 ms                                                                          | 347 ms: 1.01x faster                                                             |
| logging_format          | 7.91 us                                                                         | 7.80 us: 1.01x faster                                                            |
| python_startup_no_site  | 18.7 ms                                                                         | 18.4 ms: 1.01x faster                                                            |
| deltablue               | 2.18 ms                                                                         | 2.16 ms: 1.01x faster                                                            |
| tornado_http            | 104 ms                                                                          | 102 ms: 1.01x faster                                                             |
| scimark_sor             | 80.0 ms                                                                         | 79.1 ms: 1.01x faster                                                            |
| regex_compile           | 97.2 ms                                                                         | 96.3 ms: 1.01x faster                                                            |
| nqueens                 | 68.7 ms                                                                         | 68.2 ms: 1.01x faster                                                            |
| unpickle                | 10.0 us                                                                         | 9.97 us: 1.01x faster                                                            |
| bench_mp_pool           | 70.2 ms                                                                         | 69.8 ms: 1.01x faster                                                            |
| meteor_contest          | 76.5 ms                                                                         | 76.9 ms: 1.00x slower                                                            |
| regex_dna               | 120 ms                                                                          | 121 ms: 1.01x slower                                                             |
| hexiom                  | 4.21 ms                                                                         | 4.24 ms: 1.01x slower                                                            |
| mako                    | 6.88 ms                                                                         | 6.94 ms: 1.01x slower                                                            |
| pickle                  | 7.83 us                                                                         | 7.90 us: 1.01x slower                                                            |
| sympy_sum               | 103 ms                                                                          | 104 ms: 1.01x slower                                                             |
| async_generators        | 286 ms                                                                          | 289 ms: 1.01x slower                                                             |
| go                      | 98.3 ms                                                                         | 99.6 ms: 1.01x slower                                                            |
| gc_traversal            | 1.43 ms                                                                         | 1.45 ms: 1.01x slower                                                            |
| async_tree_memoization  | 270 ms                                                                          | 275 ms: 1.02x slower                                                             |
| comprehensions          | 11.5 us                                                                         | 11.7 us: 1.02x slower                                                            |
| async_tree_none         | 224 ms                                                                          | 228 ms: 1.02x slower                                                             |
| pickle_pure_python      | 205 us                                                                          | 209 us: 1.02x slower                                                             |
| async_tree_cpu_io_mixed | 470 ms                                                                          | 480 ms: 1.02x slower                                                             |
| html5lib                | 42.2 ms                                                                         | 43.1 ms: 1.02x slower                                                            |
| sqlglot_parse           | 888 us                                                                          | 907 us: 1.02x slower                                                             |
| xml_etree_parse         | 104 ms                                                                          | 106 ms: 1.02x slower                                                             |
| chaos                   | 46.4 ms                                                                         | 47.5 ms: 1.02x slower                                                            |
| nbody                   | 78.2 ms                                                                         | 80.3 ms: 1.03x slower                                                            |
| async_tree_io_tg        | 525 ms                                                                          | 539 ms: 1.03x slower                                                             |
| unpickle_list           | 2.81 us                                                                         | 2.90 us: 1.03x slower                                                            |
| deepcopy                | 264 us                                                                          | 272 us: 1.03x slower                                                             |
| django_template         | 28.9 ms                                                                         | 29.8 ms: 1.03x slower                                                            |
| async_tree_none_tg      | 202 ms                                                                          | 209 ms: 1.03x slower                                                             |
| pprint_pformat          | 1.13 sec                                                                        | 1.17 sec: 1.03x slower                                                           |
| pprint_safe_repr        | 556 ms                                                                          | 576 ms: 1.04x slower                                                             |
| deepcopy_memo           | 22.5 us                                                                         | 23.3 us: 1.04x slower                                                            |
| asyncio_tcp             | 809 ms                                                                          | 878 ms: 1.09x slower                                                             |
| deepcopy_reduce         | 2.37 us                                                                         | 2.58 us: 1.09x slower                                                            |
| Geometric mean          | (ref)                                                                           | 1.00x slower                                                                     |

Benchmark hidden because not significant (33): pylint, json_dumps, json_loads, 2to3, json, pickle_list, pickle_dict, thrift, pycparser, xml_etree_iterparse, genshi_xml, generators, create_gc_cycles, asyncio_tcp_ssl, bench_thread_pool, chameleon, richards, unpickle_pure_python, python_startup, fannkuch, pidigits, sqlite_synth, coverage, async_tree_io, float, pathlib, richards_super, typing_runtime_protocols, sqlglot_transpile, scimark_lu, pyflate, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

# HPT report

- Reliability score: 71.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown