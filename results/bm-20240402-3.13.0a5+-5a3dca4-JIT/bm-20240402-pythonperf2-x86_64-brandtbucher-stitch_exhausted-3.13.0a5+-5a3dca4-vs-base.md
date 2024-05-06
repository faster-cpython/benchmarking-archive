# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 306 ms: 1.03x slower                                                           |
| chameleon      | 7.35 ms                                                                      | 7.57 ms: 1.03x slower                                                          |
| docutils       | 3.07 sec                                                                     | 3.13 sec: 1.02x slower                                                         |
| html5lib       | 72.7 ms                                                                      | 74.3 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                        | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 595 ms                                                                       | 601 ms: 1.01x slower                                                           |
| Geometric mean          | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 97.5 ms                                                                      | 96.8 ms: 1.01x faster                                                          |
| pidigits       | 261 ms                                                                       | 261 ms: 1.00x slower                                                           |
| float          | 77.8 ms                                                                      | 79.0 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                      | 25.7 ms: 1.01x faster                                                          |
| regex_dna      | 238 ms                                                                       | 240 ms: 1.01x slower                                                           |
| regex_effbot   | 3.48 ms                                                                      | 3.60 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_list        | 4.74 us                                                                      | 4.61 us: 1.03x faster                                                          |
| xml_etree_generate   | 84.6 ms                                                                      | 82.7 ms: 1.02x faster                                                          |
| xml_etree_iterparse  | 103 ms                                                                       | 102 ms: 1.01x faster                                                           |
| unpickle             | 15.2 us                                                                      | 15.1 us: 1.01x faster                                                          |
| unpickle_pure_python | 232 us                                                                       | 230 us: 1.01x faster                                                           |
| json_dumps           | 10.6 ms                                                                      | 10.7 ms: 1.01x slower                                                          |
| pickle_list          | 4.31 us                                                                      | 4.50 us: 1.04x slower                                                          |
| pickle_dict          | 30.8 us                                                                      | 33.0 us: 1.07x slower                                                          |
| Geometric mean       | (ref)                                                                        | 1.00x slower                                                                   |

