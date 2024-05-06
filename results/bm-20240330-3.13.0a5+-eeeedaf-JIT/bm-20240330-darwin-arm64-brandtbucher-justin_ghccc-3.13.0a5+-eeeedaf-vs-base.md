# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: darwin-arm64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.00x slower
- HPT reliability: 96.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 173 ms                                                                 | 173 ms: 1.00x slower                                                 |
| chameleon      | 4.45 ms                                                                | 4.51 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed    | 354 ms                                                                 | 355 ms: 1.00x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                 |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (14): async_tree_none, async_tree_eager, async_tree_eager_io, async_tree_eager_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_eager_memoization, async_tree_io_tg, async_tree_none_tg, async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 70.2 ms                                                                | 70.3 ms: 1.00x slower                                                |
| float          | 49.2 ms                                                                | 49.2 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.63 ms                                                                | 2.62 ms: 1.00x faster                                                |
| regex_dna      | 152 ms                                                                 | 152 ms: 1.00x faster                                                 |
| regex_compile  | 80.9 ms                                                                | 81.0 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps          | 6.34 ms                                                                | 6.27 ms: 1.01x faster                                                |
| xml_etree_generate  | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                |
| unpickle            | 9.21 us                                                                | 9.17 us: 1.00x faster                                                |
| xml_etree_process   | 36.8 ms                                                                | 37.0 ms: 1.01x slower                                                |
| xml_etree_iterparse | 72.5 ms                                                                | 73.0 ms: 1.01x slower                                                |
| pickle_list         | 2.95 us                                                                | 2.98 us: 1.01x slower                                                |
| xml_etree_parse     | 106 ms                                                                 | 107 ms: 1.01x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (7): unpickle_list, tomli_loads, pickle, unpickle_pure_python, pickle_dict, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 14.8 ms                                                                | 14.9 ms: 1.00x slower                                                |
| genshi_xml     | 31.3 ms                                                                | 31.5 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                        | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| fannkuch                         | 263 ms                                                                 | 259 ms: 1.02x faster                                                 |
| json_dumps                       | 6.34 ms                                                                | 6.27 ms: 1.01x faster                                                |
| logging_format                   | 3.60 us                                                                | 3.57 us: 1.01x faster                                                |
| pprint_safe_repr                 | 490 ms                                                                 | 486 ms: 1.01x faster                                                 |
| xml_etree_generate               | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                |
| sqlglot_normalize                | 176 ms                                                                 | 175 ms: 1.01x faster                                                 |
| scimark_sor                      | 108 ms                                                                 | 108 ms: 1.01x faster                                                 |
| sympy_sum                        | 75.9 ms                                                                | 75.5 ms: 1.01x faster                                                |
| async_generators                 | 305 ms                                                                 | 303 ms: 1.01x faster                                                 |
| unpickle                         | 9.21 us                                                                | 9.17 us: 1.00x faster                                                |
| coroutines                       | 16.8 ms                                                                | 16.8 ms: 1.00x faster                                                |
| deepcopy_reduce                  | 1.87 us                                                                | 1.86 us: 1.00x faster                                                |
| chaos                            | 38.6 ms                                                                | 38.5 ms: 1.00x faster                                                |
| raytrace                         | 180 ms                                                                 | 179 ms: 1.00x faster                                                 |
| pprint_pformat                   | 1000 ms                                                                | 998 ms: 1.00x faster                                                 |
| sympy_expand                     | 237 ms                                                                 | 236 ms: 1.00x faster                                                 |
| scimark_fft                      | 199 ms                                                                 | 199 ms: 1.00x faster                                                 |
| regex_effbot                     | 2.63 ms                                                                | 2.62 ms: 1.00x faster                                                |
| regex_dna                        | 152 ms                                                                 | 152 ms: 1.00x faster                                                 |
| scimark_monte_carlo              | 44.3 ms                                                                | 44.3 ms: 1.00x faster                                                |
| nbody                            | 70.2 ms                                                                | 70.3 ms: 1.00x slower                                                |
| float                            | 49.2 ms                                                                | 49.2 ms: 1.00x slower                                                |
| regex_compile                    | 80.9 ms                                                                | 81.0 ms: 1.00x slower                                                |
| sympy_integrate                  | 11.2 ms                                                                | 11.3 ms: 1.00x slower                                                |
| asyncio_websockets               | 409 ms                                                                 | 410 ms: 1.00x slower                                                 |
| comprehensions                   | 12.0 us                                                                | 12.1 us: 1.00x slower                                                |
| 2to3                             | 173 ms                                                                 | 173 ms: 1.00x slower                                                 |
| python_startup_no_site           | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                |
| meteor_contest                   | 73.1 ms                                                                | 73.3 ms: 1.00x slower                                                |
| genshi_text                      | 14.8 ms                                                                | 14.9 ms: 1.00x slower                                                |
| sqlglot_parse                    | 766 us                                                                 | 769 us: 1.00x slower                                                 |
| pyflate                          | 332 ms                                                                 | 333 ms: 1.00x slower                                                 |
| nqueens                          | 60.5 ms                                                                | 60.7 ms: 1.00x slower                                                |
| async_tree_eager_cpu_io_mixed    | 354 ms                                                                 | 355 ms: 1.00x slower                                                 |
| sympy_str                        | 139 ms                                                                 | 140 ms: 1.00x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                 |
| crypto_pyaes                     | 46.8 ms                                                                | 47.1 ms: 1.01x slower                                                |
| create_gc_cycles                 | 845 us                                                                 | 850 us: 1.01x slower                                                 |
| bench_thread_pool                | 494 us                                                                 | 497 us: 1.01x slower                                                 |
| genshi_xml                       | 31.3 ms                                                                | 31.5 ms: 1.01x slower                                                |
| sqlite_synth                     | 1.58 us                                                                | 1.59 us: 1.01x slower                                                |
| xml_etree_process                | 36.8 ms                                                                | 37.0 ms: 1.01x slower                                                |
| xml_etree_iterparse              | 72.5 ms                                                                | 73.0 ms: 1.01x slower                                                |
| thrift                           | 433 us                                                                 | 436 us: 1.01x slower                                                 |
| richards_super                   | 34.7 ms                                                                | 34.9 ms: 1.01x slower                                                |
| generators                       | 26.4 ms                                                                | 26.7 ms: 1.01x slower                                                |
| pickle_list                      | 2.95 us                                                                | 2.98 us: 1.01x slower                                                |
| xml_etree_parse                  | 106 ms                                                                 | 107 ms: 1.01x slower                                                 |
| mdp                              | 1.57 sec                                                               | 1.59 sec: 1.01x slower                                               |
| richards                         | 31.0 ms                                                                | 31.4 ms: 1.01x slower                                                |
| chameleon                        | 4.45 ms                                                                | 4.51 ms: 1.01x slower                                                |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (58): asyncio_tcp_ssl, logging_silent, unpickle_list, async_tree_none, tomli_loads, async_tree_eager, aiohttp, django_template, dulwich_log, logging_simple, async_tree_eager_io, deepcopy, sqlglot_optimize, async_tree_eager_tg, pickle, hexiom, async_tree_io, deltablue, mypy2, coverage, pylint, unpickle_pure_python, pycparser, async_tree_memoization, regex_v8, pidigits, telco, docutils, python_startup, scimark_lu, go, pickle_dict, deepcopy_memo, scimark_sparse_mat_mult, async_tree_memoization_tg, mako, async_tree_eager_memoization, async_tree_io_tg, json_loads, gc_traversal, async_tree_none_tg, async_tree_eager_io_tg, pickle_pure_python, spectral_norm, async_tree_eager_memoization_tg, html5lib, json, dask, typing_runtime_protocols, sqlglot_transpile, unpack_sequence, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, pathlib, gunicorn, bench_mp_pool, tornado_http, asyncio_tcp

# HPT report

- Reliability score: 96.48% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x