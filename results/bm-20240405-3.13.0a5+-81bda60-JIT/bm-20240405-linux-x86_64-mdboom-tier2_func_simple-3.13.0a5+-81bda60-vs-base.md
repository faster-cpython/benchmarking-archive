# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.00x slower
- HPT reliability: 91.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 279 ms: 1.00x slower                                                |
| docutils       | 2.92 sec                                                               | 2.94 sec: 1.00x slower                                              |
| html5lib       | 66.7 ms                                                                | 68.7 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 189 ms                                                                 | 193 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                 | 144 ms: 1.01x slower                                                |
| regex_v8       | 25.0 ms                                                                | 25.5 ms: 1.02x slower                                               |
| regex_dna      | 225 ms                                                                 | 230 ms: 1.02x slower                                                |
| regex_effbot   | 3.73 ms                                                                | 3.86 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle             | 17.4 us                                                                | 16.1 us: 1.08x faster                                               |
| unpickle_list        | 5.31 us                                                                | 5.12 us: 1.04x faster                                               |
| tomli_loads          | 2.05 sec                                                               | 2.03 sec: 1.01x faster                                              |
| json_loads           | 28.4 us                                                                | 28.2 us: 1.01x faster                                               |
| pickle               | 11.7 us                                                                | 11.6 us: 1.00x faster                                               |
| pickle_pure_python   | 308 us                                                                 | 306 us: 1.00x faster                                                |
| pickle_dict          | 34.2 us                                                                | 34.1 us: 1.00x faster                                               |
| unpickle_pure_python | 242 us                                                                 | 241 us: 1.00x faster                                                |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (6): xml_etree_process, xml_etree_generate, xml_etree_parse, xml_etree_iterparse, json_dumps, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                               |
| python_startup_no_site | 9.52 ms                                                                | 9.45 ms: 1.01x faster                                               |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml     | 54.5 ms                                                                | 54.1 ms: 1.01x faster                                               |
| mako           | 10.7 ms                                                                | 10.7 ms: 1.00x slower                                               |
| genshi_text    | 24.7 ms                                                                | 25.2 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                        |

All benchmarks:
===============

