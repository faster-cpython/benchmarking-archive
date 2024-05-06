# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: darwin-arm64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.00x faster
- HPT reliability: 99.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| chameleon      | 4.55 ms                                                                | 4.52 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 355 ms                                                                 | 355 ms: 1.00x slower                                                 |
| async_tree_eager              | 65.8 ms                                                                | 66.1 ms: 1.01x slower                                                |
| Geometric mean                | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (14): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization_tg, async_tree_eager_memoization, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, async_tree_eager_io, async_tree_memoization, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_tg, async_tree_io, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 49.1 ms                                                                | 49.3 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 80.8 ms                                                                | 79.6 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (3): regex_dna, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 7.49 us                                                                | 7.41 us: 1.01x faster                                                |
| unpickle             | 9.18 us                                                                | 9.10 us: 1.01x faster                                                |
| xml_etree_iterparse  | 72.9 ms                                                                | 72.4 ms: 1.01x faster                                                |
| json_dumps           | 6.36 ms                                                                | 6.32 ms: 1.01x faster                                                |
| xml_etree_process    | 36.8 ms                                                                | 36.8 ms: 1.00x faster                                                |
| unpickle_pure_python | 143 us                                                                 | 143 us: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (8): xml_etree_parse, json_loads, xml_etree_generate, pickle_pure_python, pickle_dict, pickle_list, unpickle_list, tomli_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 31.3 ms                                                                | 31.2 ms: 1.00x faster                                                |
| mako            | 6.95 ms                                                                | 6.92 ms: 1.00x faster                                                |
| django_template | 20.7 ms                                                                | 20.7 ms: 1.00x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                     | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-darwin-arm64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal                  | 2.60 ms                                                                | 2.45 ms: 1.06x faster                                                |
| pathlib                       | 24.5 ms                                                                | 24.0 ms: 1.02x faster                                                |
| fannkuch                      | 264 ms                                                                 | 259 ms: 1.02x faster                                                 |
| regex_compile                 | 80.8 ms                                                                | 79.6 ms: 1.02x faster                                                |
| scimark_monte_carlo           | 44.4 ms                                                                | 43.8 ms: 1.02x faster                                                |
| create_gc_cycles              | 855 us                                                                 | 844 us: 1.01x faster                                                 |
| hexiom                        | 4.97 ms                                                                | 4.91 ms: 1.01x faster                                                |
| pycparser                     | 669 ms                                                                 | 661 ms: 1.01x faster                                                 |
| pickle                        | 7.49 us                                                                | 7.41 us: 1.01x faster                                                |
| unpickle                      | 9.18 us                                                                | 9.10 us: 1.01x faster                                                |
| pyflate                       | 331 ms                                                                 | 328 ms: 1.01x faster                                                 |
| pprint_pformat                | 994 ms                                                                 | 986 ms: 1.01x faster                                                 |
| richards                      | 31.5 ms                                                                | 31.2 ms: 1.01x faster                                                |
| bench_thread_pool             | 495 us                                                                 | 492 us: 1.01x faster                                                 |
| deepcopy                      | 213 us                                                                 | 212 us: 1.01x faster                                                 |
| sqlite_synth                  | 1.59 us                                                                | 1.58 us: 1.01x faster                                                |
| richards_super                | 34.7 ms                                                                | 34.5 ms: 1.01x faster                                                |
| deltablue                     | 2.37 ms                                                                | 2.35 ms: 1.01x faster                                                |
| chameleon                     | 4.55 ms                                                                | 4.52 ms: 1.01x faster                                                |
| xml_etree_iterparse           | 72.9 ms                                                                | 72.4 ms: 1.01x faster                                                |
| sqlglot_normalize             | 177 ms                                                                 | 176 ms: 1.01x faster                                                 |
| json_dumps                    | 6.36 ms                                                                | 6.32 ms: 1.01x faster                                                |
| sympy_expand                  | 237 ms                                                                 | 236 ms: 1.00x faster                                                 |
| chaos                         | 38.5 ms                                                                | 38.3 ms: 1.00x faster                                                |
| genshi_xml                    | 31.3 ms                                                                | 31.2 ms: 1.00x faster                                                |
| raytrace                      | 179 ms                                                                 | 178 ms: 1.00x faster                                                 |
| mako                          | 6.95 ms                                                                | 6.92 ms: 1.00x faster                                                |
| sqlglot_optimize              | 33.8 ms                                                                | 33.6 ms: 1.00x faster                                                |
| pprint_safe_repr              | 485 ms                                                                 | 483 ms: 1.00x faster                                                 |
| go                            | 104 ms                                                                 | 104 ms: 1.00x faster                                                 |
| django_template               | 20.7 ms                                                                | 20.7 ms: 1.00x faster                                                |
| scimark_sparse_mat_mult       | 3.13 ms                                                                | 3.12 ms: 1.00x faster                                                |
| xml_etree_process             | 36.8 ms                                                                | 36.8 ms: 1.00x faster                                                |
| asyncio_websockets            | 409 ms                                                                 | 409 ms: 1.00x faster                                                 |
| meteor_contest                | 73.8 ms                                                                | 73.9 ms: 1.00x slower                                                |
| async_tree_eager_cpu_io_mixed | 355 ms                                                                 | 355 ms: 1.00x slower                                                 |
| crypto_pyaes                  | 46.8 ms                                                                | 46.9 ms: 1.00x slower                                                |
| unpickle_pure_python          | 143 us                                                                 | 143 us: 1.00x slower                                                 |
| float                         | 49.1 ms                                                                | 49.3 ms: 1.00x slower                                                |
| mdp                           | 1.57 sec                                                               | 1.58 sec: 1.00x slower                                               |
| coroutines                    | 16.8 ms                                                                | 16.9 ms: 1.00x slower                                                |
| async_tree_eager              | 65.8 ms                                                                | 66.1 ms: 1.01x slower                                                |
| typing_runtime_protocols      | 69.3 us                                                                | 69.7 us: 1.01x slower                                                |
| comprehensions                | 12.0 us                                                                | 12.1 us: 1.01x slower                                                |
| scimark_lu                    | 81.8 ms                                                                | 82.4 ms: 1.01x slower                                                |
| nqueens                       | 60.4 ms                                                                | 60.9 ms: 1.01x slower                                                |
| logging_format                | 3.55 us                                                                | 3.59 us: 1.01x slower                                                |
| scimark_fft                   | 199 ms                                                                 | 202 ms: 1.01x slower                                                 |
| Geometric mean                | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (61): asyncio_tcp, async_tree_eager_io_tg, unpack_sequence, xml_etree_parse, asyncio_tcp_ssl, sqlglot_transpile, sympy_str, async_tree_cpu_io_mixed, logging_silent, deepcopy_reduce, pylint, async_tree_eager_memoization_tg, json_loads, html5lib, async_tree_eager_memoization, async_tree_cpu_io_mixed_tg, async_tree_none_tg, thrift, sqlglot_parse, async_tree_io_tg, logging_simple, sympy_integrate, nbody, deepcopy_memo, async_tree_eager_io, scimark_sor, json, mypy2, regex_dna, async_tree_memoization, async_tree_eager_cpu_io_mixed_tg, regex_v8, genshi_text, telco, async_tree_eager_tg, python_startup, coverage, pidigits, dask, xml_etree_generate, python_startup_no_site, gunicorn, async_generators, generators, pickle_pure_python, regex_effbot, docutils, pickle_dict, spectral_norm, async_tree_io, sympy_sum, pickle_list, 2to3, unpickle_list, tomli_loads, async_tree_none, dulwich_log, bench_mp_pool, tornado_http, async_tree_memoization_tg, aiohttp

# HPT report

- Reliability score: 99.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x