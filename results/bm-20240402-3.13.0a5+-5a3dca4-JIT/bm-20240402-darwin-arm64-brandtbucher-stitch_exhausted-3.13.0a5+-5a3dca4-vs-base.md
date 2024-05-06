# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 174 ms                                                                 | 176 ms: 1.01x slower                                                     |
| chameleon      | 4.53 ms                                                                | 4.47 ms: 1.01x faster                                                    |
| docutils       | 1.56 sec                                                               | 1.58 sec: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 355 ms                                                                 | 356 ms: 1.00x slower                                                     |
| async_tree_eager              | 66.1 ms                                                                | 66.9 ms: 1.01x slower                                                    |
| Geometric mean                | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (14): async_tree_eager_io_tg, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_none, async_tree_io, async_tree_eager_memoization, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                                | 70.0 ms: 1.00x faster                                                    |
| pidigits       | 282 ms                                                                 | 283 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 80.9 ms                                                                | 87.2 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 107 ms                                                                 | 98.3 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 72.5 ms                                                                | 68.5 ms: 1.06x faster                                                    |
| unpickle_list        | 3.09 us                                                                | 3.04 us: 1.01x faster                                                    |
| xml_etree_generate   | 54.7 ms                                                                | 54.1 ms: 1.01x faster                                                    |
| xml_etree_process    | 36.8 ms                                                                | 36.5 ms: 1.01x faster                                                    |
| json_dumps           | 6.32 ms                                                                | 6.28 ms: 1.01x faster                                                    |
| pickle_dict          | 18.1 us                                                                | 18.0 us: 1.00x faster                                                    |
| pickle_pure_python   | 183 us                                                                 | 183 us: 1.00x faster                                                     |
| json_loads           | 17.0 us                                                                | 17.1 us: 1.00x slower                                                    |
| unpickle_pure_python | 143 us                                                                 | 143 us: 1.00x slower                                                     |
| pickle               | 7.40 us                                                                | 7.47 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                    |
| python_startup         | 13.4 ms                                                                | 13.4 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 14.9 ms                                                                | 14.7 ms: 1.02x faster                                                    |
| django_template | 20.7 ms                                                                | 21.3 ms: 1.03x slower                                                    |
| genshi_xml      | 31.5 ms                                                                | 32.7 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                     | bm-20240329-darwin-arm64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse               | 107 ms                                                                 | 98.3 ms: 1.09x faster                                                    |
| xml_etree_iterparse           | 72.5 ms                                                                | 68.5 ms: 1.06x faster                                                    |
| richards                      | 32.0 ms                                                                | 31.2 ms: 1.02x faster                                                    |
| genshi_text                   | 14.9 ms                                                                | 14.7 ms: 1.02x faster                                                    |
| richards_super                | 35.3 ms                                                                | 34.8 ms: 1.01x faster                                                    |
| chameleon                     | 4.53 ms                                                                | 4.47 ms: 1.01x faster                                                    |
| unpickle_list                 | 3.09 us                                                                | 3.04 us: 1.01x faster                                                    |
| pathlib                       | 25.1 ms                                                                | 24.7 ms: 1.01x faster                                                    |
| xml_etree_generate            | 54.7 ms                                                                | 54.1 ms: 1.01x faster                                                    |
| coverage                      | 46.8 ms                                                                | 46.4 ms: 1.01x faster                                                    |
| json                          | 2.97 ms                                                                | 2.95 ms: 1.01x faster                                                    |
| xml_etree_process             | 36.8 ms                                                                | 36.5 ms: 1.01x faster                                                    |
| json_dumps                    | 6.32 ms                                                                | 6.28 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult       | 3.15 ms                                                                | 3.13 ms: 1.01x faster                                                    |
| scimark_lu                    | 82.0 ms                                                                | 81.5 ms: 1.01x faster                                                    |
| python_startup_no_site        | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                    |
| nbody                         | 70.3 ms                                                                | 70.0 ms: 1.00x faster                                                    |
| pickle_dict                   | 18.1 us                                                                | 18.0 us: 1.00x faster                                                    |
| pickle_pure_python            | 183 us                                                                 | 183 us: 1.00x faster                                                     |
| logging_simple                | 3.30 us                                                                | 3.29 us: 1.00x faster                                                    |
| python_startup                | 13.4 ms                                                                | 13.4 ms: 1.00x faster                                                    |
| asyncio_websockets            | 408 ms                                                                 | 409 ms: 1.00x slower                                                     |
| pidigits                      | 282 ms                                                                 | 283 ms: 1.00x slower                                                     |
| scimark_sor                   | 107 ms                                                                 | 108 ms: 1.00x slower                                                     |
| sqlite_synth                  | 1.58 us                                                                | 1.58 us: 1.00x slower                                                    |
| json_loads                    | 17.0 us                                                                | 17.1 us: 1.00x slower                                                    |
| create_gc_cycles              | 845 us                                                                 | 847 us: 1.00x slower                                                     |
| deltablue                     | 2.36 ms                                                                | 2.37 ms: 1.00x slower                                                    |
| unpickle_pure_python          | 143 us                                                                 | 143 us: 1.00x slower                                                     |
| async_generators              | 300 ms                                                                 | 301 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed | 355 ms                                                                 | 356 ms: 1.00x slower                                                     |
| logging_format                | 3.58 us                                                                | 3.59 us: 1.00x slower                                                    |
| comprehensions                | 12.1 us                                                                | 12.1 us: 1.01x slower                                                    |
| crypto_pyaes                  | 47.2 ms                                                                | 47.5 ms: 1.01x slower                                                    |
| fannkuch                      | 256 ms                                                                 | 258 ms: 1.01x slower                                                     |
| thrift                        | 434 us                                                                 | 437 us: 1.01x slower                                                     |
| deepcopy                      | 214 us                                                                 | 215 us: 1.01x slower                                                     |
| sqlglot_transpile             | 936 us                                                                 | 944 us: 1.01x slower                                                     |
| meteor_contest                | 73.8 ms                                                                | 74.4 ms: 1.01x slower                                                    |
| pyflate                       | 332 ms                                                                 | 335 ms: 1.01x slower                                                     |
| pickle                        | 7.40 us                                                                | 7.47 us: 1.01x slower                                                    |
| dulwich_log                   | 29.9 ms                                                                | 30.2 ms: 1.01x slower                                                    |
| async_tree_eager              | 66.1 ms                                                                | 66.9 ms: 1.01x slower                                                    |
| 2to3                          | 174 ms                                                                 | 176 ms: 1.01x slower                                                     |
| raytrace                      | 179 ms                                                                 | 181 ms: 1.01x slower                                                     |
| bench_mp_pool                 | 46.5 ms                                                                | 47.0 ms: 1.01x slower                                                    |
| typing_runtime_protocols      | 69.0 us                                                                | 69.9 us: 1.01x slower                                                    |
| nqueens                       | 60.7 ms                                                                | 61.6 ms: 1.01x slower                                                    |
| dask                          | 222 ms                                                                 | 226 ms: 1.01x slower                                                     |
| sqlglot_normalize             | 175 ms                                                                 | 178 ms: 1.02x slower                                                     |
| bench_thread_pool             | 493 us                                                                 | 501 us: 1.02x slower                                                     |
| docutils                      | 1.56 sec                                                               | 1.58 sec: 1.02x slower                                                   |
| go                            | 105 ms                                                                 | 107 ms: 1.02x slower                                                     |
| chaos                         | 38.7 ms                                                                | 39.4 ms: 1.02x slower                                                    |
| sqlglot_optimize              | 33.7 ms                                                                | 34.4 ms: 1.02x slower                                                    |
| sympy_expand                  | 236 ms                                                                 | 241 ms: 1.02x slower                                                     |
| sympy_str                     | 140 ms                                                                 | 143 ms: 1.02x slower                                                     |
| pylint                        | 156 ms                                                                 | 159 ms: 1.02x slower                                                     |
| django_template               | 20.7 ms                                                                | 21.3 ms: 1.03x slower                                                    |
| sympy_sum                     | 75.4 ms                                                                | 77.9 ms: 1.03x slower                                                    |
| scimark_monte_carlo           | 44.4 ms                                                                | 45.9 ms: 1.03x slower                                                    |
| mypy2                         | 411 ms                                                                 | 426 ms: 1.03x slower                                                     |
| genshi_xml                    | 31.5 ms                                                                | 32.7 ms: 1.04x slower                                                    |
| sympy_integrate               | 11.3 ms                                                                | 11.7 ms: 1.04x slower                                                    |
| hexiom                        | 4.99 ms                                                                | 5.28 ms: 1.06x slower                                                    |
| pprint_pformat                | 1.01 sec                                                               | 1.07 sec: 1.06x slower                                                   |
| pprint_safe_repr              | 489 ms                                                                 | 527 ms: 1.08x slower                                                     |
| regex_compile                 | 80.9 ms                                                                | 87.2 ms: 1.08x slower                                                    |
| Geometric mean                | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (41): async_tree_eager_io_tg, regex_effbot, logging_silent, unpack_sequence, tomli_loads, asyncio_tcp_ssl, generators, coroutines, async_tree_eager_tg, gc_traversal, deepcopy_reduce, async_tree_eager_cpu_io_mixed_tg, regex_dna, pycparser, float, async_tree_none_tg, telco, scimark_fft, sqlglot_parse, spectral_norm, async_tree_memoization_tg, mako, mdp, regex_v8, async_tree_io_tg, async_tree_eager_io, deepcopy_memo, async_tree_eager_memoization_tg, unpickle, async_tree_memoization, pickle_list, async_tree_none, async_tree_io, async_tree_eager_memoization, html5lib, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, aiohttp, asyncio_tcp, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x