# Results vs. base

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: accc60a
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 268 ms: 1.00x slower                                                             |
| chameleon      | 6.92 ms                                                                | 6.96 ms: 1.01x slower                                                            |
| docutils       | 2.77 sec                                                               | 2.78 sec: 1.00x slower                                                           |
| html5lib       | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                            |
| tornado_http   | 93.9 ms                                                                | 94.3 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 195 ms: 1.02x slower                                                             |
| float          | 78.7 ms                                                                | 81.7 ms: 1.04x slower                                                            |
| nbody          | 88.5 ms                                                                | 127 ms: 1.43x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.72 ms                                                                | 3.66 ms: 1.02x faster                                                            |
| regex_v8       | 25.5 ms                                                                | 25.4 ms: 1.01x faster                                                            |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| regex_dna      | 224 ms                                                                 | 227 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 5.26 us: 1.01x faster                                                            |
| pickle_dict          | 35.4 us                                                                | 35.2 us: 1.01x faster                                                            |
| pickle_pure_python   | 299 us                                                                 | 297 us: 1.01x faster                                                             |
| json_loads           | 28.6 us                                                                | 28.5 us: 1.00x faster                                                            |
| unpickle_pure_python | 218 us                                                                 | 219 us: 1.00x slower                                                             |
| pickle               | 11.9 us                                                                | 12.0 us: 1.01x slower                                                            |
| xml_etree_process    | 60.0 ms                                                                | 61.1 ms: 1.02x slower                                                            |
| unpickle_list        | 4.97 us                                                                | 5.09 us: 1.02x slower                                                            |
| xml_etree_generate   | 86.4 ms                                                                | 88.6 ms: 1.03x slower                                                            |
| tomli_loads          | 2.15 sec                                                               | 2.26 sec: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (4): json_dumps, xml_etree_parse, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 9.01 ms: 1.00x slower                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                            |
| genshi_xml     | 51.8 ms                                                                | 51.2 ms: 1.01x faster                                                            |
| mako           | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| deepcopy_memo            | 37.8 us                                                                | 36.5 us: 1.03x faster                                                            |
| mdp                      | 2.73 sec                                                               | 2.65 sec: 1.03x faster                                                           |
| logging_silent           | 101 ns                                                                 | 99.2 ns: 1.02x faster                                                            |
| deepcopy_reduce          | 3.17 us                                                                | 3.12 us: 1.02x faster                                                            |
| deepcopy                 | 353 us                                                                 | 347 us: 1.02x faster                                                             |
| regex_effbot             | 3.72 ms                                                                | 3.66 ms: 1.02x faster                                                            |
| pickle_list              | 5.33 us                                                                | 5.26 us: 1.01x faster                                                            |
| typing_runtime_protocols | 115 us                                                                 | 113 us: 1.01x faster                                                             |
| genshi_text              | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                            |
| genshi_xml               | 51.8 ms                                                                | 51.2 ms: 1.01x faster                                                            |
| pickle_dict              | 35.4 us                                                                | 35.2 us: 1.01x faster                                                            |
| regex_v8                 | 25.5 ms                                                                | 25.4 ms: 1.01x faster                                                            |
| pickle_pure_python       | 299 us                                                                 | 297 us: 1.01x faster                                                             |
| json_loads               | 28.6 us                                                                | 28.5 us: 1.00x faster                                                            |
| create_gc_cycles         | 1.75 ms                                                                | 1.75 ms: 1.00x faster                                                            |
| python_startup_no_site   | 9.00 ms                                                                | 9.01 ms: 1.00x slower                                                            |
| pylint                   | 277 ms                                                                 | 278 ms: 1.00x slower                                                             |
| bench_thread_pool        | 826 us                                                                 | 828 us: 1.00x slower                                                             |
| unpickle_pure_python     | 218 us                                                                 | 219 us: 1.00x slower                                                             |
| docutils                 | 2.77 sec                                                               | 2.78 sec: 1.00x slower                                                           |
| pprint_pformat           | 1.50 sec                                                               | 1.50 sec: 1.00x slower                                                           |
| sqlglot_optimize         | 54.4 ms                                                                | 54.7 ms: 1.00x slower                                                            |
| 2to3                     | 267 ms                                                                 | 268 ms: 1.00x slower                                                             |
| tornado_http             | 93.9 ms                                                                | 94.3 ms: 1.00x slower                                                            |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| chameleon                | 6.92 ms                                                                | 6.96 ms: 1.01x slower                                                            |
| async_generators         | 441 ms                                                                 | 444 ms: 1.01x slower                                                             |
| deltablue                | 3.14 ms                                                                | 3.17 ms: 1.01x slower                                                            |
| richards_super           | 51.6 ms                                                                | 52.0 ms: 1.01x slower                                                            |
| aiohttp                  | 1.16 ms                                                                | 1.16 ms: 1.01x slower                                                            |
| generators               | 29.3 ms                                                                | 29.6 ms: 1.01x slower                                                            |
| pickle                   | 11.9 us                                                                | 12.0 us: 1.01x slower                                                            |
| sqlglot_normalize        | 109 ms                                                                 | 109 ms: 1.01x slower                                                             |
| mako                     | 11.0 ms                                                                | 11.0 ms: 1.01x slower                                                            |
| sympy_expand             | 462 ms                                                                 | 466 ms: 1.01x slower                                                             |
| sqlglot_transpile        | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                                            |
| dulwich_log              | 67.0 ms                                                                | 67.6 ms: 1.01x slower                                                            |
| asyncio_tcp              | 505 ms                                                                 | 510 ms: 1.01x slower                                                             |
| regex_compile            | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| regex_dna                | 224 ms                                                                 | 227 ms: 1.01x slower                                                             |
| sympy_str                | 275 ms                                                                 | 278 ms: 1.01x slower                                                             |
| sympy_integrate          | 20.0 ms                                                                | 20.3 ms: 1.01x slower                                                            |
| logging_simple           | 5.67 us                                                                | 5.75 us: 1.01x slower                                                            |
| sqlite_synth             | 2.92 us                                                                | 2.96 us: 1.01x slower                                                            |
| hexiom                   | 6.21 ms                                                                | 6.30 ms: 1.01x slower                                                            |
| thrift                   | 799 us                                                                 | 811 us: 1.02x slower                                                             |
| sympy_sum                | 153 ms                                                                 | 156 ms: 1.02x slower                                                             |
| richards                 | 45.5 ms                                                                | 46.2 ms: 1.02x slower                                                            |
| xml_etree_process        | 60.0 ms                                                                | 61.1 ms: 1.02x slower                                                            |
| gc_traversal             | 3.94 ms                                                                | 4.02 ms: 1.02x slower                                                            |
| sqlglot_parse            | 1.27 ms                                                                | 1.29 ms: 1.02x slower                                                            |
| html5lib                 | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                            |
| pidigits                 | 191 ms                                                                 | 195 ms: 1.02x slower                                                             |
| telco                    | 8.41 ms                                                                | 8.60 ms: 1.02x slower                                                            |
| unpickle_list            | 4.97 us                                                                | 5.09 us: 1.02x slower                                                            |
| xml_etree_generate       | 86.4 ms                                                                | 88.6 ms: 1.03x slower                                                            |
| logging_format           | 6.26 us                                                                | 6.43 us: 1.03x slower                                                            |
| crypto_pyaes             | 73.0 ms                                                                | 75.0 ms: 1.03x slower                                                            |
| go                       | 141 ms                                                                 | 146 ms: 1.03x slower                                                             |
| coverage                 | 96.9 ms                                                                | 101 ms: 1.04x slower                                                             |
| float                    | 78.7 ms                                                                | 81.7 ms: 1.04x slower                                                            |
| nqueens                  | 80.6 ms                                                                | 83.8 ms: 1.04x slower                                                            |
| fannkuch                 | 397 ms                                                                 | 414 ms: 1.04x slower                                                             |
| scimark_sor              | 129 ms                                                                 | 135 ms: 1.04x slower                                                             |
| coroutines               | 23.1 ms                                                                | 24.1 ms: 1.05x slower                                                            |
| tomli_loads              | 2.15 sec                                                               | 2.26 sec: 1.05x slower                                                           |
| pyflate                  | 461 ms                                                                 | 486 ms: 1.05x slower                                                             |
| scimark_monte_carlo      | 67.7 ms                                                                | 73.0 ms: 1.08x slower                                                            |
| scimark_lu               | 112 ms                                                                 | 121 ms: 1.08x slower                                                             |
| raytrace                 | 258 ms                                                                 | 280 ms: 1.09x slower                                                             |
| chaos                    | 59.9 ms                                                                | 69.9 ms: 1.17x slower                                                            |
| scimark_fft              | 359 ms                                                                 | 427 ms: 1.19x slower                                                             |
| scimark_sparse_mat_mult  | 4.99 ms                                                                | 6.13 ms: 1.23x slower                                                            |
| spectral_norm            | 110 ms                                                                 | 141 ms: 1.28x slower                                                             |
| nbody                    | 88.5 ms                                                                | 127 ms: 1.43x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (24): async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, json, async_tree_memoization, json_dumps, meteor_contest, pycparser, xml_etree_parse, pathlib, comprehensions, pprint_safe_repr, asyncio_websockets, async_tree_memoization_tg, asyncio_tcp_ssl, dask, async_tree_io_tg, async_tree_none, xml_etree_iterparse, async_tree_none_tg, bench_mp_pool, mypy2, gunicorn, unpickle

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x