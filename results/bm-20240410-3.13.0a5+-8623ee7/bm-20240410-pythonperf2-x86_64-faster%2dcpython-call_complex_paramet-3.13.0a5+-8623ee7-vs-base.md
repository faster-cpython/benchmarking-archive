# Results vs. base

- fork: faster-cpython
- ref: call_complex_paramet
- machine: linux-x86_64
- commit hash: 8623ee7
- commit date: 2024-04-10
- overall geometric mean: 1.01x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 288 ms                                                                       | 292 ms: 1.01x slower                                                                   |
| chameleon      | 7.33 ms                                                                      | 7.12 ms: 1.03x faster                                                                  |
| html5lib       | 74.2 ms                                                                      | 74.6 ms: 1.01x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 263 ms                                                                       | 262 ms: 1.00x faster                                                                   |
| float          | 75.6 ms                                                                      | 77.2 ms: 1.02x slower                                                                  |
| nbody          | 84.4 ms                                                                      | 90.0 ms: 1.07x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.03x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_effbot   | 3.54 ms                                                                      | 3.56 ms: 1.00x slower                                                                  |
| regex_v8       | 25.2 ms                                                                      | 26.0 ms: 1.03x slower                                                                  |
| regex_dna      | 231 ms                                                                       | 252 ms: 1.09x slower                                                                   |
| Geometric mean | (ref)                                                                        | 1.03x slower                                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| xml_etree_parse      | 149 ms                                                                       | 146 ms: 1.02x faster                                                                   |
| xml_etree_generate   | 84.3 ms                                                                      | 84.5 ms: 1.00x slower                                                                  |
| tomli_loads          | 2.17 sec                                                                     | 2.19 sec: 1.01x slower                                                                 |
| unpickle             | 14.7 us                                                                      | 14.9 us: 1.02x slower                                                                  |
| json_loads           | 25.4 us                                                                      | 25.9 us: 1.02x slower                                                                  |
| unpickle_list        | 4.51 us                                                                      | 4.60 us: 1.02x slower                                                                  |
| pickle_pure_python   | 306 us                                                                       | 315 us: 1.03x slower                                                                   |
| unpickle_pure_python | 214 us                                                                       | 225 us: 1.06x slower                                                                   |
| Geometric mean       | (ref)                                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (6): pickle_list, json_dumps, pickle, xml_etree_process, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                      | 11.1 ms: 1.00x slower                                                                  |
| python_startup         | 12.8 ms                                                                      | 12.9 ms: 1.00x slower                                                                  |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 10.1 ms                                                                      | 10.2 ms: 1.01x slower                                                                  |
| genshi_xml     | 53.8 ms                                                                      | 54.3 ms: 1.01x slower                                                                  |
| genshi_text    | 24.7 ms                                                                      | 25.1 ms: 1.02x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240408-pythonperf2-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 119 us                                                                       | 114 us: 1.05x faster                                                                   |
| coverage                 | 88.7 ms                                                                      | 85.3 ms: 1.04x faster                                                                  |
| chameleon                | 7.33 ms                                                                      | 7.12 ms: 1.03x faster                                                                  |
| crypto_pyaes             | 73.7 ms                                                                      | 71.8 ms: 1.03x faster                                                                  |
| create_gc_cycles         | 1.92 ms                                                                      | 1.87 ms: 1.02x faster                                                                  |
| aiohttp                  | 1.10 ms                                                                      | 1.07 ms: 1.02x faster                                                                  |
| xml_etree_parse          | 149 ms                                                                       | 146 ms: 1.02x faster                                                                   |
| gunicorn                 | 1.06 ms                                                                      | 1.04 ms: 1.02x faster                                                                  |
| comprehensions           | 16.8 us                                                                      | 16.6 us: 1.02x faster                                                                  |
| thrift                   | 892 us                                                                       | 880 us: 1.01x faster                                                                   |
| go                       | 173 ms                                                                       | 170 ms: 1.01x faster                                                                   |
| scimark_fft              | 301 ms                                                                       | 297 ms: 1.01x faster                                                                   |
| telco                    | 8.21 ms                                                                      | 8.11 ms: 1.01x faster                                                                  |
| spectral_norm            | 96.0 ms                                                                      | 95.0 ms: 1.01x faster                                                                  |
| deltablue                | 3.48 ms                                                                      | 3.45 ms: 1.01x faster                                                                  |
| sqlglot_optimize         | 59.0 ms                                                                      | 58.6 ms: 1.01x faster                                                                  |
| sympy_str                | 297 ms                                                                       | 296 ms: 1.00x faster                                                                   |
| dulwich_log              | 68.3 ms                                                                      | 68.0 ms: 1.00x faster                                                                  |
| sympy_integrate          | 23.5 ms                                                                      | 23.4 ms: 1.00x faster                                                                  |
| pidigits                 | 263 ms                                                                       | 262 ms: 1.00x faster                                                                   |
| xml_etree_generate       | 84.3 ms                                                                      | 84.5 ms: 1.00x slower                                                                  |
| python_startup_no_site   | 11.1 ms                                                                      | 11.1 ms: 1.00x slower                                                                  |
| hexiom                   | 6.43 ms                                                                      | 6.45 ms: 1.00x slower                                                                  |
| mdp                      | 2.54 sec                                                                     | 2.54 sec: 1.00x slower                                                                 |
| sqlglot_normalize        | 117 ms                                                                       | 118 ms: 1.00x slower                                                                   |
| python_startup           | 12.8 ms                                                                      | 12.9 ms: 1.00x slower                                                                  |
| asyncio_tcp              | 371 ms                                                                       | 372 ms: 1.00x slower                                                                   |
| regex_effbot             | 3.54 ms                                                                      | 3.56 ms: 1.00x slower                                                                  |
| raytrace                 | 257 ms                                                                       | 258 ms: 1.00x slower                                                                   |
| richards_super           | 57.9 ms                                                                      | 58.2 ms: 1.00x slower                                                                  |
| sqlglot_transpile        | 1.77 ms                                                                      | 1.78 ms: 1.01x slower                                                                  |
| html5lib                 | 74.2 ms                                                                      | 74.6 ms: 1.01x slower                                                                  |
| mako                     | 10.1 ms                                                                      | 10.2 ms: 1.01x slower                                                                  |
| genshi_xml               | 53.8 ms                                                                      | 54.3 ms: 1.01x slower                                                                  |
| sqlglot_parse            | 1.38 ms                                                                      | 1.40 ms: 1.01x slower                                                                  |
| generators               | 33.2 ms                                                                      | 33.6 ms: 1.01x slower                                                                  |
| meteor_contest           | 128 ms                                                                       | 129 ms: 1.01x slower                                                                   |
| 2to3                     | 288 ms                                                                       | 292 ms: 1.01x slower                                                                   |
| tomli_loads              | 2.17 sec                                                                     | 2.19 sec: 1.01x slower                                                                 |
| asyncio_websockets       | 390 ms                                                                       | 395 ms: 1.01x slower                                                                   |
| pprint_safe_repr         | 782 ms                                                                       | 792 ms: 1.01x slower                                                                   |
| pprint_pformat           | 1.60 sec                                                                     | 1.62 sec: 1.01x slower                                                                 |
| unpickle                 | 14.7 us                                                                      | 14.9 us: 1.02x slower                                                                  |
| genshi_text              | 24.7 ms                                                                      | 25.1 ms: 1.02x slower                                                                  |
| json_loads               | 25.4 us                                                                      | 25.9 us: 1.02x slower                                                                  |
| unpickle_list            | 4.51 us                                                                      | 4.60 us: 1.02x slower                                                                  |
| chaos                    | 58.7 ms                                                                      | 59.9 ms: 1.02x slower                                                                  |
| fannkuch                 | 384 ms                                                                       | 392 ms: 1.02x slower                                                                   |
| logging_format           | 7.11 us                                                                      | 7.27 us: 1.02x slower                                                                  |
| float                    | 75.6 ms                                                                      | 77.2 ms: 1.02x slower                                                                  |
| nqueens                  | 87.9 ms                                                                      | 90.1 ms: 1.02x slower                                                                  |
| pickle_pure_python       | 306 us                                                                       | 315 us: 1.03x slower                                                                   |
| pathlib                  | 18.9 ms                                                                      | 19.4 ms: 1.03x slower                                                                  |
| async_generators         | 354 ms                                                                       | 364 ms: 1.03x slower                                                                   |
| scimark_sparse_mat_mult  | 4.12 ms                                                                      | 4.24 ms: 1.03x slower                                                                  |
| regex_v8                 | 25.2 ms                                                                      | 26.0 ms: 1.03x slower                                                                  |
| deepcopy                 | 376 us                                                                       | 387 us: 1.03x slower                                                                   |
| gc_traversal             | 4.54 ms                                                                      | 4.68 ms: 1.03x slower                                                                  |
| pycparser                | 1.23 sec                                                                     | 1.27 sec: 1.03x slower                                                                 |
| pyflate                  | 504 ms                                                                       | 523 ms: 1.04x slower                                                                   |
| logging_simple           | 6.33 us                                                                      | 6.59 us: 1.04x slower                                                                  |
| scimark_monte_carlo      | 67.2 ms                                                                      | 70.1 ms: 1.04x slower                                                                  |
| unpickle_pure_python     | 214 us                                                                       | 225 us: 1.06x slower                                                                   |
| nbody                    | 84.4 ms                                                                      | 90.0 ms: 1.07x slower                                                                  |
| regex_dna                | 231 ms                                                                       | 252 ms: 1.09x slower                                                                   |
| Geometric mean           | (ref)                                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (34): deepcopy_memo, bench_thread_pool, pickle_list, logging_silent, sympy_sum, json, json_dumps, async_tree_cpu_io_mixed, pylint, pickle, asyncio_tcp_ssl, regex_compile, scimark_sor, xml_etree_process, docutils, scimark_lu, sympy_expand, async_tree_memoization, sqlite_synth, xml_etree_iterparse, pickle_dict, tornado_http, async_tree_none, async_tree_cpu_io_mixed_tg, deepcopy_reduce, mypy2, richards, coroutines, dask, async_tree_memoization_tg, async_tree_none_tg, bench_mp_pool, async_tree_io, async_tree_io_tg

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x