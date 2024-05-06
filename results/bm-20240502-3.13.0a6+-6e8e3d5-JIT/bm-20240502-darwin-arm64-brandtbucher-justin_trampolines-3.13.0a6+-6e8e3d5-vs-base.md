# Results vs. base

- fork: brandtbucher
- ref: justin_trampolines
- machine: darwin-arm64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 171 ms                                                                 | 170 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (4): chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 334 ms: 1.00x slower                                                       |
| async_tree_eager_tg              | 42.8 ms                                                                | 43.1 ms: 1.01x slower                                                      |
| async_tree_eager                 | 64.4 ms                                                                | 64.8 ms: 1.01x slower                                                      |
| Geometric mean                   | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (13): async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_eager_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 68.0 ms                                                                | 67.8 ms: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 72.7 ms                                                                | 71.5 ms: 1.02x faster                                                      |
| regex_effbot   | 2.59 ms                                                                | 2.57 ms: 1.01x faster                                                      |
| regex_v8       | 17.4 ms                                                                | 17.3 ms: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 131 us                                                                 | 129 us: 1.02x faster                                                       |
| tomli_loads          | 1.24 sec                                                               | 1.22 sec: 1.02x faster                                                     |
| xml_etree_process    | 36.0 ms                                                                | 35.7 ms: 1.01x faster                                                      |
| pickle               | 7.26 us                                                                | 7.20 us: 1.01x faster                                                      |
| json_dumps           | 6.30 ms                                                                | 6.32 ms: 1.00x slower                                                      |
| json_loads           | 16.9 us                                                                | 17.0 us: 1.00x slower                                                      |
| xml_etree_generate   | 52.5 ms                                                                | 53.3 ms: 1.01x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (7): xml_etree_iterparse, pickle_list, pickle_pure_python, unpickle, unpickle_list, pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 14.5 ms: 1.01x faster                                                      |
| python_startup_no_site | 11.8 ms                                                                | 11.7 ms: 1.01x faster                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 18.0 ms                                                                | 17.4 ms: 1.04x faster                                                      |
| django_template | 21.5 ms                                                                | 21.2 ms: 1.01x faster                                                      |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pprint_pformat                   | 992 ms                                                                 | 922 ms: 1.08x faster                                                       |
| pprint_safe_repr                 | 476 ms                                                                 | 449 ms: 1.06x faster                                                       |
| genshi_text                      | 18.0 ms                                                                | 17.4 ms: 1.04x faster                                                      |
| scimark_monte_carlo              | 44.8 ms                                                                | 43.7 ms: 1.03x faster                                                      |
| fannkuch                         | 239 ms                                                                 | 233 ms: 1.02x faster                                                       |
| hexiom                           | 4.46 ms                                                                | 4.36 ms: 1.02x faster                                                      |
| comprehensions                   | 12.4 us                                                                | 12.1 us: 1.02x faster                                                      |
| regex_compile                    | 72.7 ms                                                                | 71.5 ms: 1.02x faster                                                      |
| unpickle_pure_python             | 131 us                                                                 | 129 us: 1.02x faster                                                       |
| richards                         | 29.7 ms                                                                | 29.2 ms: 1.02x faster                                                      |
| tomli_loads                      | 1.24 sec                                                               | 1.22 sec: 1.02x faster                                                     |
| django_template                  | 21.5 ms                                                                | 21.2 ms: 1.01x faster                                                      |
| sqlglot_normalize                | 176 ms                                                                 | 174 ms: 1.01x faster                                                       |
| richards_super                   | 33.4 ms                                                                | 32.9 ms: 1.01x faster                                                      |
| typing_runtime_protocols         | 103 us                                                                 | 102 us: 1.01x faster                                                       |
| chaos                            | 40.1 ms                                                                | 39.6 ms: 1.01x faster                                                      |
| sqlglot_optimize                 | 33.4 ms                                                                | 33.1 ms: 1.01x faster                                                      |
| meteor_contest                   | 73.3 ms                                                                | 72.5 ms: 1.01x faster                                                      |
| scimark_lu                       | 79.5 ms                                                                | 78.8 ms: 1.01x faster                                                      |
| regex_effbot                     | 2.59 ms                                                                | 2.57 ms: 1.01x faster                                                      |
| sqlglot_transpile                | 950 us                                                                 | 943 us: 1.01x faster                                                       |
| xml_etree_process                | 36.0 ms                                                                | 35.7 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult          | 3.01 ms                                                                | 2.98 ms: 1.01x faster                                                      |
| pickle                           | 7.26 us                                                                | 7.20 us: 1.01x faster                                                      |
| python_startup                   | 14.7 ms                                                                | 14.5 ms: 1.01x faster                                                      |
| pyflate                          | 316 ms                                                                 | 314 ms: 1.01x faster                                                       |
| spectral_norm                    | 70.6 ms                                                                | 70.1 ms: 1.01x faster                                                      |
| python_startup_no_site           | 11.8 ms                                                                | 11.7 ms: 1.01x faster                                                      |
| dulwich_log                      | 29.1 ms                                                                | 29.0 ms: 1.01x faster                                                      |
| scimark_sor                      | 104 ms                                                                 | 103 ms: 1.01x faster                                                       |
| 2to3                             | 171 ms                                                                 | 170 ms: 1.01x faster                                                       |
| bench_thread_pool                | 483 us                                                                 | 481 us: 1.01x faster                                                       |
| sympy_str                        | 138 ms                                                                 | 137 ms: 1.01x faster                                                       |
| deepcopy                         | 212 us                                                                 | 211 us: 1.01x faster                                                       |
| nqueens                          | 57.8 ms                                                                | 57.5 ms: 1.00x faster                                                      |
| coverage                         | 45.6 ms                                                                | 45.4 ms: 1.00x faster                                                      |
| sympy_expand                     | 236 ms                                                                 | 235 ms: 1.00x faster                                                       |
| sqlglot_parse                    | 779 us                                                                 | 777 us: 1.00x faster                                                       |
| sympy_integrate                  | 11.0 ms                                                                | 10.9 ms: 1.00x faster                                                      |
| nbody                            | 68.0 ms                                                                | 67.8 ms: 1.00x faster                                                      |
| mdp                              | 1.52 sec                                                               | 1.52 sec: 1.00x faster                                                     |
| deepcopy_memo                    | 23.5 us                                                                | 23.4 us: 1.00x faster                                                      |
| raytrace                         | 170 ms                                                                 | 170 ms: 1.00x faster                                                       |
| regex_v8                         | 17.4 ms                                                                | 17.3 ms: 1.00x faster                                                      |
| gc_traversal                     | 2.45 ms                                                                | 2.46 ms: 1.00x slower                                                      |
| async_tree_eager_cpu_io_mixed_tg | 334 ms                                                                 | 334 ms: 1.00x slower                                                       |
| logging_simple                   | 3.12 us                                                                | 3.13 us: 1.00x slower                                                      |
| sqlite_synth                     | 1.57 us                                                                | 1.58 us: 1.00x slower                                                      |
| json_dumps                       | 6.30 ms                                                                | 6.32 ms: 1.00x slower                                                      |
| logging_format                   | 3.39 us                                                                | 3.41 us: 1.00x slower                                                      |
| json_loads                       | 16.9 us                                                                | 17.0 us: 1.00x slower                                                      |
| async_generators                 | 290 ms                                                                 | 291 ms: 1.00x slower                                                       |
| async_tree_eager_tg              | 42.8 ms                                                                | 43.1 ms: 1.01x slower                                                      |
| create_gc_cycles                 | 901 us                                                                 | 906 us: 1.01x slower                                                       |
| async_tree_eager                 | 64.4 ms                                                                | 64.8 ms: 1.01x slower                                                      |
| xml_etree_generate               | 52.5 ms                                                                | 53.3 ms: 1.01x slower                                                      |
| thrift                           | 439 us                                                                 | 447 us: 1.02x slower                                                       |
| Geometric mean                   | (ref)                                                                  | 1.01x faster                                                               |

Benchmark hidden because not significant (51): tornado_http, asyncio_tcp, aiohttp, bench_mp_pool, pathlib, async_tree_io, float, xml_etree_iterparse, gunicorn, pickle_list, pylint, html5lib, coroutines, pickle_pure_python, docutils, unpickle, async_tree_memoization_tg, scimark_fft, sympy_sum, unpickle_list, pickle_dict, asyncio_tcp_ssl, go, async_tree_cpu_io_mixed, async_tree_none, telco, async_tree_none_tg, async_tree_eager_memoization_tg, deepcopy_reduce, pidigits, asyncio_websockets, mako, async_tree_eager_cpu_io_mixed, deltablue, pycparser, async_tree_memoization, regex_dna, async_tree_cpu_io_mixed_tg, logging_silent, async_tree_io_tg, crypto_pyaes, async_tree_eager_io_tg, generators, json, async_tree_eager_memoization, genshi_xml, chameleon, async_tree_eager_io, dask, xml_etree_parse, mypy2

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x