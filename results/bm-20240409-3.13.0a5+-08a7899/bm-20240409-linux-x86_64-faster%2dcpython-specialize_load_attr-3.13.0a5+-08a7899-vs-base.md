# Results vs. base

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 08a7899
- commit date: 2024-04-09
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 270 ms: 1.01x faster                                                             |
| chameleon      | 6.94 ms                                                                | 6.81 ms: 1.02x faster                                                            |
| docutils       | 2.83 sec                                                               | 2.81 sec: 1.00x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                                | 88.8 ms: 1.01x faster                                                            |
| float          | 78.9 ms                                                                | 78.5 ms: 1.01x faster                                                            |
| pidigits       | 191 ms                                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 136 ms                                                                 | 134 ms: 1.02x faster                                                             |
| regex_effbot   | 3.74 ms                                                                | 3.69 ms: 1.01x faster                                                            |
| regex_v8       | 26.1 ms                                                                | 25.9 ms: 1.00x faster                                                            |
| regex_dna      | 226 ms                                                                 | 225 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.23 us                                                                | 5.00 us: 1.05x faster                                                            |
| tomli_loads          | 2.18 sec                                                               | 2.11 sec: 1.03x faster                                                           |
| unpickle_pure_python | 225 us                                                                 | 220 us: 1.02x faster                                                             |
| xml_etree_parse      | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| xml_etree_iterparse  | 110 ms                                                                 | 108 ms: 1.02x faster                                                             |
| pickle_pure_python   | 302 us                                                                 | 299 us: 1.01x faster                                                             |
| xml_etree_generate   | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| json_loads           | 28.5 us                                                                | 28.7 us: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| xml_etree_process    | 60.3 ms                                                                | 60.8 ms: 1.01x slower                                                            |
| pickle               | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| pickle_dict          | 34.5 us                                                                | 35.0 us: 1.01x slower                                                            |
| unpickle_list        | 5.09 us                                                                | 5.35 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| python_startup_no_site | 8.96 ms                                                                | 9.00 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.1 ms                                                                | 10.8 ms: 1.03x faster                                                            |
| genshi_text    | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                                            |
| genshi_xml     | 52.3 ms                                                                | 51.7 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| spectral_norm            | 116 ms                                                                 | 110 ms: 1.06x faster                                                             |
| pickle_list              | 5.23 us                                                                | 5.00 us: 1.05x faster                                                            |
| gc_traversal             | 3.88 ms                                                                | 3.74 ms: 1.04x faster                                                            |
| logging_silent           | 103 ns                                                                 | 99.8 ns: 1.04x faster                                                            |
| mako                     | 11.1 ms                                                                | 10.8 ms: 1.03x faster                                                            |
| tomli_loads              | 2.18 sec                                                               | 2.11 sec: 1.03x faster                                                           |
| logging_simple           | 5.80 us                                                                | 5.64 us: 1.03x faster                                                            |
| telco                    | 8.75 ms                                                                | 8.52 ms: 1.03x faster                                                            |
| deepcopy_memo            | 38.2 us                                                                | 37.2 us: 1.03x faster                                                            |
| scimark_fft              | 374 ms                                                                 | 365 ms: 1.03x faster                                                             |
| genshi_text              | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                                            |
| unpickle_pure_python     | 225 us                                                                 | 220 us: 1.02x faster                                                             |
| richards_super           | 53.9 ms                                                                | 52.9 ms: 1.02x faster                                                            |
| richards                 | 47.7 ms                                                                | 46.7 ms: 1.02x faster                                                            |
| chameleon                | 6.94 ms                                                                | 6.81 ms: 1.02x faster                                                            |
| logging_format           | 6.39 us                                                                | 6.28 us: 1.02x faster                                                            |
| scimark_monte_carlo      | 68.0 ms                                                                | 66.9 ms: 1.02x faster                                                            |
| async_tree_none_tg       | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| sympy_expand             | 474 ms                                                                 | 467 ms: 1.02x faster                                                             |
| xml_etree_parse          | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| xml_etree_iterparse      | 110 ms                                                                 | 108 ms: 1.02x faster                                                             |
| hexiom                   | 6.36 ms                                                                | 6.26 ms: 1.02x faster                                                            |
| regex_compile            | 136 ms                                                                 | 134 ms: 1.02x faster                                                             |
| regex_effbot             | 3.74 ms                                                                | 3.69 ms: 1.01x faster                                                            |
| deltablue                | 3.23 ms                                                                | 3.18 ms: 1.01x faster                                                            |
| generators               | 29.7 ms                                                                | 29.3 ms: 1.01x faster                                                            |
| pycparser                | 1.21 sec                                                               | 1.20 sec: 1.01x faster                                                           |
| go                       | 144 ms                                                                 | 142 ms: 1.01x faster                                                             |
| genshi_xml               | 52.3 ms                                                                | 51.7 ms: 1.01x faster                                                            |
| deepcopy_reduce          | 3.21 us                                                                | 3.17 us: 1.01x faster                                                            |
| chaos                    | 60.6 ms                                                                | 60.0 ms: 1.01x faster                                                            |
| comprehensions           | 17.0 us                                                                | 16.8 us: 1.01x faster                                                            |
| json                     | 5.37 ms                                                                | 5.32 ms: 1.01x faster                                                            |
| sqlglot_optimize         | 55.7 ms                                                                | 55.2 ms: 1.01x faster                                                            |
| create_gc_cycles         | 1.74 ms                                                                | 1.73 ms: 1.01x faster                                                            |
| scimark_sparse_mat_mult  | 5.25 ms                                                                | 5.21 ms: 1.01x faster                                                            |
| sqlglot_parse            | 1.29 ms                                                                | 1.28 ms: 1.01x faster                                                            |
| pickle_pure_python       | 302 us                                                                 | 299 us: 1.01x faster                                                             |
| nqueens                  | 82.1 ms                                                                | 81.5 ms: 1.01x faster                                                            |
| sqlglot_normalize        | 112 ms                                                                 | 111 ms: 1.01x faster                                                             |
| pylint                   | 280 ms                                                                 | 278 ms: 1.01x faster                                                             |
| 2to3                     | 272 ms                                                                 | 270 ms: 1.01x faster                                                             |
| nbody                    | 89.3 ms                                                                | 88.8 ms: 1.01x faster                                                            |
| float                    | 78.9 ms                                                                | 78.5 ms: 1.01x faster                                                            |
| pprint_pformat           | 1.55 sec                                                               | 1.54 sec: 1.01x faster                                                           |
| sympy_sum                | 157 ms                                                                 | 156 ms: 1.01x faster                                                             |
| pidigits                 | 191 ms                                                                 | 190 ms: 1.01x faster                                                             |
| regex_v8                 | 26.1 ms                                                                | 25.9 ms: 1.00x faster                                                            |
| async_generators         | 449 ms                                                                 | 447 ms: 1.00x faster                                                             |
| fannkuch                 | 397 ms                                                                 | 395 ms: 1.00x faster                                                             |
| meteor_contest           | 111 ms                                                                 | 110 ms: 1.00x faster                                                             |
| sqlglot_transpile        | 1.59 ms                                                                | 1.59 ms: 1.00x faster                                                            |
| docutils                 | 2.83 sec                                                               | 2.81 sec: 1.00x faster                                                           |
| bench_thread_pool        | 838 us                                                                 | 835 us: 1.00x faster                                                             |
| regex_dna                | 226 ms                                                                 | 225 ms: 1.00x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| python_startup           | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| deepcopy                 | 354 us                                                                 | 355 us: 1.00x slower                                                             |
| python_startup_no_site   | 8.96 ms                                                                | 9.00 ms: 1.00x slower                                                            |
| coroutines               | 22.3 ms                                                                | 22.4 ms: 1.00x slower                                                            |
| pprint_safe_repr         | 750 ms                                                                 | 754 ms: 1.01x slower                                                             |
| xml_etree_generate       | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| json_loads               | 28.5 us                                                                | 28.7 us: 1.01x slower                                                            |
| unpickle                 | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| xml_etree_process        | 60.3 ms                                                                | 60.8 ms: 1.01x slower                                                            |
| raytrace                 | 262 ms                                                                 | 264 ms: 1.01x slower                                                             |
| pickle                   | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| typing_runtime_protocols | 113 us                                                                 | 114 us: 1.01x slower                                                             |
| scimark_lu               | 114 ms                                                                 | 115 ms: 1.01x slower                                                             |
| coverage                 | 96.9 ms                                                                | 98.2 ms: 1.01x slower                                                            |
| pickle_dict              | 34.5 us                                                                | 35.0 us: 1.01x slower                                                            |
| asyncio_tcp              | 499 ms                                                                 | 508 ms: 1.02x slower                                                             |
| crypto_pyaes             | 74.6 ms                                                                | 75.9 ms: 1.02x slower                                                            |
| unpickle_list            | 5.09 us                                                                | 5.35 us: 1.05x slower                                                            |
| mdp                      | 2.62 sec                                                               | 2.79 sec: 1.07x slower                                                           |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (24): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, mypy2, async_tree_io_tg, gunicorn, sympy_str, thrift, dask, asyncio_websockets, bench_mp_pool, sympy_integrate, sqlite_synth, tornado_http, scimark_sor, pyflate, async_tree_io, dulwich_log, aiohttp, pathlib, json_dumps, html5lib

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x