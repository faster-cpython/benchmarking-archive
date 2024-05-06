# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.00x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| chameleon      | 4.45 ms                                                                | 4.53 ms: 1.02x slower                                                |
| docutils       | 1.55 sec                                                               | 1.54 sec: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_tg              | 44.8 ms                                                                | 44.4 ms: 1.01x faster                                                |
| async_tree_eager                 | 65.9 ms                                                                | 65.4 ms: 1.01x faster                                                |
| async_tree_eager_cpu_io_mixed    | 354 ms                                                                 | 355 ms: 1.00x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.01x slower                                                 |
| Geometric mean                   | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (12): async_tree_none, async_tree_io, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_memoization, async_tree_io_tg, async_tree_eager_io, async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 49.2 ms                                                                | 49.1 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 80.9 ms                                                                | 79.5 ms: 1.02x faster                                                |
| regex_effbot   | 2.63 ms                                                                | 2.62 ms: 1.00x faster                                                |
| regex_v8       | 17.1 ms                                                                | 17.1 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 9.21 us                                                                | 9.12 us: 1.01x faster                                                |
| xml_etree_generate   | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                |
| tomli_loads          | 1.30 sec                                                               | 1.29 sec: 1.01x faster                                               |
| pickle_dict          | 18.1 us                                                                | 18.0 us: 1.00x faster                                                |
| json_dumps           | 6.34 ms                                                                | 6.32 ms: 1.00x faster                                                |
| unpickle_pure_python | 143 us                                                                 | 143 us: 1.00x slower                                                 |
| pickle_list          | 2.95 us                                                                | 2.97 us: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (7): xml_etree_iterparse, xml_etree_process, unpickle_list, pickle, json_loads, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                |
| python_startup         | 13.3 ms                                                                | 13.4 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 20.7 ms                                                                | 20.7 ms: 1.00x faster                                                |
| mako            | 6.94 ms                                                                | 6.96 ms: 1.00x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| aiohttp                          | 1.12 ms                                                                | 1.06 ms: 1.06x faster                                                |
| fannkuch                         | 263 ms                                                                 | 254 ms: 1.03x faster                                                 |
| regex_compile                    | 80.9 ms                                                                | 79.5 ms: 1.02x faster                                                |
| logging_format                   | 3.60 us                                                                | 3.56 us: 1.01x faster                                                |
| scimark_monte_carlo              | 44.3 ms                                                                | 43.8 ms: 1.01x faster                                                |
| pprint_safe_repr                 | 490 ms                                                                 | 485 ms: 1.01x faster                                                 |
| async_generators                 | 305 ms                                                                 | 301 ms: 1.01x faster                                                 |
| sympy_sum                        | 75.9 ms                                                                | 75.1 ms: 1.01x faster                                                |
| unpickle                         | 9.21 us                                                                | 9.12 us: 1.01x faster                                                |
| pprint_pformat                   | 1000 ms                                                                | 990 ms: 1.01x faster                                                 |
| async_tree_eager_tg              | 44.8 ms                                                                | 44.4 ms: 1.01x faster                                                |
| hexiom                           | 4.97 ms                                                                | 4.93 ms: 1.01x faster                                                |
| logging_simple                   | 3.30 us                                                                | 3.27 us: 1.01x faster                                                |
| pycparser                        | 668 ms                                                                 | 663 ms: 1.01x faster                                                 |
| thrift                           | 433 us                                                                 | 429 us: 1.01x faster                                                 |
| xml_etree_generate               | 54.7 ms                                                                | 54.3 ms: 1.01x faster                                                |
| chaos                            | 38.6 ms                                                                | 38.3 ms: 1.01x faster                                                |
| coroutines                       | 16.8 ms                                                                | 16.7 ms: 1.01x faster                                                |
| logging_silent                   | 66.1 ns                                                                | 65.6 ns: 1.01x faster                                                |
| async_tree_eager                 | 65.9 ms                                                                | 65.4 ms: 1.01x faster                                                |
| docutils                         | 1.55 sec                                                               | 1.54 sec: 1.01x faster                                               |
| raytrace                         | 180 ms                                                                 | 179 ms: 1.01x faster                                                 |
| tomli_loads                      | 1.30 sec                                                               | 1.29 sec: 1.01x faster                                               |
| bench_thread_pool                | 494 us                                                                 | 491 us: 1.01x faster                                                 |
| pyflate                          | 332 ms                                                                 | 330 ms: 1.01x faster                                                 |
| sqlglot_transpile                | 938 us                                                                 | 933 us: 1.01x faster                                                 |
| pickle_dict                      | 18.1 us                                                                | 18.0 us: 1.00x faster                                                |
| telco                            | 4.56 ms                                                                | 4.54 ms: 1.00x faster                                                |
| json_dumps                       | 6.34 ms                                                                | 6.32 ms: 1.00x faster                                                |
| sqlglot_normalize                | 176 ms                                                                 | 175 ms: 1.00x faster                                                 |
| deltablue                        | 2.36 ms                                                                | 2.35 ms: 1.00x faster                                                |
| django_template                  | 20.7 ms                                                                | 20.7 ms: 1.00x faster                                                |
| nqueens                          | 60.5 ms                                                                | 60.4 ms: 1.00x faster                                                |
| deepcopy_memo                    | 24.3 us                                                                | 24.3 us: 1.00x faster                                                |
| sympy_expand                     | 237 ms                                                                 | 236 ms: 1.00x faster                                                 |
| go                               | 104 ms                                                                 | 104 ms: 1.00x faster                                                 |
| regex_effbot                     | 2.63 ms                                                                | 2.62 ms: 1.00x faster                                                |
| regex_v8                         | 17.1 ms                                                                | 17.1 ms: 1.00x faster                                                |
| scimark_lu                       | 81.9 ms                                                                | 81.8 ms: 1.00x faster                                                |
| float                            | 49.2 ms                                                                | 49.1 ms: 1.00x faster                                                |
| scimark_fft                      | 199 ms                                                                 | 199 ms: 1.00x faster                                                 |
| meteor_contest                   | 73.1 ms                                                                | 73.2 ms: 1.00x slower                                                |
| unpickle_pure_python             | 143 us                                                                 | 143 us: 1.00x slower                                                 |
| asyncio_websockets               | 409 ms                                                                 | 409 ms: 1.00x slower                                                 |
| mako                             | 6.94 ms                                                                | 6.96 ms: 1.00x slower                                                |
| create_gc_cycles                 | 845 us                                                                 | 846 us: 1.00x slower                                                 |
| async_tree_eager_cpu_io_mixed    | 354 ms                                                                 | 355 ms: 1.00x slower                                                 |
| richards                         | 31.0 ms                                                                | 31.1 ms: 1.00x slower                                                |
| python_startup_no_site           | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 335 ms: 1.01x slower                                                 |
| comprehensions                   | 12.0 us                                                                | 12.1 us: 1.01x slower                                                |
| python_startup                   | 13.3 ms                                                                | 13.4 ms: 1.01x slower                                                |
| pickle_list                      | 2.95 us                                                                | 2.97 us: 1.01x slower                                                |
| mdp                              | 1.57 sec                                                               | 1.58 sec: 1.01x slower                                               |
| sympy_integrate                  | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                |
| json                             | 2.95 ms                                                                | 3.00 ms: 1.02x slower                                                |
| chameleon                        | 4.45 ms                                                                | 4.53 ms: 1.02x slower                                                |
| Geometric mean                   | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (52): asyncio_tcp, unpack_sequence, async_tree_none, pathlib, scimark_sor, async_tree_io, mypy2, async_tree_eager_memoization, asyncio_tcp_ssl, async_tree_memoization_tg, async_tree_memoization, deepcopy_reduce, async_tree_io_tg, gunicorn, xml_etree_iterparse, pylint, html5lib, genshi_text, async_tree_eager_io, sqlglot_parse, sympy_str, sqlite_synth, nbody, async_tree_none_tg, crypto_pyaes, regex_dna, generators, spectral_norm, sqlglot_optimize, async_tree_eager_memoization_tg, async_tree_eager_io_tg, coverage, xml_etree_process, unpickle_list, pidigits, 2to3, pickle, gc_traversal, json_loads, scimark_sparse_mat_mult, richards_super, pickle_pure_python, dulwich_log, deepcopy, async_tree_cpu_io_mixed_tg, bench_mp_pool, genshi_xml, async_tree_cpu_io_mixed, typing_runtime_protocols, xml_etree_parse, dask, tornado_http

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x