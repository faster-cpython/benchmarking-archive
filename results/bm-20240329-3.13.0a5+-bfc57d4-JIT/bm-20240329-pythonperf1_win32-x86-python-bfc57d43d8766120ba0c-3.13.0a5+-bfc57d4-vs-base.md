# Results vs. base

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.00x faster
- HPT reliability: 93.83%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                          | 255 ms: 1.01x faster                                                            |
| chameleon      | 6.17 ms                                                                         | 6.13 ms: 1.01x faster                                                           |
| html5lib       | 46.5 ms                                                                         | 46.0 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 207 ms                                                                          | 209 ms: 1.01x slower                                                            |
| async_tree_cpu_io_mixed    | 472 ms                                                                          | 481 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed_tg | 451 ms                                                                          | 468 ms: 1.04x slower                                                            |
| Geometric mean             | (ref)                                                                           | 1.00x slower                                                                    |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_none, async_tree_io, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                          | 198 ms: 1.01x faster                                                            |
| nbody          | 95.8 ms                                                                         | 98.8 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 120 ms                                                                          | 125 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 180 us                                                                          | 171 us: 1.05x faster                                                            |
| json_dumps           | 6.93 ms                                                                         | 6.78 ms: 1.02x faster                                                           |
| unpickle_list        | 2.85 us                                                                         | 2.80 us: 1.02x faster                                                           |
| unpickle             | 10.0 us                                                                         | 9.88 us: 1.02x faster                                                           |
| xml_etree_generate   | 62.4 ms                                                                         | 61.7 ms: 1.01x faster                                                           |
| xml_etree_process    | 43.7 ms                                                                         | 43.4 ms: 1.01x faster                                                           |
| tomli_loads          | 1.73 sec                                                                        | 1.72 sec: 1.01x faster                                                          |
| xml_etree_parse      | 107 ms                                                                          | 108 ms: 1.01x slower                                                            |
| json_loads           | 19.9 us                                                                         | 20.3 us: 1.02x slower                                                           |
| pickle               | 7.98 us                                                                         | 8.18 us: 1.03x slower                                                           |
| pickle_pure_python   | 220 us                                                                          | 227 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 24.3 ms                                                                         | 24.4 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                                           | 1.00x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 21.2 ms                                                                         | 20.1 ms: 1.05x faster                                                           |
| genshi_xml      | 48.6 ms                                                                         | 47.7 ms: 1.02x faster                                                           |
| django_template | 33.4 ms                                                                         | 33.2 ms: 1.01x faster                                                           |
| mako            | 7.10 ms                                                                         | 7.24 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                                           | 1.02x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpack_sequence            | 46.6 ns                                                                         | 44.0 ns: 1.06x faster                                                           |
| genshi_text                | 21.2 ms                                                                         | 20.1 ms: 1.05x faster                                                           |
| unpickle_pure_python       | 180 us                                                                          | 171 us: 1.05x faster                                                            |
| raytrace                   | 273 ms                                                                          | 260 ms: 1.05x faster                                                            |
| meteor_contest             | 83.9 ms                                                                         | 81.2 ms: 1.03x faster                                                           |
| telco                      | 6.50 ms                                                                         | 6.33 ms: 1.03x faster                                                           |
| json_dumps                 | 6.93 ms                                                                         | 6.78 ms: 1.02x faster                                                           |
| chaos                      | 63.1 ms                                                                         | 61.8 ms: 1.02x faster                                                           |
| genshi_xml                 | 48.6 ms                                                                         | 47.7 ms: 1.02x faster                                                           |
| fannkuch                   | 319 ms                                                                          | 313 ms: 1.02x faster                                                            |
| comprehensions             | 15.6 us                                                                         | 15.3 us: 1.02x faster                                                           |
| unpickle_list              | 2.85 us                                                                         | 2.80 us: 1.02x faster                                                           |
| unpickle                   | 10.0 us                                                                         | 9.88 us: 1.02x faster                                                           |
| deepcopy                   | 300 us                                                                          | 295 us: 1.02x faster                                                            |
| pprint_pformat             | 1.51 sec                                                                        | 1.49 sec: 1.01x faster                                                          |
| sqlglot_normalize          | 241 ms                                                                          | 238 ms: 1.01x faster                                                            |
| html5lib                   | 46.5 ms                                                                         | 46.0 ms: 1.01x faster                                                           |
| sqlglot_parse              | 1.01 ms                                                                         | 996 us: 1.01x faster                                                            |
| coverage                   | 487 ms                                                                          | 482 ms: 1.01x faster                                                            |
| xml_etree_generate         | 62.4 ms                                                                         | 61.7 ms: 1.01x faster                                                           |
| deltablue                  | 2.62 ms                                                                         | 2.59 ms: 1.01x faster                                                           |
| sympy_expand               | 381 ms                                                                          | 378 ms: 1.01x faster                                                            |
| 2to3                       | 257 ms                                                                          | 255 ms: 1.01x faster                                                            |
| gc_traversal               | 1.43 ms                                                                         | 1.42 ms: 1.01x faster                                                           |
| scimark_sor                | 100.0 ms                                                                        | 99.1 ms: 1.01x faster                                                           |
| go                         | 123 ms                                                                          | 122 ms: 1.01x faster                                                            |
| django_template            | 33.4 ms                                                                         | 33.2 ms: 1.01x faster                                                           |
| chameleon                  | 6.17 ms                                                                         | 6.13 ms: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                                          | 198 ms: 1.01x faster                                                            |
| generators                 | 23.1 ms                                                                         | 23.0 ms: 1.01x faster                                                           |
| sympy_integrate            | 16.4 ms                                                                         | 16.3 ms: 1.01x faster                                                           |
| xml_etree_process          | 43.7 ms                                                                         | 43.4 ms: 1.01x faster                                                           |
| hexiom                     | 6.28 ms                                                                         | 6.24 ms: 1.01x faster                                                           |
| tomli_loads                | 1.73 sec                                                                        | 1.72 sec: 1.01x faster                                                          |
| sqlglot_optimize           | 46.5 ms                                                                         | 46.3 ms: 1.01x faster                                                           |
| sympy_sum                  | 110 ms                                                                          | 109 ms: 1.00x faster                                                            |
| mdp                        | 1.78 sec                                                                        | 1.78 sec: 1.00x faster                                                          |
| coroutines                 | 14.7 ms                                                                         | 14.8 ms: 1.00x slower                                                           |
| sqlite_synth               | 1.94 us                                                                         | 1.95 us: 1.00x slower                                                           |
| python_startup             | 24.3 ms                                                                         | 24.4 ms: 1.01x slower                                                           |
| logging_silent             | 60.3 ns                                                                         | 60.7 ns: 1.01x slower                                                           |
| nqueens                    | 92.1 ms                                                                         | 93.0 ms: 1.01x slower                                                           |
| richards_super             | 40.2 ms                                                                         | 40.6 ms: 1.01x slower                                                           |
| async_tree_none_tg         | 207 ms                                                                          | 209 ms: 1.01x slower                                                            |
| xml_etree_parse            | 107 ms                                                                          | 108 ms: 1.01x slower                                                            |
| richards                   | 35.6 ms                                                                         | 36.1 ms: 1.01x slower                                                           |
| scimark_monte_carlo        | 61.5 ms                                                                         | 62.4 ms: 1.01x slower                                                           |
| typing_runtime_protocols   | 96.5 us                                                                         | 98.2 us: 1.02x slower                                                           |
| async_tree_cpu_io_mixed    | 472 ms                                                                          | 481 ms: 1.02x slower                                                            |
| json_loads                 | 19.9 us                                                                         | 20.3 us: 1.02x slower                                                           |
| mako                       | 7.10 ms                                                                         | 7.24 ms: 1.02x slower                                                           |
| pickle                     | 7.98 us                                                                         | 8.18 us: 1.03x slower                                                           |
| logging_format             | 8.81 us                                                                         | 9.05 us: 1.03x slower                                                           |
| logging_simple             | 8.24 us                                                                         | 8.50 us: 1.03x slower                                                           |
| nbody                      | 95.8 ms                                                                         | 98.8 ms: 1.03x slower                                                           |
| pickle_pure_python         | 220 us                                                                          | 227 us: 1.03x slower                                                            |
| async_generators           | 285 ms                                                                          | 295 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed_tg | 451 ms                                                                          | 468 ms: 1.04x slower                                                            |
| scimark_lu                 | 93.0 ms                                                                         | 96.7 ms: 1.04x slower                                                           |
| regex_dna                  | 120 ms                                                                          | 125 ms: 1.04x slower                                                            |
| scimark_fft                | 237 ms                                                                          | 247 ms: 1.04x slower                                                            |
| asyncio_tcp                | 604 ms                                                                          | 632 ms: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                                           | 1.00x faster                                                                    |

Benchmark hidden because not significant (33): async_tree_memoization, async_tree_none, async_tree_io, float, deepcopy_reduce, async_tree_io_tg, pathlib, sympy_str, asyncio_tcp_ssl, regex_compile, pycparser, scimark_sparse_mat_mult, regex_v8, pyflate, pickle_list, pprint_safe_repr, sqlglot_transpile, python_startup_no_site, xml_etree_iterparse, pickle_dict, spectral_norm, bench_mp_pool, bench_thread_pool, pylint, async_tree_memoization_tg, regex_effbot, crypto_pyaes, create_gc_cycles, tornado_http, thrift, deepcopy_memo, docutils, json

# HPT report

- Reliability score: 93.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown