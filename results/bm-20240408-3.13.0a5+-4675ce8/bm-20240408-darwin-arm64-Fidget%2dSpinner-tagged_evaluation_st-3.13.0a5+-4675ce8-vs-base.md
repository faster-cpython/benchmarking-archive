# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: darwin-arm64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.00x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 163 ms                                                                 | 162 ms: 1.00x faster                                                             |
| chameleon      | 4.54 ms                                                                | 4.40 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_tg              | 43.9 ms                                                                | 43.3 ms: 1.01x faster                                                            |
| async_tree_eager                 | 63.1 ms                                                                | 62.9 ms: 1.00x faster                                                            |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 334 ms: 1.00x slower                                                             |
| Geometric mean                   | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (13): async_tree_memoization, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_eager_memoization, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 65.9 ms                                                                | 65.0 ms: 1.01x faster                                                            |
| float          | 51.1 ms                                                                | 51.0 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 154 ms                                                                 | 155 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_generate   | 55.2 ms                                                                | 54.2 ms: 1.02x faster                                                            |
| unpickle_list        | 3.07 us                                                                | 3.02 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 69.8 ms                                                                | 68.8 ms: 1.02x faster                                                            |
| xml_etree_process    | 37.9 ms                                                                | 37.4 ms: 1.01x faster                                                            |
| xml_etree_parse      | 101 ms                                                                 | 99.6 ms: 1.01x faster                                                            |
| pickle_dict          | 18.2 us                                                                | 18.1 us: 1.00x faster                                                            |
| unpickle_pure_python | 145 us                                                                 | 146 us: 1.00x slower                                                             |
| pickle_list          | 2.92 us                                                                | 2.95 us: 1.01x slower                                                            |
| tomli_loads          | 1.49 sec                                                               | 1.50 sec: 1.01x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (5): unpickle, pickle, json_loads, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 12.1 ms                                                                | 12.0 ms: 1.01x faster                                                            |
| python_startup_no_site | 10.4 ms                                                                | 10.3 ms: 1.01x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                            |
| mako           | 7.20 ms                                                                | 7.14 ms: 1.01x faster                                                            |
| genshi_xml     | 31.8 ms                                                                | 31.6 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240406-darwin-arm64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| chameleon                        | 4.54 ms                                                                | 4.40 ms: 1.03x faster                                                            |
| coverage                         | 47.4 ms                                                                | 46.4 ms: 1.02x faster                                                            |
| generators                       | 27.9 ms                                                                | 27.4 ms: 1.02x faster                                                            |
| xml_etree_generate               | 55.2 ms                                                                | 54.2 ms: 1.02x faster                                                            |
| deepcopy                         | 213 us                                                                 | 209 us: 1.02x faster                                                             |
| unpickle_list                    | 3.07 us                                                                | 3.02 us: 1.02x faster                                                            |
| xml_etree_iterparse              | 69.8 ms                                                                | 68.8 ms: 1.02x faster                                                            |
| coroutines                       | 17.3 ms                                                                | 17.0 ms: 1.01x faster                                                            |
| async_tree_eager_tg              | 43.9 ms                                                                | 43.3 ms: 1.01x faster                                                            |
| logging_format                   | 3.47 us                                                                | 3.42 us: 1.01x faster                                                            |
| typing_runtime_protocols         | 70.3 us                                                                | 69.4 us: 1.01x faster                                                            |
| richards                         | 31.0 ms                                                                | 30.6 ms: 1.01x faster                                                            |
| nbody                            | 65.9 ms                                                                | 65.0 ms: 1.01x faster                                                            |
| crypto_pyaes                     | 46.9 ms                                                                | 46.3 ms: 1.01x faster                                                            |
| logging_simple                   | 3.19 us                                                                | 3.16 us: 1.01x faster                                                            |
| xml_etree_process                | 37.9 ms                                                                | 37.4 ms: 1.01x faster                                                            |
| xml_etree_parse                  | 101 ms                                                                 | 99.6 ms: 1.01x faster                                                            |
| deepcopy_reduce                  | 1.90 us                                                                | 1.88 us: 1.01x faster                                                            |
| thrift                           | 446 us                                                                 | 442 us: 1.01x faster                                                             |
| json                             | 2.98 ms                                                                | 2.95 ms: 1.01x faster                                                            |
| scimark_sparse_mat_mult          | 3.03 ms                                                                | 3.00 ms: 1.01x faster                                                            |
| bench_thread_pool                | 475 us                                                                 | 471 us: 1.01x faster                                                             |
| genshi_text                      | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                            |
| sympy_expand                     | 232 ms                                                                 | 230 ms: 1.01x faster                                                             |
| sympy_str                        | 136 ms                                                                 | 135 ms: 1.01x faster                                                             |
| mako                             | 7.20 ms                                                                | 7.14 ms: 1.01x faster                                                            |
| spectral_norm                    | 71.8 ms                                                                | 71.2 ms: 1.01x faster                                                            |
| pyflate                          | 327 ms                                                                 | 325 ms: 1.01x faster                                                             |
| sqlglot_normalize                | 172 ms                                                                 | 171 ms: 1.01x faster                                                             |
| create_gc_cycles                 | 890 us                                                                 | 885 us: 1.01x faster                                                             |
| scimark_sor                      | 99.8 ms                                                                | 99.2 ms: 1.01x faster                                                            |
| python_startup                   | 12.1 ms                                                                | 12.0 ms: 1.01x faster                                                            |
| sympy_sum                        | 71.4 ms                                                                | 71.0 ms: 1.01x faster                                                            |
| python_startup_no_site           | 10.4 ms                                                                | 10.3 ms: 1.01x faster                                                            |
| hexiom                           | 4.23 ms                                                                | 4.20 ms: 1.01x faster                                                            |
| mdp                              | 1.54 sec                                                               | 1.53 sec: 1.01x faster                                                           |
| genshi_xml                       | 31.8 ms                                                                | 31.6 ms: 1.01x faster                                                            |
| sqlite_synth                     | 1.56 us                                                                | 1.56 us: 1.00x faster                                                            |
| nqueens                          | 56.2 ms                                                                | 56.0 ms: 1.00x faster                                                            |
| scimark_lu                       | 68.8 ms                                                                | 68.5 ms: 1.00x faster                                                            |
| async_generators                 | 289 ms                                                                 | 287 ms: 1.00x faster                                                             |
| raytrace                         | 154 ms                                                                 | 153 ms: 1.00x faster                                                             |
| deepcopy_memo                    | 23.8 us                                                                | 23.7 us: 1.00x faster                                                            |
| chaos                            | 36.1 ms                                                                | 35.9 ms: 1.00x faster                                                            |
| 2to3                             | 163 ms                                                                 | 162 ms: 1.00x faster                                                             |
| scimark_monte_carlo              | 44.2 ms                                                                | 44.1 ms: 1.00x faster                                                            |
| sqlglot_optimize                 | 32.1 ms                                                                | 31.9 ms: 1.00x faster                                                            |
| pickle_dict                      | 18.2 us                                                                | 18.1 us: 1.00x faster                                                            |
| async_tree_eager                 | 63.1 ms                                                                | 62.9 ms: 1.00x faster                                                            |
| fannkuch                         | 261 ms                                                                 | 260 ms: 1.00x faster                                                             |
| sqlglot_parse                    | 749 us                                                                 | 747 us: 1.00x faster                                                             |
| float                            | 51.1 ms                                                                | 51.0 ms: 1.00x faster                                                            |
| logging_silent                   | 64.4 ns                                                                | 64.3 ns: 1.00x faster                                                            |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 334 ms: 1.00x slower                                                             |
| richards_super                   | 34.4 ms                                                                | 34.5 ms: 1.00x slower                                                            |
| meteor_contest                   | 71.4 ms                                                                | 71.7 ms: 1.00x slower                                                            |
| unpickle_pure_python             | 145 us                                                                 | 146 us: 1.00x slower                                                             |
| pathlib                          | 24.6 ms                                                                | 24.8 ms: 1.01x slower                                                            |
| pprint_pformat                   | 976 ms                                                                 | 983 ms: 1.01x slower                                                             |
| pprint_safe_repr                 | 480 ms                                                                 | 483 ms: 1.01x slower                                                             |
| regex_dna                        | 154 ms                                                                 | 155 ms: 1.01x slower                                                             |
| pickle_list                      | 2.92 us                                                                | 2.95 us: 1.01x slower                                                            |
| tomli_loads                      | 1.49 sec                                                               | 1.50 sec: 1.01x slower                                                           |
| aiohttp                          | 1.04 ms                                                                | 1.10 ms: 1.06x slower                                                            |
| Geometric mean                   | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (43): asyncio_tcp, tornado_http, unpickle, async_tree_memoization, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_io, async_tree_none_tg, telco, async_tree_io_tg, dask, pylint, async_tree_cpu_io_mixed_tg, async_tree_none, sqlglot_transpile, async_tree_eager_io, mypy2, scimark_fft, pickle, async_tree_eager_memoization_tg, sympy_integrate, asyncio_tcp_ssl, json_loads, gc_traversal, go, async_tree_eager_memoization, pickle_pure_python, dulwich_log, pidigits, regex_compile, json_dumps, html5lib, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, comprehensions, pycparser, deltablue, regex_v8, bench_mp_pool, docutils, regex_effbot, gunicorn

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x