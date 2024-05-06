# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: darwin-arm64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.00x faster
- HPT reliability: 55.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| chameleon      | 4.51 ms                                                                | 4.46 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                   |
| async_tree_eager_tg              | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                                  |
| async_tree_eager                 | 64.1 ms                                                                | 65.1 ms: 1.02x slower                                                  |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (13): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed, async_tree_none, async_tree_memoization, async_tree_eager_memoization, async_tree_io, async_tree_none_tg, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.68 ms                                                                | 2.64 ms: 1.02x faster                                                  |
| regex_compile  | 85.8 ms                                                                | 85.3 ms: 1.01x faster                                                  |
| regex_v8       | 17.2 ms                                                                | 17.1 ms: 1.00x faster                                                  |
| regex_dna      | 152 ms                                                                 | 152 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                                 | 98.5 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 72.1 ms                                                                | 68.5 ms: 1.05x faster                                                  |
| pickle               | 7.50 us                                                                | 7.25 us: 1.03x faster                                                  |
| unpickle_list        | 3.06 us                                                                | 2.99 us: 1.02x faster                                                  |
| pickle_dict          | 18.2 us                                                                | 18.1 us: 1.00x faster                                                  |
| xml_etree_process    | 37.1 ms                                                                | 37.3 ms: 1.00x slower                                                  |
| unpickle_pure_python | 140 us                                                                 | 141 us: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (7): unpickle, json_dumps, xml_etree_generate, pickle_pure_python, json_loads, tomli_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 13.4 ms                                                                | 13.3 ms: 1.00x faster                                                  |
| python_startup_no_site | 11.6 ms                                                                | 11.6 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 6.95 ms                                                                | 6.93 ms: 1.00x faster                                                  |
| genshi_text    | 14.7 ms                                                                | 14.7 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse                  | 106 ms                                                                 | 98.5 ms: 1.08x faster                                                  |
| xml_etree_iterparse              | 72.1 ms                                                                | 68.5 ms: 1.05x faster                                                  |
| pickle                           | 7.50 us                                                                | 7.25 us: 1.03x faster                                                  |
| unpickle_list                    | 3.06 us                                                                | 2.99 us: 1.02x faster                                                  |
| regex_effbot                     | 2.68 ms                                                                | 2.64 ms: 1.02x faster                                                  |
| coroutines                       | 17.1 ms                                                                | 16.8 ms: 1.02x faster                                                  |
| pprint_pformat                   | 1000 ms                                                                | 987 ms: 1.01x faster                                                   |
| chameleon                        | 4.51 ms                                                                | 4.46 ms: 1.01x faster                                                  |
| richards                         | 29.6 ms                                                                | 29.3 ms: 1.01x faster                                                  |
| pylint                           | 153 ms                                                                 | 152 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 492 ms                                                                 | 488 ms: 1.01x faster                                                   |
| richards_super                   | 33.1 ms                                                                | 32.8 ms: 1.01x faster                                                  |
| pyflate                          | 317 ms                                                                 | 315 ms: 1.01x faster                                                   |
| regex_compile                    | 85.8 ms                                                                | 85.3 ms: 1.01x faster                                                  |
| deepcopy                         | 211 us                                                                 | 209 us: 1.01x faster                                                   |
| telco                            | 4.63 ms                                                                | 4.60 ms: 1.01x faster                                                  |
| regex_v8                         | 17.2 ms                                                                | 17.1 ms: 1.00x faster                                                  |
| pickle_dict                      | 18.2 us                                                                | 18.1 us: 1.00x faster                                                  |
| bench_thread_pool                | 489 us                                                                 | 487 us: 1.00x faster                                                   |
| logging_silent                   | 63.9 ns                                                                | 63.6 ns: 1.00x faster                                                  |
| mako                             | 6.95 ms                                                                | 6.93 ms: 1.00x faster                                                  |
| nqueens                          | 60.5 ms                                                                | 60.3 ms: 1.00x faster                                                  |
| sqlglot_normalize                | 176 ms                                                                 | 175 ms: 1.00x faster                                                   |
| go                               | 107 ms                                                                 | 106 ms: 1.00x faster                                                   |
| generators                       | 26.1 ms                                                                | 26.0 ms: 1.00x faster                                                  |
| scimark_lu                       | 82.1 ms                                                                | 82.0 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                                 | 408 ms: 1.00x faster                                                   |
| python_startup                   | 13.4 ms                                                                | 13.3 ms: 1.00x faster                                                  |
| sqlglot_optimize                 | 33.6 ms                                                                | 33.6 ms: 1.00x faster                                                  |
| sympy_expand                     | 238 ms                                                                 | 237 ms: 1.00x faster                                                   |
| python_startup_no_site           | 11.6 ms                                                                | 11.6 ms: 1.00x faster                                                  |
| regex_dna                        | 152 ms                                                                 | 152 ms: 1.00x slower                                                   |
| mdp                              | 1.58 sec                                                               | 1.58 sec: 1.00x slower                                                 |
| comprehensions                   | 11.9 us                                                                | 12.0 us: 1.00x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                   |
| crypto_pyaes                     | 46.3 ms                                                                | 46.4 ms: 1.00x slower                                                  |
| chaos                            | 37.9 ms                                                                | 38.0 ms: 1.00x slower                                                  |
| dulwich_log                      | 28.7 ms                                                                | 28.8 ms: 1.00x slower                                                  |
| logging_simple                   | 3.13 us                                                                | 3.14 us: 1.00x slower                                                  |
| xml_etree_process                | 37.1 ms                                                                | 37.3 ms: 1.00x slower                                                  |
| scimark_sparse_mat_mult          | 3.12 ms                                                                | 3.14 ms: 1.00x slower                                                  |
| genshi_text                      | 14.7 ms                                                                | 14.7 ms: 1.00x slower                                                  |
| deepcopy_reduce                  | 1.86 us                                                                | 1.86 us: 1.00x slower                                                  |
| scimark_sor                      | 106 ms                                                                 | 106 ms: 1.00x slower                                                   |
| sqlglot_parse                    | 766 us                                                                 | 770 us: 1.01x slower                                                   |
| scimark_monte_carlo              | 43.2 ms                                                                | 43.4 ms: 1.01x slower                                                  |
| sqlglot_transpile                | 937 us                                                                 | 943 us: 1.01x slower                                                   |
| unpickle_pure_python             | 140 us                                                                 | 141 us: 1.01x slower                                                   |
| create_gc_cycles                 | 892 us                                                                 | 898 us: 1.01x slower                                                   |
| coverage                         | 46.0 ms                                                                | 46.4 ms: 1.01x slower                                                  |
| fannkuch                         | 258 ms                                                                 | 260 ms: 1.01x slower                                                   |
| meteor_contest                   | 73.5 ms                                                                | 74.0 ms: 1.01x slower                                                  |
| spectral_norm                    | 73.7 ms                                                                | 74.3 ms: 1.01x slower                                                  |
| logging_format                   | 3.39 us                                                                | 3.42 us: 1.01x slower                                                  |
| async_tree_eager_tg              | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                                  |
| typing_runtime_protocols         | 69.4 us                                                                | 70.4 us: 1.01x slower                                                  |
| async_tree_eager                 | 64.1 ms                                                                | 65.1 ms: 1.02x slower                                                  |
| Geometric mean                   | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (50): tornado_http, dask, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, mypy2, deltablue, 2to3, unpickle, asyncio_tcp, docutils, html5lib, json_dumps, async_generators, json, async_tree_io_tg, nbody, async_tree_eager_io, gc_traversal, hexiom, scimark_fft, deepcopy_memo, pidigits, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed, sqlite_synth, raytrace, bench_mp_pool, xml_etree_generate, pickle_pure_python, sympy_sum, async_tree_none, sympy_integrate, sympy_str, json_loads, asyncio_tcp_ssl, tomli_loads, pickle_list, async_tree_memoization, genshi_xml, async_tree_eager_memoization, pycparser, float, async_tree_io, thrift, async_tree_none_tg, async_tree_eager_memoization_tg, pathlib, aiohttp, gunicorn

# HPT report

- Reliability score: 55.81% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x