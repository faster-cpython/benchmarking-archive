# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.00x faster
- HPT reliability: 99.63%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 297 ms: 1.00x faster                                                      |
| html5lib       | 74.4 ms                                                                      | 73.0 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                              |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 77.2 ms                                                                      | 75.2 ms: 1.03x faster                                                     |
| nbody          | 94.5 ms                                                                      | 103 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                                       | 241 ms: 1.04x faster                                                      |
| regex_effbot   | 3.53 ms                                                                      | 3.54 ms: 1.00x slower                                                     |
| regex_compile  | 146 ms                                                                       | 148 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|---------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_dict         | 32.5 us                                                                      | 30.8 us: 1.06x faster                                                     |
| xml_etree_parse     | 147 ms                                                                       | 142 ms: 1.03x faster                                                      |
| unpickle            | 15.3 us                                                                      | 14.8 us: 1.03x faster                                                     |
| pickle              | 10.6 us                                                                      | 10.3 us: 1.02x faster                                                     |
| xml_etree_iterparse | 102 ms                                                                       | 99.8 ms: 1.02x faster                                                     |
| xml_etree_generate  | 84.8 ms                                                                      | 83.5 ms: 1.02x faster                                                     |
| json_loads          | 25.3 us                                                                      | 25.4 us: 1.01x slower                                                     |
| pickle_pure_python  | 309 us                                                                       | 313 us: 1.01x slower                                                      |
| unpickle_list       | 4.57 us                                                                      | 4.63 us: 1.01x slower                                                     |
| json_dumps          | 10.5 ms                                                                      | 10.6 ms: 1.02x slower                                                     |
| Geometric mean      | (ref)                                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (4): xml_etree_process, unpickle_pure_python, pickle_list, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                              |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml     | 57.1 ms                                                                      | 56.4 ms: 1.01x faster                                                     |
| mako           | 10.00 ms                                                                     | 10.1 ms: 1.01x slower                                                     |
| genshi_text    | 25.7 ms                                                                      | 26.1 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark               | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_dict             | 32.5 us                                                                      | 30.8 us: 1.06x faster                                                     |
| coverage                | 84.2 ms                                                                      | 80.7 ms: 1.04x faster                                                     |
| richards_super          | 54.4 ms                                                                      | 52.3 ms: 1.04x faster                                                     |
| regex_dna               | 249 ms                                                                       | 241 ms: 1.04x faster                                                      |
| xml_etree_parse         | 147 ms                                                                       | 142 ms: 1.03x faster                                                      |
| unpickle                | 15.3 us                                                                      | 14.8 us: 1.03x faster                                                     |
| richards                | 46.9 ms                                                                      | 45.7 ms: 1.03x faster                                                     |
| float                   | 77.2 ms                                                                      | 75.2 ms: 1.03x faster                                                     |
| nqueens                 | 103 ms                                                                       | 100 ms: 1.03x faster                                                      |
| scimark_monte_carlo     | 71.2 ms                                                                      | 69.4 ms: 1.03x faster                                                     |
| pickle                  | 10.6 us                                                                      | 10.3 us: 1.02x faster                                                     |
| pycparser               | 1.27 sec                                                                     | 1.24 sec: 1.02x faster                                                    |
| xml_etree_iterparse     | 102 ms                                                                       | 99.8 ms: 1.02x faster                                                     |
| thrift                  | 897 us                                                                       | 880 us: 1.02x faster                                                      |
| html5lib                | 74.4 ms                                                                      | 73.0 ms: 1.02x faster                                                     |
| scimark_lu              | 120 ms                                                                       | 118 ms: 1.02x faster                                                      |
| deepcopy                | 385 us                                                                       | 379 us: 1.02x faster                                                      |
| xml_etree_generate      | 84.8 ms                                                                      | 83.5 ms: 1.02x faster                                                     |
| sqlglot_parse           | 1.42 ms                                                                      | 1.40 ms: 1.01x faster                                                     |
| genshi_xml              | 57.1 ms                                                                      | 56.4 ms: 1.01x faster                                                     |
| logging_format          | 7.09 us                                                                      | 7.02 us: 1.01x faster                                                     |
| gunicorn                | 1.10 ms                                                                      | 1.09 ms: 1.01x faster                                                     |
| hexiom                  | 7.20 ms                                                                      | 7.13 ms: 1.01x faster                                                     |
| coroutines              | 22.5 ms                                                                      | 22.3 ms: 1.01x faster                                                     |
| sqlite_synth            | 2.70 us                                                                      | 2.68 us: 1.01x faster                                                     |
| asyncio_tcp             | 375 ms                                                                       | 372 ms: 1.01x faster                                                      |
| dulwich_log             | 68.2 ms                                                                      | 67.7 ms: 1.01x faster                                                     |
| sqlglot_transpile       | 1.81 ms                                                                      | 1.80 ms: 1.00x faster                                                     |
| 2to3                    | 298 ms                                                                       | 297 ms: 1.00x faster                                                      |
| python_startup_no_site  | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                     |
| regex_effbot            | 3.53 ms                                                                      | 3.54 ms: 1.00x slower                                                     |
| mdp                     | 2.63 sec                                                                     | 2.63 sec: 1.00x slower                                                    |
| gc_traversal            | 4.42 ms                                                                      | 4.44 ms: 1.00x slower                                                     |
| json_loads              | 25.3 us                                                                      | 25.4 us: 1.01x slower                                                     |
| sympy_str               | 308 ms                                                                       | 310 ms: 1.01x slower                                                      |
| pylint                  | 333 ms                                                                       | 335 ms: 1.01x slower                                                      |
| fannkuch                | 391 ms                                                                       | 393 ms: 1.01x slower                                                      |
| go                      | 176 ms                                                                       | 177 ms: 1.01x slower                                                      |
| create_gc_cycles        | 1.86 ms                                                                      | 1.87 ms: 1.01x slower                                                     |
| regex_compile           | 146 ms                                                                       | 148 ms: 1.01x slower                                                      |
| sqlglot_optimize        | 62.3 ms                                                                      | 62.9 ms: 1.01x slower                                                     |
| deepcopy_reduce         | 3.39 us                                                                      | 3.43 us: 1.01x slower                                                     |
| sympy_integrate         | 25.1 ms                                                                      | 25.4 ms: 1.01x slower                                                     |
| spectral_norm           | 92.3 ms                                                                      | 93.4 ms: 1.01x slower                                                     |
| comprehensions          | 19.0 us                                                                      | 19.3 us: 1.01x slower                                                     |
| pyflate                 | 498 ms                                                                       | 504 ms: 1.01x slower                                                      |
| generators              | 33.0 ms                                                                      | 33.4 ms: 1.01x slower                                                     |
| pickle_pure_python      | 309 us                                                                       | 313 us: 1.01x slower                                                      |
| mako                    | 10.00 ms                                                                     | 10.1 ms: 1.01x slower                                                     |
| unpickle_list           | 4.57 us                                                                      | 4.63 us: 1.01x slower                                                     |
| genshi_text             | 25.7 ms                                                                      | 26.1 ms: 1.01x slower                                                     |
| scimark_sor             | 150 ms                                                                       | 152 ms: 1.01x slower                                                      |
| sympy_sum               | 163 ms                                                                       | 165 ms: 1.01x slower                                                      |
| json_dumps              | 10.5 ms                                                                      | 10.6 ms: 1.02x slower                                                     |
| async_generators        | 376 ms                                                                       | 383 ms: 1.02x slower                                                      |
| scimark_fft             | 313 ms                                                                       | 319 ms: 1.02x slower                                                      |
| aiohttp                 | 1.11 ms                                                                      | 1.13 ms: 1.02x slower                                                     |
| sqlglot_normalize       | 121 ms                                                                       | 123 ms: 1.02x slower                                                      |
| telco                   | 8.09 ms                                                                      | 8.29 ms: 1.02x slower                                                     |
| bench_mp_pool           | 4.62 ms                                                                      | 4.74 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult | 4.13 ms                                                                      | 4.24 ms: 1.03x slower                                                     |
| bench_thread_pool       | 926 us                                                                       | 951 us: 1.03x slower                                                      |
| nbody                   | 94.5 ms                                                                      | 103 ms: 1.09x slower                                                      |
| Geometric mean          | (ref)                                                                        | 1.00x faster                                                              |

Benchmark hidden because not significant (36): raytrace, chaos, typing_runtime_protocols, logging_silent, pprint_pformat, tornado_http, xml_etree_process, logging_simple, deepcopy_memo, pathlib, sympy_expand, pidigits, json, python_startup, async_tree_none, asyncio_tcp_ssl, unpickle_pure_python, chameleon, docutils, pickle_list, meteor_contest, deltablue, mypy2, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, tomli_loads, pprint_safe_repr, crypto_pyaes, async_tree_none_tg, asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_memoization_tg, dask, async_tree_memoization, regex_v8

# HPT report

- Reliability score: 99.63% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x