| Benchmark               | bm-20240405-linux-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle                | 17.4 us                                                                | 16.1 us: 1.08x faster                                               |
| gc_traversal            | 4.04 ms                                                                | 3.77 ms: 1.07x faster                                               |
| unpickle_list           | 5.31 us                                                                | 5.12 us: 1.04x faster                                               |
| logging_simple          | 5.94 us                                                                | 5.83 us: 1.02x faster                                               |
| pyflate                 | 476 ms                                                                 | 468 ms: 1.02x faster                                                |
| scimark_sparse_mat_mult | 5.02 ms                                                                | 4.94 ms: 1.02x faster                                               |
| deepcopy_memo           | 39.5 us                                                                | 39.0 us: 1.01x faster                                               |
| fannkuch                | 398 ms                                                                 | 393 ms: 1.01x faster                                                |
| tomli_loads             | 2.05 sec                                                               | 2.03 sec: 1.01x faster                                              |
| scimark_fft             | 345 ms                                                                 | 341 ms: 1.01x faster                                                |
| logging_format          | 6.49 us                                                                | 6.42 us: 1.01x faster                                               |
| pathlib                 | 19.2 ms                                                                | 19.0 ms: 1.01x faster                                               |
| deepcopy                | 366 us                                                                 | 363 us: 1.01x faster                                                |
| create_gc_cycles        | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                               |
| python_startup          | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                               |
| python_startup_no_site  | 9.52 ms                                                                | 9.45 ms: 1.01x faster                                               |
| comprehensions          | 18.0 us                                                                | 17.9 us: 1.01x faster                                               |
| json_loads              | 28.4 us                                                                | 28.2 us: 1.01x faster                                               |
| genshi_xml              | 54.5 ms                                                                | 54.1 ms: 1.01x faster                                               |
| scimark_lu              | 133 ms                                                                 | 132 ms: 1.01x faster                                                |
| pickle                  | 11.7 us                                                                | 11.6 us: 1.00x faster                                               |
| pickle_pure_python      | 308 us                                                                 | 306 us: 1.00x faster                                                |
| pickle_dict             | 34.2 us                                                                | 34.1 us: 1.00x faster                                               |
| unpickle_pure_python    | 242 us                                                                 | 241 us: 1.00x faster                                                |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.86 sec: 1.00x faster                                              |
| mako                    | 10.7 ms                                                                | 10.7 ms: 1.00x slower                                               |
| docutils                | 2.92 sec                                                               | 2.94 sec: 1.00x slower                                              |
| 2to3                    | 278 ms                                                                 | 279 ms: 1.00x slower                                                |
| sympy_str               | 296 ms                                                                 | 297 ms: 1.00x slower                                                |
| async_generators        | 458 ms                                                                 | 461 ms: 1.00x slower                                                |
| sympy_expand            | 494 ms                                                                 | 496 ms: 1.00x slower                                                |
| chaos                   | 62.3 ms                                                                | 62.6 ms: 1.01x slower                                               |
| sympy_integrate         | 22.0 ms                                                                | 22.1 ms: 1.01x slower                                               |
| nqueens                 | 89.8 ms                                                                | 90.5 ms: 1.01x slower                                               |
| raytrace                | 273 ms                                                                 | 275 ms: 1.01x slower                                                |
| go                      | 154 ms                                                                 | 155 ms: 1.01x slower                                                |
| meteor_contest          | 110 ms                                                                 | 111 ms: 1.01x slower                                                |
| regex_compile           | 143 ms                                                                 | 144 ms: 1.01x slower                                                |
| coverage                | 97.8 ms                                                                | 98.9 ms: 1.01x slower                                               |
| richards                | 43.6 ms                                                                | 44.2 ms: 1.01x slower                                               |
| json                    | 5.29 ms                                                                | 5.36 ms: 1.01x slower                                               |
| richards_super          | 49.5 ms                                                                | 50.3 ms: 1.02x slower                                               |
| pidigits                | 189 ms                                                                 | 193 ms: 1.02x slower                                                |
| regex_v8                | 25.0 ms                                                                | 25.5 ms: 1.02x slower                                               |
| genshi_text             | 24.7 ms                                                                | 25.2 ms: 1.02x slower                                               |
| coroutines              | 22.2 ms                                                                | 22.6 ms: 1.02x slower                                               |
| regex_dna               | 225 ms                                                                 | 230 ms: 1.02x slower                                                |
| pprint_safe_repr        | 743 ms                                                                 | 762 ms: 1.03x slower                                                |
| html5lib                | 66.7 ms                                                                | 68.7 ms: 1.03x slower                                               |
| pycparser               | 1.18 sec                                                               | 1.22 sec: 1.03x slower                                              |
| regex_effbot            | 3.73 ms                                                                | 3.86 ms: 1.03x slower                                               |
| pprint_pformat          | 1.52 sec                                                               | 1.59 sec: 1.05x slower                                              |
| logging_silent          | 100 ns                                                                 | 106 ns: 1.06x slower                                                |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (46): async_tree_cpu_io_mixed_tg, chameleon, async_tree_cpu_io_mixed, float, dask, gunicorn, tornado_http, xml_etree_process, scimark_sor, sqlite_synth, spectral_norm, bench_mp_pool, deltablue, xml_etree_generate, deepcopy_reduce, typing_runtime_protocols, asyncio_websockets, async_tree_memoization, dulwich_log, pylint, asyncio_tcp, sqlglot_parse, mdp, sqlglot_transpile, generators, sympy_sum, sqlglot_normalize, bench_thread_pool, xml_etree_parse, mypy2, xml_etree_iterparse, sqlglot_optimize, aiohttp, thrift, hexiom, telco, json_dumps, async_tree_none, async_tree_memoization_tg, pickle_list, async_tree_io, crypto_pyaes, nbody, async_tree_none_tg, async_tree_io_tg, scimark_monte_carlo

# HPT report

- Reliability score: 91.71% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x