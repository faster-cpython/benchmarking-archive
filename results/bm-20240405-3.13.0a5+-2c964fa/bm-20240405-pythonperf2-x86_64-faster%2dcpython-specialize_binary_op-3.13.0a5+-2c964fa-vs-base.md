# Results vs. base

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.00x slower
- HPT reliability: 95.31%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                                       | 288 ms: 1.01x faster                                                                   |
| chameleon      | 7.26 ms                                                                      | 7.47 ms: 1.03x slower                                                                  |
| docutils       | 2.99 sec                                                                     | 2.98 sec: 1.00x faster                                                                 |
| html5lib       | 74.5 ms                                                                      | 73.9 ms: 1.01x faster                                                                  |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 84.6 ms                                                                      | 91.4 ms: 1.08x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.03x slower                                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_v8       | 25.9 ms                                                                      | 25.4 ms: 1.02x faster                                                                  |
| regex_compile  | 142 ms                                                                       | 141 ms: 1.01x faster                                                                   |
| regex_effbot   | 3.47 ms                                                                      | 3.48 ms: 1.00x slower                                                                  |
| regex_dna      | 237 ms                                                                       | 240 ms: 1.01x slower                                                                   |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| tomli_loads          | 2.29 sec                                                                     | 2.20 sec: 1.04x faster                                                                 |
| unpickle             | 15.7 us                                                                      | 15.2 us: 1.04x faster                                                                  |
| pickle_pure_python   | 314 us                                                                       | 307 us: 1.02x faster                                                                   |
| unpickle_list        | 4.63 us                                                                      | 4.57 us: 1.01x faster                                                                  |
| xml_etree_generate   | 83.6 ms                                                                      | 82.6 ms: 1.01x faster                                                                  |
| xml_etree_process    | 58.2 ms                                                                      | 57.6 ms: 1.01x faster                                                                  |
| json_dumps           | 10.6 ms                                                                      | 10.6 ms: 1.01x faster                                                                  |
| pickle_list          | 4.26 us                                                                      | 4.29 us: 1.01x slower                                                                  |
| unpickle_pure_python | 216 us                                                                       | 221 us: 1.02x slower                                                                   |
| xml_etree_parse      | 144 ms                                                                       | 148 ms: 1.03x slower                                                                   |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                      | 11.0 ms: 1.00x faster                                                                  |
| python_startup         | 12.8 ms                                                                      | 12.8 ms: 1.00x faster                                                                  |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 10.2 ms                                                                      | 10.3 ms: 1.01x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240403-pythonperf2-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| spectral_norm            | 92.6 ms                                                                      | 88.4 ms: 1.05x faster                                                                  |
| tomli_loads              | 2.29 sec                                                                     | 2.20 sec: 1.04x faster                                                                 |
| unpickle                 | 15.7 us                                                                      | 15.2 us: 1.04x faster                                                                  |
| fannkuch                 | 391 ms                                                                       | 381 ms: 1.03x faster                                                                   |
| thrift                   | 888 us                                                                       | 867 us: 1.02x faster                                                                   |
| pprint_pformat           | 1.63 sec                                                                     | 1.60 sec: 1.02x faster                                                                 |
| scimark_sor              | 143 ms                                                                       | 139 ms: 1.02x faster                                                                   |
| pickle_pure_python       | 314 us                                                                       | 307 us: 1.02x faster                                                                   |
| deepcopy_reduce          | 3.51 us                                                                      | 3.43 us: 1.02x faster                                                                  |
| regex_v8                 | 25.9 ms                                                                      | 25.4 ms: 1.02x faster                                                                  |
| sympy_sum                | 156 ms                                                                       | 153 ms: 1.02x faster                                                                   |
| deepcopy_memo            | 37.8 us                                                                      | 37.2 us: 1.02x faster                                                                  |
| asyncio_tcp              | 375 ms                                                                       | 369 ms: 1.02x faster                                                                   |
| telco                    | 8.03 ms                                                                      | 7.91 ms: 1.02x faster                                                                  |
| typing_runtime_protocols | 117 us                                                                       | 116 us: 1.01x faster                                                                   |
| sqlglot_optimize         | 59.0 ms                                                                      | 58.1 ms: 1.01x faster                                                                  |
| unpickle_list            | 4.63 us                                                                      | 4.57 us: 1.01x faster                                                                  |
| comprehensions           | 16.8 us                                                                      | 16.5 us: 1.01x faster                                                                  |
| logging_silent           | 95.3 ns                                                                      | 94.0 ns: 1.01x faster                                                                  |
| pprint_safe_repr         | 795 ms                                                                       | 785 ms: 1.01x faster                                                                   |
| richards_super           | 59.0 ms                                                                      | 58.3 ms: 1.01x faster                                                                  |
| xml_etree_generate       | 83.6 ms                                                                      | 82.6 ms: 1.01x faster                                                                  |
| sympy_integrate          | 23.6 ms                                                                      | 23.3 ms: 1.01x faster                                                                  |
| gc_traversal             | 4.65 ms                                                                      | 4.60 ms: 1.01x faster                                                                  |
| sqlglot_parse            | 1.42 ms                                                                      | 1.41 ms: 1.01x faster                                                                  |
| xml_etree_process        | 58.2 ms                                                                      | 57.6 ms: 1.01x faster                                                                  |
| sqlglot_transpile        | 1.79 ms                                                                      | 1.77 ms: 1.01x faster                                                                  |
| 2to3                     | 291 ms                                                                       | 288 ms: 1.01x faster                                                                   |
| sympy_expand             | 499 ms                                                                       | 495 ms: 1.01x faster                                                                   |
| sqlglot_normalize        | 117 ms                                                                       | 116 ms: 1.01x faster                                                                   |
| regex_compile            | 142 ms                                                                       | 141 ms: 1.01x faster                                                                   |
| html5lib                 | 74.5 ms                                                                      | 73.9 ms: 1.01x faster                                                                  |
| richards                 | 52.1 ms                                                                      | 51.7 ms: 1.01x faster                                                                  |
| json_dumps               | 10.6 ms                                                                      | 10.6 ms: 1.01x faster                                                                  |
| coverage                 | 89.6 ms                                                                      | 89.1 ms: 1.01x faster                                                                  |
| python_startup_no_site   | 11.1 ms                                                                      | 11.0 ms: 1.00x faster                                                                  |
| python_startup           | 12.8 ms                                                                      | 12.8 ms: 1.00x faster                                                                  |
| docutils                 | 2.99 sec                                                                     | 2.98 sec: 1.00x faster                                                                 |
| pylint                   | 319 ms                                                                       | 318 ms: 1.00x faster                                                                   |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x faster                                                                 |
| meteor_contest           | 127 ms                                                                       | 127 ms: 1.00x slower                                                                   |
| regex_effbot             | 3.47 ms                                                                      | 3.48 ms: 1.00x slower                                                                  |
| pickle_list              | 4.26 us                                                                      | 4.29 us: 1.01x slower                                                                  |
| pyflate                  | 502 ms                                                                       | 507 ms: 1.01x slower                                                                   |
| mako                     | 10.2 ms                                                                      | 10.3 ms: 1.01x slower                                                                  |
| pathlib                  | 18.9 ms                                                                      | 19.1 ms: 1.01x slower                                                                  |
| mdp                      | 2.48 sec                                                                     | 2.51 sec: 1.01x slower                                                                 |
| regex_dna                | 237 ms                                                                       | 240 ms: 1.01x slower                                                                   |
| pycparser                | 1.25 sec                                                                     | 1.26 sec: 1.01x slower                                                                 |
| coroutines               | 22.4 ms                                                                      | 22.7 ms: 1.02x slower                                                                  |
| crypto_pyaes             | 71.1 ms                                                                      | 72.4 ms: 1.02x slower                                                                  |
| nqueens                  | 87.8 ms                                                                      | 89.5 ms: 1.02x slower                                                                  |
| unpickle_pure_python     | 216 us                                                                       | 221 us: 1.02x slower                                                                   |
| create_gc_cycles         | 1.87 ms                                                                      | 1.92 ms: 1.02x slower                                                                  |
| raytrace                 | 252 ms                                                                       | 258 ms: 1.03x slower                                                                   |
| xml_etree_parse          | 144 ms                                                                       | 148 ms: 1.03x slower                                                                   |
| chameleon                | 7.26 ms                                                                      | 7.47 ms: 1.03x slower                                                                  |
| async_generators         | 348 ms                                                                       | 359 ms: 1.03x slower                                                                   |
| chaos                    | 58.8 ms                                                                      | 60.7 ms: 1.03x slower                                                                  |
| logging_format           | 6.99 us                                                                      | 7.24 us: 1.04x slower                                                                  |
| logging_simple           | 6.26 us                                                                      | 6.49 us: 1.04x slower                                                                  |
| scimark_sparse_mat_mult  | 4.19 ms                                                                      | 4.35 ms: 1.04x slower                                                                  |
| scimark_lu               | 94.3 ms                                                                      | 98.7 ms: 1.05x slower                                                                  |
| scimark_monte_carlo      | 64.2 ms                                                                      | 68.2 ms: 1.06x slower                                                                  |
| scimark_fft              | 300 ms                                                                       | 320 ms: 1.07x slower                                                                   |
| nbody                    | 84.6 ms                                                                      | 91.4 ms: 1.08x slower                                                                  |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (33): bench_thread_pool, mypy2, async_tree_memoization, tornado_http, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, dask, json, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, aiohttp, gunicorn, sympy_str, deltablue, dulwich_log, genshi_xml, async_tree_none, pidigits, pickle, pickle_dict, json_loads, hexiom, sqlite_synth, genshi_text, go, deepcopy, asyncio_websockets, generators, float, async_tree_io_tg, async_tree_io, bench_mp_pool

# HPT report

- Reliability score: 95.31% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x