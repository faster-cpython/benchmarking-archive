# Results vs. base

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: dd7732d
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 267 ms                                                                 | 268 ms: 1.00x slower                                                          |
| chameleon      | 6.92 ms                                                                | 6.98 ms: 1.01x slower                                                         |
| docutils       | 2.77 sec                                                               | 2.80 sec: 1.01x slower                                                        |
| html5lib       | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                         |
| tornado_http   | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 78.7 ms                                                                | 81.3 ms: 1.03x slower                                                         |
| pidigits       | 191 ms                                                                 | 198 ms: 1.04x slower                                                          |
| nbody          | 88.5 ms                                                                | 127 ms: 1.43x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 25.5 ms                                                                | 24.4 ms: 1.04x faster                                                         |
| regex_dna      | 224 ms                                                                 | 221 ms: 1.02x faster                                                          |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 4.93 us: 1.08x faster                                                         |
| pickle_dict          | 35.4 us                                                                | 34.2 us: 1.04x faster                                                         |
| pickle               | 11.9 us                                                                | 11.7 us: 1.02x faster                                                         |
| unpickle_pure_python | 218 us                                                                 | 219 us: 1.00x slower                                                          |
| json_dumps           | 10.7 ms                                                                | 10.7 ms: 1.01x slower                                                         |
| xml_etree_process    | 60.0 ms                                                                | 60.9 ms: 1.01x slower                                                         |
| xml_etree_generate   | 86.4 ms                                                                | 88.8 ms: 1.03x slower                                                         |
| tomli_loads          | 2.15 sec                                                               | 2.26 sec: 1.05x slower                                                        |
| unpickle_list        | 4.97 us                                                                | 5.22 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (5): xml_etree_parse, unpickle, pickle_pure_python, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 8.97 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 51.8 ms                                                                | 51.0 ms: 1.02x faster                                                         |
| genshi_text    | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                         |
| mako           | 11.0 ms                                                                | 11.2 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal             | 3.94 ms                                                                | 3.59 ms: 1.10x faster                                                         |
| pickle_list              | 5.33 us                                                                | 4.93 us: 1.08x faster                                                         |
| regex_v8                 | 25.5 ms                                                                | 24.4 ms: 1.04x faster                                                         |
| pycparser                | 1.19 sec                                                               | 1.15 sec: 1.04x faster                                                        |
| pickle_dict              | 35.4 us                                                                | 34.2 us: 1.04x faster                                                         |
| pickle                   | 11.9 us                                                                | 11.7 us: 1.02x faster                                                         |
| genshi_xml               | 51.8 ms                                                                | 51.0 ms: 1.02x faster                                                         |
| regex_dna                | 224 ms                                                                 | 221 ms: 1.02x faster                                                          |
| genshi_text              | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                         |
| typing_runtime_protocols | 115 us                                                                 | 114 us: 1.01x faster                                                          |
| logging_silent           | 101 ns                                                                 | 100 ns: 1.01x faster                                                          |
| deepcopy_memo            | 37.8 us                                                                | 37.6 us: 1.00x faster                                                         |
| deepcopy                 | 353 us                                                                 | 352 us: 1.00x faster                                                          |
| python_startup_no_site   | 9.00 ms                                                                | 8.97 ms: 1.00x faster                                                         |
| 2to3                     | 267 ms                                                                 | 268 ms: 1.00x slower                                                          |
| pylint                   | 277 ms                                                                 | 278 ms: 1.00x slower                                                          |
| unpickle_pure_python     | 218 us                                                                 | 219 us: 1.00x slower                                                          |
| json_dumps               | 10.7 ms                                                                | 10.7 ms: 1.01x slower                                                         |
| gunicorn                 | 1.26 ms                                                                | 1.27 ms: 1.01x slower                                                         |
| tornado_http             | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| dulwich_log              | 67.0 ms                                                                | 67.5 ms: 1.01x slower                                                         |
| deepcopy_reduce          | 3.17 us                                                                | 3.20 us: 1.01x slower                                                         |
| bench_thread_pool        | 826 us                                                                 | 833 us: 1.01x slower                                                          |
| sqlglot_transpile        | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                                         |
| generators               | 29.3 ms                                                                | 29.6 ms: 1.01x slower                                                         |
| chameleon                | 6.92 ms                                                                | 6.98 ms: 1.01x slower                                                         |
| deltablue                | 3.14 ms                                                                | 3.17 ms: 1.01x slower                                                         |
| regex_compile            | 134 ms                                                                 | 135 ms: 1.01x slower                                                          |
| comprehensions           | 16.3 us                                                                | 16.5 us: 1.01x slower                                                         |
| docutils                 | 2.77 sec                                                               | 2.80 sec: 1.01x slower                                                        |
| sympy_sum                | 153 ms                                                                 | 155 ms: 1.01x slower                                                          |
| thrift                   | 799 us                                                                 | 809 us: 1.01x slower                                                          |
| pprint_safe_repr         | 734 ms                                                                 | 742 ms: 1.01x slower                                                          |
| coverage                 | 96.9 ms                                                                | 98.1 ms: 1.01x slower                                                         |
| sqlglot_optimize         | 54.4 ms                                                                | 55.1 ms: 1.01x slower                                                         |
| sympy_integrate          | 20.0 ms                                                                | 20.3 ms: 1.01x slower                                                         |
| xml_etree_process        | 60.0 ms                                                                | 60.9 ms: 1.01x slower                                                         |
| sqlite_synth             | 2.92 us                                                                | 2.96 us: 1.02x slower                                                         |
| mdp                      | 2.73 sec                                                               | 2.78 sec: 1.02x slower                                                        |
| pprint_pformat           | 1.50 sec                                                               | 1.52 sec: 1.02x slower                                                        |
| crypto_pyaes             | 73.0 ms                                                                | 74.3 ms: 1.02x slower                                                         |
| richards_super           | 51.6 ms                                                                | 52.5 ms: 1.02x slower                                                         |
| sympy_expand             | 462 ms                                                                 | 470 ms: 1.02x slower                                                          |
| sqlglot_parse            | 1.27 ms                                                                | 1.29 ms: 1.02x slower                                                         |
| sympy_str                | 275 ms                                                                 | 281 ms: 1.02x slower                                                          |
| html5lib                 | 66.8 ms                                                                | 68.2 ms: 1.02x slower                                                         |
| sqlglot_normalize        | 109 ms                                                                 | 111 ms: 1.02x slower                                                          |
| mako                     | 11.0 ms                                                                | 11.2 ms: 1.02x slower                                                         |
| pathlib                  | 18.8 ms                                                                | 19.3 ms: 1.03x slower                                                         |
| xml_etree_generate       | 86.4 ms                                                                | 88.8 ms: 1.03x slower                                                         |
| go                       | 141 ms                                                                 | 145 ms: 1.03x slower                                                          |
| coroutines               | 23.1 ms                                                                | 23.7 ms: 1.03x slower                                                         |
| richards                 | 45.5 ms                                                                | 46.8 ms: 1.03x slower                                                         |
| logging_simple           | 5.67 us                                                                | 5.85 us: 1.03x slower                                                         |
| telco                    | 8.41 ms                                                                | 8.68 ms: 1.03x slower                                                         |
| float                    | 78.7 ms                                                                | 81.3 ms: 1.03x slower                                                         |
| nqueens                  | 80.6 ms                                                                | 83.3 ms: 1.03x slower                                                         |
| pidigits                 | 191 ms                                                                 | 198 ms: 1.04x slower                                                          |
| tomli_loads              | 2.15 sec                                                               | 2.26 sec: 1.05x slower                                                        |
| unpickle_list            | 4.97 us                                                                | 5.22 us: 1.05x slower                                                         |
| logging_format           | 6.26 us                                                                | 6.59 us: 1.05x slower                                                         |
| fannkuch                 | 397 ms                                                                 | 419 ms: 1.06x slower                                                          |
| scimark_sor              | 129 ms                                                                 | 136 ms: 1.06x slower                                                          |
| pyflate                  | 461 ms                                                                 | 490 ms: 1.06x slower                                                          |
| raytrace                 | 258 ms                                                                 | 280 ms: 1.09x slower                                                          |
| scimark_lu               | 112 ms                                                                 | 122 ms: 1.09x slower                                                          |
| scimark_monte_carlo      | 67.7 ms                                                                | 73.6 ms: 1.09x slower                                                         |
| chaos                    | 59.9 ms                                                                | 68.9 ms: 1.15x slower                                                         |
| scimark_sparse_mat_mult  | 4.99 ms                                                                | 5.81 ms: 1.16x slower                                                         |
| scimark_fft              | 359 ms                                                                 | 429 ms: 1.19x slower                                                          |
| spectral_norm            | 110 ms                                                                 | 142 ms: 1.29x slower                                                          |
| nbody                    | 88.5 ms                                                                | 127 ms: 1.43x slower                                                          |
| Geometric mean           | (ref)                                                                  | 1.02x slower                                                                  |

Benchmark hidden because not significant (27): xml_etree_parse, async_tree_io, json, unpickle, async_tree_memoization, async_tree_cpu_io_mixed, create_gc_cycles, async_tree_cpu_io_mixed_tg, asyncio_tcp_ssl, asyncio_tcp, bench_mp_pool, async_generators, python_startup, asyncio_websockets, async_tree_memoization_tg, pickle_pure_python, async_tree_none_tg, xml_etree_iterparse, dask, hexiom, aiohttp, async_tree_none, mypy2, json_loads, meteor_contest, regex_effbot, async_tree_io_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x