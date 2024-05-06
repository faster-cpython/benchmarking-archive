# Results vs. base

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.00x faster
- HPT reliability: 74.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 297 ms                                                                       | 298 ms: 1.00x slower                                                |
| chameleon      | 7.41 ms                                                                      | 7.46 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                        |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_none, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 101 ms                                                                       | 95.1 ms: 1.06x faster                                               |
| float          | 75.9 ms                                                                      | 75.0 ms: 1.01x faster                                               |
| pidigits       | 262 ms                                                                       | 261 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                        | 1.03x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 247 ms                                                                       | 241 ms: 1.03x faster                                                |
| regex_compile  | 148 ms                                                                       | 148 ms: 1.00x slower                                                |
| regex_effbot   | 3.45 ms                                                                      | 3.52 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 33.7 us                                                                      | 32.7 us: 1.03x faster                                               |
| xml_etree_parse      | 149 ms                                                                       | 146 ms: 1.02x faster                                                |
| unpickle_pure_python | 239 us                                                                       | 234 us: 1.02x faster                                                |
| xml_etree_process    | 58.6 ms                                                                      | 57.9 ms: 1.01x faster                                               |
| unpickle_list        | 4.58 us                                                                      | 4.54 us: 1.01x faster                                               |
| xml_etree_generate   | 84.0 ms                                                                      | 83.4 ms: 1.01x faster                                               |
| unpickle             | 15.1 us                                                                      | 15.2 us: 1.00x slower                                               |
| tomli_loads          | 2.15 sec                                                                     | 2.16 sec: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (6): xml_etree_iterparse, json_dumps, pickle, pickle_list, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x faster                                               |
| python_startup         | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                               |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text    | 26.8 ms                                                                      | 26.4 ms: 1.02x faster                                               |
| genshi_xml     | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                               |
| mako           | 9.91 ms                                                                      | 9.85 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|--------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody                    | 101 ms                                                                       | 95.1 ms: 1.06x faster                                               |
| pickle_dict              | 33.7 us                                                                      | 32.7 us: 1.03x faster                                               |
| gc_traversal             | 4.54 ms                                                                      | 4.41 ms: 1.03x faster                                               |
| scimark_monte_carlo      | 71.5 ms                                                                      | 69.5 ms: 1.03x faster                                               |
| pycparser                | 1.28 sec                                                                     | 1.24 sec: 1.03x faster                                              |
| nqueens                  | 105 ms                                                                       | 103 ms: 1.03x faster                                                |
| regex_dna                | 247 ms                                                                       | 241 ms: 1.03x faster                                                |
| xml_etree_parse          | 149 ms                                                                       | 146 ms: 1.02x faster                                                |
| unpickle_pure_python     | 239 us                                                                       | 234 us: 1.02x faster                                                |
| pprint_safe_repr         | 851 ms                                                                       | 836 ms: 1.02x faster                                                |
| mdp                      | 2.64 sec                                                                     | 2.59 sec: 1.02x faster                                              |
| genshi_text              | 26.8 ms                                                                      | 26.4 ms: 1.02x faster                                               |
| go                       | 177 ms                                                                       | 175 ms: 1.01x faster                                                |
| dulwich_log              | 69.8 ms                                                                      | 68.7 ms: 1.01x faster                                               |
| pprint_pformat           | 1.74 sec                                                                     | 1.71 sec: 1.01x faster                                              |
| float                    | 75.9 ms                                                                      | 75.0 ms: 1.01x faster                                               |
| xml_etree_process        | 58.6 ms                                                                      | 57.9 ms: 1.01x faster                                               |
| deepcopy                 | 394 us                                                                       | 390 us: 1.01x faster                                                |
| unpickle_list            | 4.58 us                                                                      | 4.54 us: 1.01x faster                                               |
| logging_format           | 7.21 us                                                                      | 7.15 us: 1.01x faster                                               |
| scimark_sor              | 154 ms                                                                       | 153 ms: 1.01x faster                                                |
| genshi_xml               | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                               |
| json                     | 5.51 ms                                                                      | 5.47 ms: 1.01x faster                                               |
| xml_etree_generate       | 84.0 ms                                                                      | 83.4 ms: 1.01x faster                                               |
| mako                     | 9.91 ms                                                                      | 9.85 ms: 1.01x faster                                               |
| asyncio_tcp              | 373 ms                                                                       | 370 ms: 1.01x faster                                                |
| crypto_pyaes             | 77.1 ms                                                                      | 76.7 ms: 1.01x faster                                               |
| deepcopy_memo            | 38.6 us                                                                      | 38.4 us: 1.01x faster                                               |
| sqlglot_parse            | 1.41 ms                                                                      | 1.40 ms: 1.01x faster                                               |
| scimark_fft              | 314 ms                                                                       | 313 ms: 1.00x faster                                                |
| sympy_integrate          | 25.5 ms                                                                      | 25.4 ms: 1.00x faster                                               |
| pidigits                 | 262 ms                                                                       | 261 ms: 1.00x faster                                                |
| python_startup_no_site   | 11.8 ms                                                                      | 11.8 ms: 1.00x faster                                               |
| python_startup           | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                               |
| regex_compile            | 148 ms                                                                       | 148 ms: 1.00x slower                                                |
| 2to3                     | 297 ms                                                                       | 298 ms: 1.00x slower                                                |
| telco                    | 7.98 ms                                                                      | 8.01 ms: 1.00x slower                                               |
| unpickle                 | 15.1 us                                                                      | 15.2 us: 1.00x slower                                               |
| pathlib                  | 19.4 ms                                                                      | 19.5 ms: 1.01x slower                                               |
| sqlglot_optimize         | 62.3 ms                                                                      | 62.7 ms: 1.01x slower                                               |
| pylint                   | 336 ms                                                                       | 338 ms: 1.01x slower                                                |
| chameleon                | 7.41 ms                                                                      | 7.46 ms: 1.01x slower                                               |
| tomli_loads              | 2.15 sec                                                                     | 2.16 sec: 1.01x slower                                              |
| deltablue                | 3.58 ms                                                                      | 3.61 ms: 1.01x slower                                               |
| typing_runtime_protocols | 119 us                                                                       | 120 us: 1.01x slower                                                |
| pyflate                  | 482 ms                                                                       | 487 ms: 1.01x slower                                                |
| create_gc_cycles         | 1.84 ms                                                                      | 1.86 ms: 1.01x slower                                               |
| thrift                   | 890 us                                                                       | 902 us: 1.01x slower                                                |
| meteor_contest           | 131 ms                                                                       | 133 ms: 1.01x slower                                                |
| regex_effbot             | 3.45 ms                                                                      | 3.52 ms: 1.02x slower                                               |
| logging_silent           | 95.9 ns                                                                      | 97.8 ns: 1.02x slower                                               |
| raytrace                 | 285 ms                                                                       | 291 ms: 1.02x slower                                                |
| async_generators         | 388 ms                                                                       | 397 ms: 1.02x slower                                                |
| scimark_lu               | 121 ms                                                                       | 124 ms: 1.03x slower                                                |
| coverage                 | 81.8 ms                                                                      | 86.4 ms: 1.06x slower                                               |
| coroutines               | 22.0 ms                                                                      | 23.4 ms: 1.06x slower                                               |
| Geometric mean           | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (43): bench_mp_pool, bench_thread_pool, chaos, logging_simple, async_tree_memoization_tg, async_tree_none, sqlglot_transpile, dask, xml_etree_iterparse, sympy_str, sympy_expand, json_dumps, scimark_sparse_mat_mult, tornado_http, sqlite_synth, fannkuch, async_tree_none_tg, regex_v8, comprehensions, aiohttp, hexiom, generators, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, pickle, pickle_list, mypy2, asyncio_websockets, docutils, sympy_sum, json_loads, pickle_pure_python, async_tree_io_tg, sqlglot_normalize, async_tree_cpu_io_mixed, html5lib, richards_super, richards, deepcopy_reduce, spectral_norm, gunicorn, async_tree_memoization, async_tree_io

# HPT report

- Reliability score: 74.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x