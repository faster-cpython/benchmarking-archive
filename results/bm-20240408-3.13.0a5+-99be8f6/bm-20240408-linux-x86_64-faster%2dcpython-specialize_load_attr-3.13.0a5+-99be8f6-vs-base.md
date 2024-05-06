# Results vs. base

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 99be8f6
- commit date: 2024-04-08
- overall geometric mean: 1.00x faster
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 271 ms: 1.00x faster                                                             |
| chameleon      | 6.94 ms                                                                | 6.87 ms: 1.01x faster                                                            |
| html5lib       | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_io_tg, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                                | 77.5 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                | 25.0 ms: 1.04x faster                                                            |
| regex_compile  | 136 ms                                                                 | 135 ms: 1.01x faster                                                             |
| regex_dna      | 226 ms                                                                 | 225 ms: 1.01x faster                                                             |
| regex_effbot   | 3.74 ms                                                                | 3.85 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse | 110 ms                                                                 | 107 ms: 1.02x faster                                                             |
| pickle_list         | 5.23 us                                                                | 5.14 us: 1.02x faster                                                            |
| xml_etree_parse     | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| unpickle            | 15.1 us                                                                | 14.9 us: 1.02x faster                                                            |
| pickle_pure_python  | 302 us                                                                 | 300 us: 1.01x faster                                                             |
| xml_etree_generate  | 87.5 ms                                                                | 88.3 ms: 1.01x slower                                                            |
| xml_etree_process   | 60.3 ms                                                                | 60.9 ms: 1.01x slower                                                            |
| json_dumps          | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| pickle_dict         | 34.5 us                                                                | 35.1 us: 1.02x slower                                                            |
| unpickle_list       | 5.09 us                                                                | 5.27 us: 1.03x slower                                                            |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (4): tomli_loads, pickle, unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| python_startup_no_site | 8.96 ms                                                                | 9.00 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.1 ms                                                                | 10.9 ms: 1.02x faster                                                            |
| genshi_text    | 23.8 ms                                                                | 24.2 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pycparser                | 1.21 sec                                                               | 1.15 sec: 1.06x faster                                                           |
| regex_v8                 | 26.1 ms                                                                | 25.0 ms: 1.04x faster                                                            |
| deepcopy_memo            | 38.2 us                                                                | 36.9 us: 1.03x faster                                                            |
| logging_silent           | 103 ns                                                                 | 101 ns: 1.03x faster                                                             |
| xml_etree_iterparse      | 110 ms                                                                 | 107 ms: 1.02x faster                                                             |
| async_tree_none_tg       | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| mako                     | 11.1 ms                                                                | 10.9 ms: 1.02x faster                                                            |
| float                    | 78.9 ms                                                                | 77.5 ms: 1.02x faster                                                            |
| richards_super           | 53.9 ms                                                                | 53.0 ms: 1.02x faster                                                            |
| logging_format           | 6.39 us                                                                | 6.29 us: 1.02x faster                                                            |
| telco                    | 8.75 ms                                                                | 8.61 ms: 1.02x faster                                                            |
| pickle_list              | 5.23 us                                                                | 5.14 us: 1.02x faster                                                            |
| xml_etree_parse          | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| unpickle                 | 15.1 us                                                                | 14.9 us: 1.02x faster                                                            |
| richards                 | 47.7 ms                                                                | 47.0 ms: 1.01x faster                                                            |
| async_generators         | 449 ms                                                                 | 443 ms: 1.01x faster                                                             |
| logging_simple           | 5.80 us                                                                | 5.73 us: 1.01x faster                                                            |
| regex_compile            | 136 ms                                                                 | 135 ms: 1.01x faster                                                             |
| fannkuch                 | 397 ms                                                                 | 394 ms: 1.01x faster                                                             |
| chameleon                | 6.94 ms                                                                | 6.87 ms: 1.01x faster                                                            |
| pprint_pformat           | 1.55 sec                                                               | 1.54 sec: 1.01x faster                                                           |
| sympy_expand             | 474 ms                                                                 | 471 ms: 1.01x faster                                                             |
| chaos                    | 60.6 ms                                                                | 60.1 ms: 1.01x faster                                                            |
| sqlglot_optimize         | 55.7 ms                                                                | 55.3 ms: 1.01x faster                                                            |
| pickle_pure_python       | 302 us                                                                 | 300 us: 1.01x faster                                                             |
| regex_dna                | 226 ms                                                                 | 225 ms: 1.01x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.01x faster                                                           |
| sympy_integrate          | 20.4 ms                                                                | 20.3 ms: 1.01x faster                                                            |
| sqlite_synth             | 2.94 us                                                                | 2.93 us: 1.01x faster                                                            |
| sqlglot_normalize        | 112 ms                                                                 | 111 ms: 1.01x faster                                                             |
| sqlglot_transpile        | 1.59 ms                                                                | 1.59 ms: 1.01x faster                                                            |
| pylint                   | 280 ms                                                                 | 279 ms: 1.00x faster                                                             |
| sympy_sum                | 157 ms                                                                 | 156 ms: 1.00x faster                                                             |
| pidigits                 | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| spectral_norm            | 116 ms                                                                 | 115 ms: 1.00x faster                                                             |
| create_gc_cycles         | 1.74 ms                                                                | 1.74 ms: 1.00x faster                                                            |
| 2to3                     | 272 ms                                                                 | 271 ms: 1.00x faster                                                             |
| crypto_pyaes             | 74.6 ms                                                                | 74.9 ms: 1.00x slower                                                            |
| python_startup           | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| python_startup_no_site   | 8.96 ms                                                                | 9.00 ms: 1.00x slower                                                            |
| raytrace                 | 262 ms                                                                 | 263 ms: 1.01x slower                                                             |
| pyflate                  | 477 ms                                                                 | 480 ms: 1.01x slower                                                             |
| asyncio_tcp              | 499 ms                                                                 | 503 ms: 1.01x slower                                                             |
| scimark_monte_carlo      | 68.0 ms                                                                | 68.5 ms: 1.01x slower                                                            |
| dulwich_log              | 67.2 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| xml_etree_generate       | 87.5 ms                                                                | 88.3 ms: 1.01x slower                                                            |
| xml_etree_process        | 60.3 ms                                                                | 60.9 ms: 1.01x slower                                                            |
| html5lib                 | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| meteor_contest           | 111 ms                                                                 | 113 ms: 1.01x slower                                                             |
| scimark_lu               | 114 ms                                                                 | 116 ms: 1.02x slower                                                             |
| pickle_dict              | 34.5 us                                                                | 35.1 us: 1.02x slower                                                            |
| go                       | 144 ms                                                                 | 146 ms: 1.02x slower                                                             |
| genshi_text              | 23.8 ms                                                                | 24.2 ms: 1.02x slower                                                            |
| scimark_sparse_mat_mult  | 5.25 ms                                                                | 5.36 ms: 1.02x slower                                                            |
| coverage                 | 96.9 ms                                                                | 99.5 ms: 1.03x slower                                                            |
| regex_effbot             | 3.74 ms                                                                | 3.85 ms: 1.03x slower                                                            |
| gc_traversal             | 3.88 ms                                                                | 4.00 ms: 1.03x slower                                                            |
| typing_runtime_protocols | 113 us                                                                 | 117 us: 1.03x slower                                                             |
| unpickle_list            | 5.09 us                                                                | 5.27 us: 1.03x slower                                                            |
| mdp                      | 2.62 sec                                                               | 2.73 sec: 1.05x slower                                                           |
| coroutines               | 22.3 ms                                                                | 24.1 ms: 1.08x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (37): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_io_tg, async_tree_memoization_tg, mypy2, dask, sympy_str, gunicorn, pathlib, tomli_loads, sqlglot_parse, asyncio_websockets, pickle, deltablue, async_tree_io, bench_mp_pool, deepcopy_reduce, tornado_http, bench_thread_pool, deepcopy, unpickle_pure_python, generators, comprehensions, hexiom, nbody, nqueens, json, scimark_fft, scimark_sor, docutils, genshi_xml, pprint_safe_repr, json_loads, aiohttp, thrift

# HPT report

- Reliability score: 99.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x