Benchmark hidden because not significant (6): xml_etree_parse, xml_etree_process, json_loads, tomli_loads, pickle_pure_python, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                          |
| python_startup         | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                                          |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 9.97 ms                                                                      | 9.90 ms: 1.01x faster                                                          |
| django_template | 39.4 ms                                                                      | 40.9 ms: 1.04x slower                                                          |
| genshi_xml      | 57.0 ms                                                                      | 59.9 ms: 1.05x slower                                                          |
| genshi_text     | 26.0 ms                                                                      | 28.0 ms: 1.08x slower                                                          |
| Geometric mean  | (ref)                                                                        | 1.04x slower                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| gc_traversal             | 4.60 ms                                                                      | 4.35 ms: 1.06x faster                                                          |
| scimark_sparse_mat_mult  | 4.30 ms                                                                      | 4.14 ms: 1.04x faster                                                          |
| unpickle_list            | 4.74 us                                                                      | 4.61 us: 1.03x faster                                                          |
| xml_etree_generate       | 84.6 ms                                                                      | 82.7 ms: 1.02x faster                                                          |
| richards                 | 51.7 ms                                                                      | 50.5 ms: 1.02x faster                                                          |
| scimark_fft              | 322 ms                                                                       | 317 ms: 1.02x faster                                                           |
| coroutines               | 22.5 ms                                                                      | 22.2 ms: 1.02x faster                                                          |
| dulwich_log              | 69.9 ms                                                                      | 68.9 ms: 1.01x faster                                                          |
| unpack_sequence          | 60.3 ns                                                                      | 59.5 ns: 1.01x faster                                                          |
| xml_etree_iterparse      | 103 ms                                                                       | 102 ms: 1.01x faster                                                           |
| regex_v8                 | 26.1 ms                                                                      | 25.7 ms: 1.01x faster                                                          |
| unpickle                 | 15.2 us                                                                      | 15.1 us: 1.01x faster                                                          |
| asyncio_websockets       | 387 ms                                                                       | 384 ms: 1.01x faster                                                           |
| nbody                    | 97.5 ms                                                                      | 96.8 ms: 1.01x faster                                                          |
| mako                     | 9.97 ms                                                                      | 9.90 ms: 1.01x faster                                                          |
| unpickle_pure_python     | 232 us                                                                       | 230 us: 1.01x faster                                                           |
| generators               | 33.7 ms                                                                      | 33.5 ms: 1.00x faster                                                          |
| pidigits                 | 261 ms                                                                       | 261 ms: 1.00x slower                                                           |
| python_startup_no_site   | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                          |
| python_startup           | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                                          |
| asyncio_tcp_ssl          | 1.57 sec                                                                     | 1.58 sec: 1.01x slower                                                         |
| pprint_pformat           | 1.72 sec                                                                     | 1.73 sec: 1.01x slower                                                         |
| logging_simple           | 6.59 us                                                                      | 6.63 us: 1.01x slower                                                          |
| fannkuch                 | 380 ms                                                                       | 383 ms: 1.01x slower                                                           |
| asyncio_tcp              | 371 ms                                                                       | 375 ms: 1.01x slower                                                           |
| regex_dna                | 238 ms                                                                       | 240 ms: 1.01x slower                                                           |
| spectral_norm            | 92.9 ms                                                                      | 94.0 ms: 1.01x slower                                                          |
| mdp                      | 2.62 sec                                                                     | 2.65 sec: 1.01x slower                                                         |
| async_tree_cpu_io_mixed  | 595 ms                                                                       | 601 ms: 1.01x slower                                                           |
| deepcopy_memo            | 37.9 us                                                                      | 38.4 us: 1.01x slower                                                          |
| dask                     | 402 ms                                                                       | 407 ms: 1.01x slower                                                           |
| sqlglot_transpile        | 1.81 ms                                                                      | 1.84 ms: 1.01x slower                                                          |
| scimark_sor              | 154 ms                                                                       | 156 ms: 1.01x slower                                                           |
| pathlib                  | 19.6 ms                                                                      | 19.8 ms: 1.01x slower                                                          |
| json_dumps               | 10.6 ms                                                                      | 10.7 ms: 1.01x slower                                                          |
| logging_format           | 7.21 us                                                                      | 7.32 us: 1.01x slower                                                          |
| thrift                   | 864 us                                                                       | 878 us: 1.02x slower                                                           |
| float                    | 77.8 ms                                                                      | 79.0 ms: 1.02x slower                                                          |
| create_gc_cycles         | 1.78 ms                                                                      | 1.81 ms: 1.02x slower                                                          |
| deltablue                | 3.72 ms                                                                      | 3.79 ms: 1.02x slower                                                          |
| docutils                 | 3.07 sec                                                                     | 3.13 sec: 1.02x slower                                                         |
| sympy_str                | 303 ms                                                                       | 310 ms: 1.02x slower                                                           |
| meteor_contest           | 132 ms                                                                       | 135 ms: 1.02x slower                                                           |
| html5lib                 | 72.7 ms                                                                      | 74.3 ms: 1.02x slower                                                          |
| json                     | 5.39 ms                                                                      | 5.51 ms: 1.02x slower                                                          |
| go                       | 173 ms                                                                       | 177 ms: 1.02x slower                                                           |
| bench_thread_pool        | 1.10 ms                                                                      | 1.13 ms: 1.02x slower                                                          |
| sympy_sum                | 161 ms                                                                       | 165 ms: 1.02x slower                                                           |
| hexiom                   | 7.54 ms                                                                      | 7.73 ms: 1.02x slower                                                          |
| pyflate                  | 515 ms                                                                       | 528 ms: 1.03x slower                                                           |
| aiohttp                  | 1.12 ms                                                                      | 1.15 ms: 1.03x slower                                                          |
| 2to3                     | 298 ms                                                                       | 306 ms: 1.03x slower                                                           |
| comprehensions           | 19.7 us                                                                      | 20.2 us: 1.03x slower                                                          |
| mypy2                    | 827 ms                                                                       | 852 ms: 1.03x slower                                                           |
| chameleon                | 7.35 ms                                                                      | 7.57 ms: 1.03x slower                                                          |
| scimark_monte_carlo      | 73.7 ms                                                                      | 75.9 ms: 1.03x slower                                                          |
| chaos                    | 66.9 ms                                                                      | 69.0 ms: 1.03x slower                                                          |
| pylint                   | 335 ms                                                                       | 345 ms: 1.03x slower                                                           |
| sympy_expand             | 509 ms                                                                       | 526 ms: 1.03x slower                                                           |
| sqlglot_optimize         | 62.6 ms                                                                      | 64.7 ms: 1.03x slower                                                          |
| gunicorn                 | 1.09 ms                                                                      | 1.12 ms: 1.03x slower                                                          |
| regex_effbot             | 3.48 ms                                                                      | 3.60 ms: 1.03x slower                                                          |
| sympy_integrate          | 25.2 ms                                                                      | 26.1 ms: 1.04x slower                                                          |
| pycparser                | 1.25 sec                                                                     | 1.29 sec: 1.04x slower                                                         |
| django_template          | 39.4 ms                                                                      | 40.9 ms: 1.04x slower                                                          |
| sqlglot_normalize        | 122 ms                                                                       | 127 ms: 1.04x slower                                                           |
| deepcopy                 | 385 us                                                                       | 401 us: 1.04x slower                                                           |
| pickle_list              | 4.31 us                                                                      | 4.50 us: 1.04x slower                                                          |
| typing_runtime_protocols | 117 us                                                                       | 123 us: 1.04x slower                                                           |
| raytrace                 | 302 ms                                                                       | 316 ms: 1.05x slower                                                           |
| genshi_xml               | 57.0 ms                                                                      | 59.9 ms: 1.05x slower                                                          |
| deepcopy_reduce          | 3.35 us                                                                      | 3.52 us: 1.05x slower                                                          |
| coverage                 | 79.0 ms                                                                      | 84.3 ms: 1.07x slower                                                          |
| pickle_dict              | 30.8 us                                                                      | 33.0 us: 1.07x slower                                                          |
| genshi_text              | 26.0 ms                                                                      | 28.0 ms: 1.08x slower                                                          |
| Geometric mean           | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (26): bench_mp_pool, pprint_safe_repr, regex_compile, xml_etree_parse, xml_etree_process, nqueens, async_generators, richards_super, tornado_http, sqlite_synth, logging_silent, json_loads, tomli_loads, scimark_lu, pickle_pure_python, async_tree_cpu_io_mixed_tg, telco, sqlglot_parse, async_tree_memoization_tg, crypto_pyaes, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization, async_tree_none, pickle

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x