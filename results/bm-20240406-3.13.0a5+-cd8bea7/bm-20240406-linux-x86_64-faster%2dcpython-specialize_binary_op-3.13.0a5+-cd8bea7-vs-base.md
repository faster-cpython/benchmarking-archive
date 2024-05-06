# Results vs. base

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: cd8bea7
- commit date: 2024-04-06
- overall geometric mean: 1.00x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 268 ms: 1.01x slower                                                             |
| chameleon      | 6.92 ms                                                                | 6.97 ms: 1.01x slower                                                            |
| docutils       | 2.77 sec                                                               | 2.80 sec: 1.01x slower                                                           |
| html5lib       | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.7 ms                                                                | 77.6 ms: 1.01x faster                                                            |
| pidigits       | 191 ms                                                                 | 194 ms: 1.02x slower                                                             |
| nbody          | 88.5 ms                                                                | 94.4 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| regex_dna      | 224 ms                                                                 | 230 ms: 1.02x slower                                                             |
| regex_effbot   | 3.72 ms                                                                | 3.81 ms: 1.03x slower                                                            |
| regex_v8       | 25.5 ms                                                                | 26.2 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 5.18 us: 1.03x faster                                                            |
| pickle               | 11.9 us                                                                | 11.8 us: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                                 | 219 us: 1.01x slower                                                             |
| pickle_pure_python   | 299 us                                                                 | 302 us: 1.01x slower                                                             |
| tomli_loads          | 2.15 sec                                                               | 2.21 sec: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (8): xml_etree_parse, xml_etree_process, json_loads, unpickle, pickle_dict, unpickle_list, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 8.99 ms: 1.00x faster                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                            |
| mako           | 11.0 ms                                                                | 11.2 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| gc_traversal             | 3.94 ms                                                                | 3.57 ms: 1.10x faster                                                            |
| mdp                      | 2.73 sec                                                               | 2.57 sec: 1.07x faster                                                           |
| typing_runtime_protocols | 115 us                                                                 | 111 us: 1.03x faster                                                             |
| crypto_pyaes             | 73.0 ms                                                                | 70.9 ms: 1.03x faster                                                            |
| pickle_list              | 5.33 us                                                                | 5.18 us: 1.03x faster                                                            |
| spectral_norm            | 110 ms                                                                 | 107 ms: 1.03x faster                                                             |
| pyflate                  | 461 ms                                                                 | 452 ms: 1.02x faster                                                             |
| pathlib                  | 18.8 ms                                                                | 18.5 ms: 1.02x faster                                                            |
| scimark_sparse_mat_mult  | 4.99 ms                                                                | 4.92 ms: 1.01x faster                                                            |
| float                    | 78.7 ms                                                                | 77.6 ms: 1.01x faster                                                            |
| pickle                   | 11.9 us                                                                | 11.8 us: 1.01x faster                                                            |
| json_dumps               | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| genshi_text              | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                            |
| create_gc_cycles         | 1.75 ms                                                                | 1.74 ms: 1.01x faster                                                            |
| logging_simple           | 5.67 us                                                                | 5.64 us: 1.01x faster                                                            |
| deepcopy_reduce          | 3.17 us                                                                | 3.15 us: 1.01x faster                                                            |
| async_generators         | 441 ms                                                                 | 439 ms: 1.00x faster                                                             |
| fannkuch                 | 397 ms                                                                 | 396 ms: 1.00x faster                                                             |
| python_startup_no_site   | 9.00 ms                                                                | 8.99 ms: 1.00x faster                                                            |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| pylint                   | 277 ms                                                                 | 278 ms: 1.00x slower                                                             |
| asyncio_tcp              | 505 ms                                                                 | 506 ms: 1.00x slower                                                             |
| bench_thread_pool        | 826 us                                                                 | 828 us: 1.00x slower                                                             |
| sympy_expand             | 462 ms                                                                 | 464 ms: 1.00x slower                                                             |
| coroutines               | 23.1 ms                                                                | 23.2 ms: 1.01x slower                                                            |
| asyncio_websockets       | 564 ms                                                                 | 567 ms: 1.01x slower                                                             |
| 2to3                     | 267 ms                                                                 | 268 ms: 1.01x slower                                                             |
| gunicorn                 | 1.26 ms                                                                | 1.26 ms: 1.01x slower                                                            |
| telco                    | 8.41 ms                                                                | 8.46 ms: 1.01x slower                                                            |
| unpickle_pure_python     | 218 us                                                                 | 219 us: 1.01x slower                                                             |
| coverage                 | 96.9 ms                                                                | 97.7 ms: 1.01x slower                                                            |
| chameleon                | 6.92 ms                                                                | 6.97 ms: 1.01x slower                                                            |
| pickle_pure_python       | 299 us                                                                 | 302 us: 1.01x slower                                                             |
| sqlglot_optimize         | 54.4 ms                                                                | 54.9 ms: 1.01x slower                                                            |
| sympy_sum                | 153 ms                                                                 | 155 ms: 1.01x slower                                                             |
| sqlglot_transpile        | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                                            |
| hexiom                   | 6.21 ms                                                                | 6.27 ms: 1.01x slower                                                            |
| docutils                 | 2.77 sec                                                               | 2.80 sec: 1.01x slower                                                           |
| regex_compile            | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| pprint_safe_repr         | 734 ms                                                                 | 741 ms: 1.01x slower                                                             |
| logging_silent           | 101 ns                                                                 | 102 ns: 1.01x slower                                                             |
| scimark_monte_carlo      | 67.7 ms                                                                | 68.4 ms: 1.01x slower                                                            |
| sqlite_synth             | 2.92 us                                                                | 2.95 us: 1.01x slower                                                            |
| deepcopy_memo            | 37.8 us                                                                | 38.2 us: 1.01x slower                                                            |
| generators               | 29.3 ms                                                                | 29.7 ms: 1.01x slower                                                            |
| go                       | 141 ms                                                                 | 143 ms: 1.01x slower                                                             |
| pprint_pformat           | 1.50 sec                                                               | 1.52 sec: 1.01x slower                                                           |
| sympy_integrate          | 20.0 ms                                                                | 20.3 ms: 1.01x slower                                                            |
| dulwich_log              | 67.0 ms                                                                | 67.9 ms: 1.01x slower                                                            |
| sqlglot_normalize        | 109 ms                                                                 | 110 ms: 1.02x slower                                                             |
| pidigits                 | 191 ms                                                                 | 194 ms: 1.02x slower                                                             |
| scimark_lu               | 112 ms                                                                 | 114 ms: 1.02x slower                                                             |
| thrift                   | 799 us                                                                 | 814 us: 1.02x slower                                                             |
| html5lib                 | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                            |
| chaos                    | 59.9 ms                                                                | 61.2 ms: 1.02x slower                                                            |
| mako                     | 11.0 ms                                                                | 11.2 ms: 1.02x slower                                                            |
| comprehensions           | 16.3 us                                                                | 16.7 us: 1.02x slower                                                            |
| regex_dna                | 224 ms                                                                 | 230 ms: 1.02x slower                                                             |
| nqueens                  | 80.6 ms                                                                | 82.5 ms: 1.02x slower                                                            |
| tomli_loads              | 2.15 sec                                                               | 2.21 sec: 1.02x slower                                                           |
| regex_effbot             | 3.72 ms                                                                | 3.81 ms: 1.03x slower                                                            |
| sqlglot_parse            | 1.27 ms                                                                | 1.30 ms: 1.03x slower                                                            |
| regex_v8                 | 25.5 ms                                                                | 26.2 ms: 1.03x slower                                                            |
| richards_super           | 51.6 ms                                                                | 53.1 ms: 1.03x slower                                                            |
| deltablue                | 3.14 ms                                                                | 3.25 ms: 1.03x slower                                                            |
| raytrace                 | 258 ms                                                                 | 267 ms: 1.04x slower                                                             |
| richards                 | 45.5 ms                                                                | 47.3 ms: 1.04x slower                                                            |
| scimark_fft              | 359 ms                                                                 | 377 ms: 1.05x slower                                                             |
| nbody                    | 88.5 ms                                                                | 94.4 ms: 1.07x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (30): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, json, xml_etree_parse, deepcopy, genshi_xml, async_tree_io_tg, async_tree_memoization_tg, dask, xml_etree_process, asyncio_tcp_ssl, tornado_http, bench_mp_pool, json_loads, unpickle, pickle_dict, logging_format, unpickle_list, xml_etree_iterparse, xml_etree_generate, meteor_contest, scimark_sor, pycparser, async_tree_none_tg, aiohttp, mypy2, sympy_str, async_tree_none

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x