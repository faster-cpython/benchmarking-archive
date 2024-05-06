# Results vs. base

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 23cf5de
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 268 ms: 1.00x slower                                                             |
| chameleon      | 6.92 ms                                                                | 7.00 ms: 1.01x slower                                                            |
| docutils       | 2.77 sec                                                               | 2.79 sec: 1.01x slower                                                           |
| html5lib       | 66.8 ms                                                                | 68.0 ms: 1.02x slower                                                            |
| tornado_http   | 93.9 ms                                                                | 94.8 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.7 ms                                                                | 81.7 ms: 1.04x slower                                                            |
| pidigits       | 191 ms                                                                 | 199 ms: 1.04x slower                                                             |
| nbody          | 88.5 ms                                                                | 118 ms: 1.34x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.5 ms                                                                | 24.8 ms: 1.03x faster                                                            |
| regex_effbot   | 3.72 ms                                                                | 3.62 ms: 1.03x faster                                                            |
| regex_dna      | 224 ms                                                                 | 220 ms: 1.02x faster                                                             |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 5.04 us: 1.06x faster                                                            |
| pickle_dict          | 35.4 us                                                                | 34.3 us: 1.03x faster                                                            |
| pickle               | 11.9 us                                                                | 11.6 us: 1.03x faster                                                            |
| unpickle             | 15.4 us                                                                | 15.2 us: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                                 | 219 us: 1.00x slower                                                             |
| json_loads           | 28.6 us                                                                | 28.7 us: 1.00x slower                                                            |
| xml_etree_iterparse  | 106 ms                                                                 | 108 ms: 1.01x slower                                                             |
| xml_etree_generate   | 86.4 ms                                                                | 87.5 ms: 1.01x slower                                                            |
| unpickle_list        | 4.97 us                                                                | 5.24 us: 1.05x slower                                                            |
| tomli_loads          | 2.15 sec                                                               | 2.30 sec: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (4): xml_etree_parse, json_dumps, pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 8.99 ms: 1.00x faster                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                                | 51.5 ms: 1.01x faster                                                            |
| mako           | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list              | 5.33 us                                                                | 5.04 us: 1.06x faster                                                            |
| gc_traversal             | 3.94 ms                                                                | 3.73 ms: 1.06x faster                                                            |
| pickle_dict              | 35.4 us                                                                | 34.3 us: 1.03x faster                                                            |
| pycparser                | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                                           |
| regex_v8                 | 25.5 ms                                                                | 24.8 ms: 1.03x faster                                                            |
| regex_effbot             | 3.72 ms                                                                | 3.62 ms: 1.03x faster                                                            |
| pickle                   | 11.9 us                                                                | 11.6 us: 1.03x faster                                                            |
| regex_dna                | 224 ms                                                                 | 220 ms: 1.02x faster                                                             |
| create_gc_cycles         | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                                            |
| unpickle                 | 15.4 us                                                                | 15.2 us: 1.01x faster                                                            |
| logging_silent           | 101 ns                                                                 | 100 ns: 1.01x faster                                                             |
| typing_runtime_protocols | 115 us                                                                 | 114 us: 1.01x faster                                                             |
| genshi_xml               | 51.8 ms                                                                | 51.5 ms: 1.01x faster                                                            |
| python_startup_no_site   | 9.00 ms                                                                | 8.99 ms: 1.00x faster                                                            |
| pylint                   | 277 ms                                                                 | 278 ms: 1.00x slower                                                             |
| asyncio_tcp              | 505 ms                                                                 | 506 ms: 1.00x slower                                                             |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| unpickle_pure_python     | 218 us                                                                 | 219 us: 1.00x slower                                                             |
| json_loads               | 28.6 us                                                                | 28.7 us: 1.00x slower                                                            |
| bench_thread_pool        | 826 us                                                                 | 829 us: 1.00x slower                                                             |
| pprint_pformat           | 1.50 sec                                                               | 1.51 sec: 1.00x slower                                                           |
| 2to3                     | 267 ms                                                                 | 268 ms: 1.00x slower                                                             |
| mako                     | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                            |
| crypto_pyaes             | 73.0 ms                                                                | 73.5 ms: 1.01x slower                                                            |
| docutils                 | 2.77 sec                                                               | 2.79 sec: 1.01x slower                                                           |
| aiohttp                  | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                            |
| sqlglot_optimize         | 54.4 ms                                                                | 54.9 ms: 1.01x slower                                                            |
| generators               | 29.3 ms                                                                | 29.6 ms: 1.01x slower                                                            |
| sqlglot_transpile        | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                                            |
| comprehensions           | 16.3 us                                                                | 16.5 us: 1.01x slower                                                            |
| tornado_http             | 93.9 ms                                                                | 94.8 ms: 1.01x slower                                                            |
| thrift                   | 799 us                                                                 | 808 us: 1.01x slower                                                             |
| chameleon                | 6.92 ms                                                                | 7.00 ms: 1.01x slower                                                            |
| xml_etree_iterparse      | 106 ms                                                                 | 108 ms: 1.01x slower                                                             |
| xml_etree_generate       | 86.4 ms                                                                | 87.5 ms: 1.01x slower                                                            |
| dulwich_log              | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| regex_compile            | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| deepcopy_reduce          | 3.17 us                                                                | 3.21 us: 1.01x slower                                                            |
| deepcopy_memo            | 37.8 us                                                                | 38.3 us: 1.01x slower                                                            |
| coverage                 | 96.9 ms                                                                | 98.3 ms: 1.01x slower                                                            |
| sympy_sum                | 153 ms                                                                 | 156 ms: 1.01x slower                                                             |
| sympy_integrate          | 20.0 ms                                                                | 20.3 ms: 1.01x slower                                                            |
| sympy_str                | 275 ms                                                                 | 279 ms: 1.01x slower                                                             |
| sqlglot_normalize        | 109 ms                                                                 | 110 ms: 1.02x slower                                                             |
| html5lib                 | 66.8 ms                                                                | 68.0 ms: 1.02x slower                                                            |
| sympy_expand             | 462 ms                                                                 | 470 ms: 1.02x slower                                                             |
| telco                    | 8.41 ms                                                                | 8.56 ms: 1.02x slower                                                            |
| sqlglot_parse            | 1.27 ms                                                                | 1.29 ms: 1.02x slower                                                            |
| mdp                      | 2.73 sec                                                               | 2.80 sec: 1.03x slower                                                           |
| logging_simple           | 5.67 us                                                                | 5.83 us: 1.03x slower                                                            |
| hexiom                   | 6.21 ms                                                                | 6.39 ms: 1.03x slower                                                            |
| richards_super           | 51.6 ms                                                                | 53.1 ms: 1.03x slower                                                            |
| go                       | 141 ms                                                                 | 146 ms: 1.03x slower                                                             |
| richards                 | 45.5 ms                                                                | 47.0 ms: 1.03x slower                                                            |
| coroutines               | 23.1 ms                                                                | 23.9 ms: 1.04x slower                                                            |
| float                    | 78.7 ms                                                                | 81.7 ms: 1.04x slower                                                            |
| fannkuch                 | 397 ms                                                                 | 413 ms: 1.04x slower                                                             |
| deltablue                | 3.14 ms                                                                | 3.27 ms: 1.04x slower                                                            |
| pyflate                  | 461 ms                                                                 | 480 ms: 1.04x slower                                                             |
| pidigits                 | 191 ms                                                                 | 199 ms: 1.04x slower                                                             |
| logging_format           | 6.26 us                                                                | 6.54 us: 1.04x slower                                                            |
| nqueens                  | 80.6 ms                                                                | 84.2 ms: 1.04x slower                                                            |
| unpickle_list            | 4.97 us                                                                | 5.24 us: 1.05x slower                                                            |
| scimark_sor              | 129 ms                                                                 | 137 ms: 1.06x slower                                                             |
| tomli_loads              | 2.15 sec                                                               | 2.30 sec: 1.07x slower                                                           |
| scimark_lu               | 112 ms                                                                 | 121 ms: 1.07x slower                                                             |
| raytrace                 | 258 ms                                                                 | 279 ms: 1.08x slower                                                             |
| scimark_monte_carlo      | 67.7 ms                                                                | 74.0 ms: 1.09x slower                                                            |
| chaos                    | 59.9 ms                                                                | 68.6 ms: 1.15x slower                                                            |
| scimark_fft              | 359 ms                                                                 | 428 ms: 1.19x slower                                                             |
| scimark_sparse_mat_mult  | 4.99 ms                                                                | 6.14 ms: 1.23x slower                                                            |
| spectral_norm            | 110 ms                                                                 | 138 ms: 1.25x slower                                                             |
| nbody                    | 88.5 ms                                                                | 118 ms: 1.34x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (26): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, xml_etree_parse, genshi_text, async_tree_memoization_tg, json_dumps, pickle_pure_python, async_tree_io_tg, async_tree_memoization, bench_mp_pool, pprint_safe_repr, asyncio_websockets, deepcopy, asyncio_tcp_ssl, pathlib, async_generators, async_tree_none_tg, meteor_contest, xml_etree_process, dask, sqlite_synth, gunicorn, async_tree_none, mypy2, json

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x