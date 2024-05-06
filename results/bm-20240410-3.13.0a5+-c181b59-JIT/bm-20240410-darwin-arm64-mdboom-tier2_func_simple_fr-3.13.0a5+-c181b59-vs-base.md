# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: darwin-arm64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.00x slower
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                   |
| async_tree_eager                 | 64.1 ms                                                                | 64.5 ms: 1.01x slower                                                  |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (14): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed, async_tree_eager_io, async_tree_eager_tg, async_tree_none_tg, async_tree_io, async_tree_eager_memoization, async_tree_none, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 49.0 ms                                                                | 49.3 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.68 ms                                                                | 2.64 ms: 1.02x faster                                                  |
| regex_v8       | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                  |
| regex_compile  | 85.8 ms                                                                | 85.4 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 3.06 us                                                                | 2.99 us: 1.02x faster                                                  |
| pickle_dict          | 18.2 us                                                                | 18.0 us: 1.01x faster                                                  |
| pickle               | 7.50 us                                                                | 7.46 us: 1.00x faster                                                  |
| xml_etree_generate   | 54.3 ms                                                                | 54.6 ms: 1.01x slower                                                  |
| xml_etree_process    | 37.1 ms                                                                | 37.3 ms: 1.01x slower                                                  |
| unpickle_pure_python | 140 us                                                                 | 141 us: 1.01x slower                                                   |
| xml_etree_iterparse  | 72.1 ms                                                                | 72.9 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (7): pickle_list, json_dumps, json_loads, pickle_pure_python, unpickle, tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                  |
| python_startup         | 13.4 ms                                                                | 13.6 ms: 1.02x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 14.7 ms                                                                | 14.8 ms: 1.01x slower                                                  |
| genshi_xml     | 31.4 ms                                                                | 31.8 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list                    | 3.06 us                                                                | 2.99 us: 1.02x faster                                                  |
| regex_effbot                     | 2.68 ms                                                                | 2.64 ms: 1.02x faster                                                  |
| pprint_safe_repr                 | 492 ms                                                                 | 484 ms: 1.02x faster                                                   |
| coroutines                       | 17.1 ms                                                                | 16.9 ms: 1.01x faster                                                  |
| pprint_pformat                   | 1000 ms                                                                | 988 ms: 1.01x faster                                                   |
| json                             | 2.96 ms                                                                | 2.93 ms: 1.01x faster                                                  |
| pickle_dict                      | 18.2 us                                                                | 18.0 us: 1.01x faster                                                  |
| regex_v8                         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                  |
| pyflate                          | 317 ms                                                                 | 316 ms: 1.01x faster                                                   |
| pickle                           | 7.50 us                                                                | 7.46 us: 1.00x faster                                                  |
| regex_compile                    | 85.8 ms                                                                | 85.4 ms: 1.00x faster                                                  |
| mdp                              | 1.58 sec                                                               | 1.57 sec: 1.00x faster                                                 |
| scimark_fft                      | 200 ms                                                                 | 200 ms: 1.00x faster                                                   |
| meteor_contest                   | 73.5 ms                                                                | 73.5 ms: 1.00x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.00x slower                                                   |
| asyncio_websockets               | 409 ms                                                                 | 410 ms: 1.00x slower                                                   |
| sqlite_synth                     | 1.58 us                                                                | 1.59 us: 1.00x slower                                                  |
| sqlglot_parse                    | 766 us                                                                 | 767 us: 1.00x slower                                                   |
| nqueens                          | 60.5 ms                                                                | 60.6 ms: 1.00x slower                                                  |
| chaos                            | 37.9 ms                                                                | 38.1 ms: 1.00x slower                                                  |
| gc_traversal                     | 2.45 ms                                                                | 2.46 ms: 1.00x slower                                                  |
| scimark_monte_carlo              | 43.2 ms                                                                | 43.3 ms: 1.00x slower                                                  |
| deepcopy_memo                    | 24.1 us                                                                | 24.2 us: 1.00x slower                                                  |
| go                               | 107 ms                                                                 | 107 ms: 1.00x slower                                                   |
| richards                         | 29.6 ms                                                                | 29.8 ms: 1.00x slower                                                  |
| sympy_integrate                  | 11.3 ms                                                                | 11.4 ms: 1.00x slower                                                  |
| pylint                           | 153 ms                                                                 | 154 ms: 1.00x slower                                                   |
| xml_etree_generate               | 54.3 ms                                                                | 54.6 ms: 1.01x slower                                                  |
| crypto_pyaes                     | 46.3 ms                                                                | 46.5 ms: 1.01x slower                                                  |
| dulwich_log                      | 28.7 ms                                                                | 28.9 ms: 1.01x slower                                                  |
| float                            | 49.0 ms                                                                | 49.3 ms: 1.01x slower                                                  |
| xml_etree_process                | 37.1 ms                                                                | 37.3 ms: 1.01x slower                                                  |
| hexiom                           | 4.81 ms                                                                | 4.84 ms: 1.01x slower                                                  |
| comprehensions                   | 11.9 us                                                                | 12.0 us: 1.01x slower                                                  |
| deepcopy                         | 211 us                                                                 | 212 us: 1.01x slower                                                   |
| logging_simple                   | 3.13 us                                                                | 3.16 us: 1.01x slower                                                  |
| async_tree_eager                 | 64.1 ms                                                                | 64.5 ms: 1.01x slower                                                  |
| typing_runtime_protocols         | 69.4 us                                                                | 70.0 us: 1.01x slower                                                  |
| genshi_text                      | 14.7 ms                                                                | 14.8 ms: 1.01x slower                                                  |
| unpickle_pure_python             | 140 us                                                                 | 141 us: 1.01x slower                                                   |
| xml_etree_iterparse              | 72.1 ms                                                                | 72.9 ms: 1.01x slower                                                  |
| spectral_norm                    | 73.7 ms                                                                | 74.4 ms: 1.01x slower                                                  |
| pycparser                        | 651 ms                                                                 | 658 ms: 1.01x slower                                                   |
| coverage                         | 46.0 ms                                                                | 46.6 ms: 1.01x slower                                                  |
| genshi_xml                       | 31.4 ms                                                                | 31.8 ms: 1.01x slower                                                  |
| deepcopy_reduce                  | 1.86 us                                                                | 1.88 us: 1.01x slower                                                  |
| python_startup_no_site           | 11.6 ms                                                                | 11.8 ms: 1.01x slower                                                  |
| logging_format                   | 3.39 us                                                                | 3.44 us: 1.02x slower                                                  |
| python_startup                   | 13.4 ms                                                                | 13.6 ms: 1.02x slower                                                  |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (58): tornado_http, async_tree_cpu_io_mixed_tg, thrift, dask, async_tree_cpu_io_mixed, aiohttp, async_tree_eager_io_tg, telco, asyncio_tcp_ssl, pickle_list, async_tree_io_tg, fannkuch, deltablue, docutils, async_generators, json_dumps, raytrace, bench_thread_pool, sqlglot_optimize, scimark_lu, regex_dna, chameleon, async_tree_memoization, scimark_sor, json_loads, nbody, async_tree_memoization_tg, create_gc_cycles, pickle_pure_python, scimark_sparse_mat_mult, 2to3, mypy2, richards_super, sqlglot_normalize, logging_silent, sympy_expand, mako, sqlglot_transpile, sympy_str, async_tree_eager_cpu_io_mixed, pidigits, unpickle, async_tree_eager_io, async_tree_eager_tg, async_tree_none_tg, bench_mp_pool, generators, async_tree_io, tomli_loads, sympy_sum, async_tree_eager_memoization, html5lib, async_tree_none, async_tree_eager_memoization_tg, xml_etree_parse, pathlib, gunicorn, asyncio_tcp

# HPT report

- Reliability score: 99.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x