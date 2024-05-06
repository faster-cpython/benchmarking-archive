# Results vs. base

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: 17ed8bc
- commit date: 2024-04-05
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 269 ms: 1.01x slower                                                          |
| chameleon      | 6.92 ms                                                                | 6.99 ms: 1.01x slower                                                         |
| docutils       | 2.77 sec                                                               | 2.81 sec: 1.01x slower                                                        |
| tornado_http   | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 191 ms: 1.00x slower                                                          |
| float          | 78.7 ms                                                                | 81.0 ms: 1.03x slower                                                         |
| nbody          | 88.5 ms                                                                | 116 ms: 1.31x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 134 ms                                                                 | 136 ms: 1.02x slower                                                          |
| regex_v8       | 25.5 ms                                                                | 26.1 ms: 1.02x slower                                                         |
| regex_dna      | 224 ms                                                                 | 232 ms: 1.03x slower                                                          |
| regex_effbot   | 3.72 ms                                                                | 3.87 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_dict          | 35.4 us                                                                | 34.5 us: 1.03x faster                                                         |
| json_dumps           | 10.7 ms                                                                | 10.5 ms: 1.01x faster                                                         |
| pickle_list          | 5.33 us                                                                | 5.26 us: 1.01x faster                                                         |
| unpickle_pure_python | 218 us                                                                 | 217 us: 1.00x faster                                                          |
| unpickle             | 15.4 us                                                                | 15.8 us: 1.03x slower                                                         |
| tomli_loads          | 2.15 sec                                                               | 2.25 sec: 1.05x slower                                                        |
| unpickle_list        | 4.97 us                                                                | 5.27 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (7): xml_etree_process, xml_etree_parse, json_loads, pickle_pure_python, pickle, xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 9.02 ms: 1.00x slower                                                         |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text    | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark               | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal            | 3.94 ms                                                                | 3.80 ms: 1.04x faster                                                         |
| pickle_dict             | 35.4 us                                                                | 34.5 us: 1.03x faster                                                         |
| genshi_text             | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                         |
| json_dumps              | 10.7 ms                                                                | 10.5 ms: 1.01x faster                                                         |
| pickle_list             | 5.33 us                                                                | 5.26 us: 1.01x faster                                                         |
| json                    | 5.47 ms                                                                | 5.39 ms: 1.01x faster                                                         |
| hexiom                  | 6.21 ms                                                                | 6.15 ms: 1.01x faster                                                         |
| unpickle_pure_python    | 218 us                                                                 | 217 us: 1.00x faster                                                          |
| pidigits                | 191 ms                                                                 | 191 ms: 1.00x slower                                                          |
| python_startup_no_site  | 9.00 ms                                                                | 9.02 ms: 1.00x slower                                                         |
| bench_thread_pool       | 826 us                                                                 | 828 us: 1.00x slower                                                          |
| pylint                  | 277 ms                                                                 | 279 ms: 1.00x slower                                                          |
| pprint_safe_repr        | 734 ms                                                                 | 737 ms: 1.00x slower                                                          |
| thrift                  | 799 us                                                                 | 804 us: 1.01x slower                                                          |
| python_startup          | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| asyncio_tcp             | 505 ms                                                                 | 508 ms: 1.01x slower                                                          |
| gunicorn                | 1.26 ms                                                                | 1.27 ms: 1.01x slower                                                         |
| deepcopy_reduce         | 3.17 us                                                                | 3.20 us: 1.01x slower                                                         |
| tornado_http            | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| async_generators        | 441 ms                                                                 | 444 ms: 1.01x slower                                                          |
| deepcopy_memo           | 37.8 us                                                                | 38.1 us: 1.01x slower                                                         |
| pprint_pformat          | 1.50 sec                                                               | 1.51 sec: 1.01x slower                                                        |
| 2to3                    | 267 ms                                                                 | 269 ms: 1.01x slower                                                          |
| dulwich_log             | 67.0 ms                                                                | 67.6 ms: 1.01x slower                                                         |
| chameleon               | 6.92 ms                                                                | 6.99 ms: 1.01x slower                                                         |
| sqlglot_optimize        | 54.4 ms                                                                | 54.9 ms: 1.01x slower                                                         |
| aiohttp                 | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                         |
| sqlglot_transpile       | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                                         |
| sqlglot_normalize       | 109 ms                                                                 | 110 ms: 1.01x slower                                                          |
| docutils                | 2.77 sec                                                               | 2.81 sec: 1.01x slower                                                        |
| regex_compile           | 134 ms                                                                 | 136 ms: 1.02x slower                                                          |
| sympy_sum               | 153 ms                                                                 | 156 ms: 1.02x slower                                                          |
| sympy_str               | 275 ms                                                                 | 280 ms: 1.02x slower                                                          |
| fannkuch                | 397 ms                                                                 | 404 ms: 1.02x slower                                                          |
| pathlib                 | 18.8 ms                                                                | 19.1 ms: 1.02x slower                                                         |
| coverage                | 96.9 ms                                                                | 98.6 ms: 1.02x slower                                                         |
| logging_simple          | 5.67 us                                                                | 5.78 us: 1.02x slower                                                         |
| sympy_integrate         | 20.0 ms                                                                | 20.4 ms: 1.02x slower                                                         |
| comprehensions          | 16.3 us                                                                | 16.7 us: 1.02x slower                                                         |
| sympy_expand            | 462 ms                                                                 | 471 ms: 1.02x slower                                                          |
| mdp                     | 2.73 sec                                                               | 2.79 sec: 1.02x slower                                                        |
| deltablue               | 3.14 ms                                                                | 3.21 ms: 1.02x slower                                                         |
| regex_v8                | 25.5 ms                                                                | 26.1 ms: 1.02x slower                                                         |
| sqlglot_parse           | 1.27 ms                                                                | 1.30 ms: 1.02x slower                                                         |
| go                      | 141 ms                                                                 | 145 ms: 1.02x slower                                                          |
| richards_super          | 51.6 ms                                                                | 52.9 ms: 1.03x slower                                                         |
| unpickle                | 15.4 us                                                                | 15.8 us: 1.03x slower                                                         |
| telco                   | 8.41 ms                                                                | 8.63 ms: 1.03x slower                                                         |
| float                   | 78.7 ms                                                                | 81.0 ms: 1.03x slower                                                         |
| logging_format          | 6.26 us                                                                | 6.44 us: 1.03x slower                                                         |
| richards                | 45.5 ms                                                                | 46.8 ms: 1.03x slower                                                         |
| regex_dna               | 224 ms                                                                 | 232 ms: 1.03x slower                                                          |
| nqueens                 | 80.6 ms                                                                | 83.5 ms: 1.04x slower                                                         |
| scimark_lu              | 112 ms                                                                 | 117 ms: 1.04x slower                                                          |
| scimark_sor             | 129 ms                                                                 | 134 ms: 1.04x slower                                                          |
| regex_effbot            | 3.72 ms                                                                | 3.87 ms: 1.04x slower                                                         |
| coroutines              | 23.1 ms                                                                | 24.0 ms: 1.04x slower                                                         |
| pyflate                 | 461 ms                                                                 | 482 ms: 1.05x slower                                                          |
| tomli_loads             | 2.15 sec                                                               | 2.25 sec: 1.05x slower                                                        |
| unpickle_list           | 4.97 us                                                                | 5.27 us: 1.06x slower                                                         |
| scimark_monte_carlo     | 67.7 ms                                                                | 72.8 ms: 1.08x slower                                                         |
| raytrace                | 258 ms                                                                 | 278 ms: 1.08x slower                                                          |
| chaos                   | 59.9 ms                                                                | 67.8 ms: 1.13x slower                                                         |
| scimark_sparse_mat_mult | 4.99 ms                                                                | 5.74 ms: 1.15x slower                                                         |
| scimark_fft             | 359 ms                                                                 | 419 ms: 1.17x slower                                                          |
| spectral_norm           | 110 ms                                                                 | 135 ms: 1.23x slower                                                          |
| nbody                   | 88.5 ms                                                                | 116 ms: 1.31x slower                                                          |
| Geometric mean          | (ref)                                                                  | 1.02x slower                                                                  |

Benchmark hidden because not significant (32): xml_etree_process, xml_etree_parse, typing_runtime_protocols, genshi_xml, html5lib, meteor_contest, json_loads, create_gc_cycles, async_tree_io, asyncio_websockets, crypto_pyaes, dask, pickle_pure_python, pickle, async_tree_memoization_tg, xml_etree_generate, bench_mp_pool, asyncio_tcp_ssl, async_tree_io_tg, xml_etree_iterparse, async_tree_memoization, mako, async_tree_none_tg, generators, async_tree_cpu_io_mixed_tg, logging_silent, async_tree_cpu_io_mixed, sqlite_synth, deepcopy, async_tree_none, mypy2, pycparser

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x