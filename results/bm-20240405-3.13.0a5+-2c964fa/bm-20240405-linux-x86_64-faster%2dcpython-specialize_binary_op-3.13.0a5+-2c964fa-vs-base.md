# Results vs. base

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.00x slower
- HPT reliability: 99.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| docutils       | 2.77 sec                                                               | 2.79 sec: 1.01x slower                                                           |
| tornado_http   | 93.9 ms                                                                | 94.3 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (3): 2to3, chameleon, html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.7 ms                                                                | 78.2 ms: 1.01x faster                                                            |
| nbody          | 88.5 ms                                                                | 95.9 ms: 1.08x slower                                                            |
| pidigits       | 191 ms                                                                 | 216 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.5 ms                                                                | 24.4 ms: 1.05x faster                                                            |
| regex_dna      | 224 ms                                                                 | 218 ms: 1.03x faster                                                             |
| regex_effbot   | 3.72 ms                                                                | 3.69 ms: 1.01x faster                                                            |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 4.93 us: 1.08x faster                                                            |
| unpickle             | 15.4 us                                                                | 15.0 us: 1.03x faster                                                            |
| pickle               | 11.9 us                                                                | 11.7 us: 1.02x faster                                                            |
| json_dumps           | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                            |
| pickle_dict          | 35.4 us                                                                | 35.3 us: 1.00x faster                                                            |
| json_loads           | 28.6 us                                                                | 28.5 us: 1.00x faster                                                            |
| xml_etree_generate   | 86.4 ms                                                                | 86.7 ms: 1.00x slower                                                            |
| unpickle_pure_python | 218 us                                                                 | 221 us: 1.01x slower                                                             |
| tomli_loads          | 2.15 sec                                                               | 2.19 sec: 1.02x slower                                                           |
| pickle_pure_python   | 299 us                                                                 | 305 us: 1.02x slower                                                             |
| unpickle_list        | 4.97 us                                                                | 5.11 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.00 ms                                                                | 8.97 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                                | 10.7 ms: 1.03x faster                                                            |
| genshi_xml     | 51.8 ms                                                                | 52.4 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20240403-linux-x86_64-python-85843348c5f0b8c2f973-3.13.0a5+-8584334 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list             | 5.33 us                                                                | 4.93 us: 1.08x faster                                                            |
| spectral_norm           | 110 ms                                                                 | 103 ms: 1.07x faster                                                             |
| mdp                     | 2.73 sec                                                               | 2.58 sec: 1.06x faster                                                           |
| scimark_sor             | 129 ms                                                                 | 122 ms: 1.06x faster                                                             |
| regex_v8                | 25.5 ms                                                                | 24.4 ms: 1.05x faster                                                            |
| pycparser               | 1.19 sec                                                               | 1.14 sec: 1.05x faster                                                           |
| crypto_pyaes            | 73.0 ms                                                                | 69.9 ms: 1.04x faster                                                            |
| regex_dna               | 224 ms                                                                 | 218 ms: 1.03x faster                                                             |
| mako                    | 11.0 ms                                                                | 10.7 ms: 1.03x faster                                                            |
| unpickle                | 15.4 us                                                                | 15.0 us: 1.03x faster                                                            |
| scimark_sparse_mat_mult | 4.99 ms                                                                | 4.87 ms: 1.02x faster                                                            |
| pickle                  | 11.9 us                                                                | 11.7 us: 1.02x faster                                                            |
| json_dumps              | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                            |
| deepcopy_reduce         | 3.17 us                                                                | 3.14 us: 1.01x faster                                                            |
| regex_effbot            | 3.72 ms                                                                | 3.69 ms: 1.01x faster                                                            |
| coroutines              | 23.1 ms                                                                | 22.9 ms: 1.01x faster                                                            |
| float                   | 78.7 ms                                                                | 78.2 ms: 1.01x faster                                                            |
| pickle_dict             | 35.4 us                                                                | 35.3 us: 1.00x faster                                                            |
| json_loads              | 28.6 us                                                                | 28.5 us: 1.00x faster                                                            |
| python_startup_no_site  | 9.00 ms                                                                | 8.97 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl         | 1.84 sec                                                               | 1.84 sec: 1.00x slower                                                           |
| asyncio_tcp             | 505 ms                                                                 | 506 ms: 1.00x slower                                                             |
| xml_etree_generate      | 86.4 ms                                                                | 86.7 ms: 1.00x slower                                                            |
| dulwich_log             | 67.0 ms                                                                | 67.3 ms: 1.00x slower                                                            |
| tornado_http            | 93.9 ms                                                                | 94.3 ms: 1.00x slower                                                            |
| nqueens                 | 80.6 ms                                                                | 81.0 ms: 1.01x slower                                                            |
| gc_traversal            | 3.94 ms                                                                | 3.97 ms: 1.01x slower                                                            |
| create_gc_cycles        | 1.75 ms                                                                | 1.76 ms: 1.01x slower                                                            |
| sympy_sum               | 153 ms                                                                 | 154 ms: 1.01x slower                                                             |
| sqlglot_transpile       | 1.58 ms                                                                | 1.59 ms: 1.01x slower                                                            |
| docutils                | 2.77 sec                                                               | 2.79 sec: 1.01x slower                                                           |
| pprint_pformat          | 1.50 sec                                                               | 1.51 sec: 1.01x slower                                                           |
| sympy_expand            | 462 ms                                                                 | 465 ms: 1.01x slower                                                             |
| pprint_safe_repr        | 734 ms                                                                 | 739 ms: 1.01x slower                                                             |
| scimark_lu              | 112 ms                                                                 | 113 ms: 1.01x slower                                                             |
| aiohttp                 | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                            |
| regex_compile           | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| thrift                  | 799 us                                                                 | 806 us: 1.01x slower                                                             |
| unpickle_pure_python    | 218 us                                                                 | 221 us: 1.01x slower                                                             |
| genshi_xml              | 51.8 ms                                                                | 52.4 ms: 1.01x slower                                                            |
| sympy_integrate         | 20.0 ms                                                                | 20.3 ms: 1.01x slower                                                            |
| sympy_str               | 275 ms                                                                 | 279 ms: 1.01x slower                                                             |
| coverage                | 96.9 ms                                                                | 98.2 ms: 1.01x slower                                                            |
| sqlglot_optimize        | 54.4 ms                                                                | 55.1 ms: 1.01x slower                                                            |
| hexiom                  | 6.21 ms                                                                | 6.30 ms: 1.01x slower                                                            |
| tomli_loads             | 2.15 sec                                                               | 2.19 sec: 1.02x slower                                                           |
| deepcopy_memo           | 37.8 us                                                                | 38.4 us: 1.02x slower                                                            |
| pyflate                 | 461 ms                                                                 | 469 ms: 1.02x slower                                                             |
| sqlglot_parse           | 1.27 ms                                                                | 1.29 ms: 1.02x slower                                                            |
| pickle_pure_python      | 299 us                                                                 | 305 us: 1.02x slower                                                             |
| go                      | 141 ms                                                                 | 144 ms: 1.02x slower                                                             |
| richards_super          | 51.6 ms                                                                | 52.7 ms: 1.02x slower                                                            |
| logging_simple          | 5.67 us                                                                | 5.81 us: 1.02x slower                                                            |
| deltablue               | 3.14 ms                                                                | 3.22 ms: 1.02x slower                                                            |
| raytrace                | 258 ms                                                                 | 265 ms: 1.03x slower                                                             |
| unpickle_list           | 4.97 us                                                                | 5.11 us: 1.03x slower                                                            |
| comprehensions          | 16.3 us                                                                | 16.8 us: 1.03x slower                                                            |
| sqlglot_normalize       | 109 ms                                                                 | 112 ms: 1.03x slower                                                             |
| logging_format          | 6.26 us                                                                | 6.47 us: 1.03x slower                                                            |
| richards                | 45.5 ms                                                                | 47.0 ms: 1.03x slower                                                            |
| scimark_monte_carlo     | 67.7 ms                                                                | 70.3 ms: 1.04x slower                                                            |
| logging_silent          | 101 ns                                                                 | 105 ns: 1.04x slower                                                             |
| scimark_fft             | 359 ms                                                                 | 375 ms: 1.05x slower                                                             |
| chaos                   | 59.9 ms                                                                | 62.8 ms: 1.05x slower                                                            |
| nbody                   | 88.5 ms                                                                | 95.9 ms: 1.08x slower                                                            |
| pidigits                | 191 ms                                                                 | 216 ms: 1.13x slower                                                             |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (33): async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, dask, xml_etree_process, xml_etree_parse, typing_runtime_protocols, async_tree_memoization, json, generators, deepcopy, async_generators, pathlib, asyncio_websockets, sqlite_synth, pylint, python_startup, mypy2, gunicorn, genshi_text, 2to3, fannkuch, bench_thread_pool, bench_mp_pool, chameleon, meteor_contest, async_tree_none, telco, async_tree_memoization_tg, html5lib, xml_etree_iterparse, async_tree_io_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x