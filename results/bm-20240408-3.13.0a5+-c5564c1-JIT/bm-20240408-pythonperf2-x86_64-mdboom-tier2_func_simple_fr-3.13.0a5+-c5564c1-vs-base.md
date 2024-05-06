# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.00x slower
- HPT reliability: 85.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 298 ms: 1.00x slower                                                         |
| chameleon      | 7.43 ms                                                                      | 7.70 ms: 1.04x slower                                                        |
| html5lib       | 74.4 ms                                                                      | 73.7 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io  | 852 ms                                                                       | 847 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 77.2 ms                                                                      | 76.3 ms: 1.01x faster                                                        |
| nbody          | 94.5 ms                                                                      | 96.2 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                                       | 238 ms: 1.05x faster                                                         |
| regex_v8       | 26.0 ms                                                                      | 25.3 ms: 1.03x faster                                                        |
| regex_compile  | 146 ms                                                                       | 148 ms: 1.01x slower                                                         |
| regex_effbot   | 3.53 ms                                                                      | 3.58 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.3 us                                                                      | 14.6 us: 1.05x faster                                                        |
| xml_etree_parse      | 147 ms                                                                       | 143 ms: 1.03x faster                                                         |
| xml_etree_iterparse  | 102 ms                                                                       | 101 ms: 1.01x faster                                                         |
| pickle_pure_python   | 309 us                                                                       | 310 us: 1.01x slower                                                         |
| json_loads           | 25.3 us                                                                      | 25.4 us: 1.01x slower                                                        |
| json_dumps           | 10.5 ms                                                                      | 10.5 ms: 1.01x slower                                                        |
| unpickle_pure_python | 230 us                                                                       | 233 us: 1.01x slower                                                         |
| pickle_list          | 4.38 us                                                                      | 4.44 us: 1.01x slower                                                        |
| pickle               | 10.6 us                                                                      | 10.7 us: 1.01x slower                                                        |
| xml_etree_generate   | 84.8 ms                                                                      | 85.9 ms: 1.01x slower                                                        |
| tomli_loads          | 2.14 sec                                                                     | 2.18 sec: 1.02x slower                                                       |
| xml_etree_process    | 58.1 ms                                                                      | 59.2 ms: 1.02x slower                                                        |
| unpickle_list        | 4.57 us                                                                      | 4.67 us: 1.02x slower                                                        |
| pickle_dict          | 32.5 us                                                                      | 34.6 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup | 13.4 ms                                                                      | 13.4 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.00 ms                                                                     | 10.0 ms: 1.00x slower                                                        |
| genshi_text    | 25.7 ms                                                                      | 27.4 ms: 1.07x slower                                                        |
| genshi_xml     | 57.1 ms                                                                      | 60.9 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle                 | 15.3 us                                                                      | 14.6 us: 1.05x faster                                                        |
| regex_dna                | 249 ms                                                                       | 238 ms: 1.05x faster                                                         |
| richards_super           | 54.4 ms                                                                      | 52.1 ms: 1.04x faster                                                        |
| pyflate                  | 498 ms                                                                       | 481 ms: 1.03x faster                                                         |
| nqueens                  | 103 ms                                                                       | 99.7 ms: 1.03x faster                                                        |
| xml_etree_parse          | 147 ms                                                                       | 143 ms: 1.03x faster                                                         |
| regex_v8                 | 26.0 ms                                                                      | 25.3 ms: 1.03x faster                                                        |
| richards                 | 46.9 ms                                                                      | 45.8 ms: 1.03x faster                                                        |
| chaos                    | 65.2 ms                                                                      | 64.2 ms: 1.02x faster                                                        |
| thrift                   | 897 us                                                                       | 884 us: 1.01x faster                                                         |
| gunicorn                 | 1.10 ms                                                                      | 1.09 ms: 1.01x faster                                                        |
| coroutines               | 22.5 ms                                                                      | 22.2 ms: 1.01x faster                                                        |
| logging_simple           | 6.37 us                                                                      | 6.30 us: 1.01x faster                                                        |
| float                    | 77.2 ms                                                                      | 76.3 ms: 1.01x faster                                                        |
| html5lib                 | 74.4 ms                                                                      | 73.7 ms: 1.01x faster                                                        |
| gc_traversal             | 4.42 ms                                                                      | 4.38 ms: 1.01x faster                                                        |
| mdp                      | 2.63 sec                                                                     | 2.61 sec: 1.01x faster                                                       |
| meteor_contest           | 133 ms                                                                       | 132 ms: 1.01x faster                                                         |
| dulwich_log              | 68.2 ms                                                                      | 67.7 ms: 1.01x faster                                                        |
| async_tree_io            | 852 ms                                                                       | 847 ms: 1.01x faster                                                         |
| telco                    | 8.09 ms                                                                      | 8.05 ms: 1.01x faster                                                        |
| xml_etree_iterparse      | 102 ms                                                                       | 101 ms: 1.01x faster                                                         |
| asyncio_tcp              | 375 ms                                                                       | 373 ms: 1.01x faster                                                         |
| coverage                 | 84.2 ms                                                                      | 83.9 ms: 1.00x faster                                                        |
| python_startup           | 13.4 ms                                                                      | 13.4 ms: 1.00x faster                                                        |
| 2to3                     | 298 ms                                                                       | 298 ms: 1.00x slower                                                         |
| mako                     | 10.00 ms                                                                     | 10.0 ms: 1.00x slower                                                        |
| sqlglot_transpile        | 1.81 ms                                                                      | 1.81 ms: 1.00x slower                                                        |
| pylint                   | 333 ms                                                                       | 334 ms: 1.00x slower                                                         |
| pickle_pure_python       | 309 us                                                                       | 310 us: 1.01x slower                                                         |
| json_loads               | 25.3 us                                                                      | 25.4 us: 1.01x slower                                                        |
| sqlglot_optimize         | 62.3 ms                                                                      | 62.7 ms: 1.01x slower                                                        |
| sympy_integrate          | 25.1 ms                                                                      | 25.3 ms: 1.01x slower                                                        |
| sqlglot_normalize        | 121 ms                                                                       | 121 ms: 1.01x slower                                                         |
| generators               | 33.0 ms                                                                      | 33.2 ms: 1.01x slower                                                        |
| regex_compile            | 146 ms                                                                       | 148 ms: 1.01x slower                                                         |
| json_dumps               | 10.5 ms                                                                      | 10.5 ms: 1.01x slower                                                        |
| pathlib                  | 19.4 ms                                                                      | 19.5 ms: 1.01x slower                                                        |
| sympy_sum                | 163 ms                                                                       | 164 ms: 1.01x slower                                                         |
| create_gc_cycles         | 1.86 ms                                                                      | 1.87 ms: 1.01x slower                                                        |
| crypto_pyaes             | 77.1 ms                                                                      | 77.8 ms: 1.01x slower                                                        |
| comprehensions           | 19.0 us                                                                      | 19.2 us: 1.01x slower                                                        |
| sqlite_synth             | 2.70 us                                                                      | 2.73 us: 1.01x slower                                                        |
| spectral_norm            | 92.3 ms                                                                      | 93.3 ms: 1.01x slower                                                        |
| unpickle_pure_python     | 230 us                                                                       | 233 us: 1.01x slower                                                         |
| regex_effbot             | 3.53 ms                                                                      | 3.58 ms: 1.01x slower                                                        |
| pickle_list              | 4.38 us                                                                      | 4.44 us: 1.01x slower                                                        |
| pickle                   | 10.6 us                                                                      | 10.7 us: 1.01x slower                                                        |
| xml_etree_generate       | 84.8 ms                                                                      | 85.9 ms: 1.01x slower                                                        |
| tomli_loads              | 2.14 sec                                                                     | 2.18 sec: 1.02x slower                                                       |
| async_generators         | 376 ms                                                                       | 382 ms: 1.02x slower                                                         |
| nbody                    | 94.5 ms                                                                      | 96.2 ms: 1.02x slower                                                        |
| xml_etree_process        | 58.1 ms                                                                      | 59.2 ms: 1.02x slower                                                        |
| aiohttp                  | 1.11 ms                                                                      | 1.13 ms: 1.02x slower                                                        |
| fannkuch                 | 391 ms                                                                       | 398 ms: 1.02x slower                                                         |
| bench_mp_pool            | 4.62 ms                                                                      | 4.71 ms: 1.02x slower                                                        |
| scimark_fft              | 313 ms                                                                       | 320 ms: 1.02x slower                                                         |
| unpickle_list            | 4.57 us                                                                      | 4.67 us: 1.02x slower                                                        |
| go                       | 176 ms                                                                       | 180 ms: 1.02x slower                                                         |
| deepcopy                 | 385 us                                                                       | 398 us: 1.03x slower                                                         |
| deepcopy_reduce          | 3.39 us                                                                      | 3.50 us: 1.03x slower                                                        |
| chameleon                | 7.43 ms                                                                      | 7.70 ms: 1.04x slower                                                        |
| typing_runtime_protocols | 119 us                                                                       | 123 us: 1.04x slower                                                         |
| scimark_sor              | 150 ms                                                                       | 156 ms: 1.04x slower                                                         |
| deepcopy_memo            | 37.3 us                                                                      | 38.9 us: 1.04x slower                                                        |
| pickle_dict              | 32.5 us                                                                      | 34.6 us: 1.06x slower                                                        |
| genshi_text              | 25.7 ms                                                                      | 27.4 ms: 1.07x slower                                                        |
| genshi_xml               | 57.1 ms                                                                      | 60.9 ms: 1.07x slower                                                        |
| scimark_lu               | 120 ms                                                                       | 128 ms: 1.07x slower                                                         |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (30): async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, json, scimark_monte_carlo, hexiom, pprint_pformat, sqlglot_parse, async_tree_memoization, raytrace, async_tree_cpu_io_mixed_tg, logging_format, async_tree_none_tg, sympy_expand, scimark_sparse_mat_mult, pycparser, mypy2, python_startup_no_site, async_tree_memoization_tg, pidigits, pprint_safe_repr, sympy_str, asyncio_tcp_ssl, deltablue, docutils, asyncio_websockets, tornado_http, bench_thread_pool, logging_silent, dask

# HPT report

- Reliability score: 85.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x