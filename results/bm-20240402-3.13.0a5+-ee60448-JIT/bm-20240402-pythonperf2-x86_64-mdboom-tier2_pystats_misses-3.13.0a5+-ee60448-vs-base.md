# Results vs. base

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.00x slower
- HPT reliability: 96.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 297 ms                                                                       | 300 ms: 1.01x slower                                                         |
| chameleon      | 7.41 ms                                                                      | 7.54 ms: 1.02x slower                                                        |
| docutils       | 3.09 sec                                                                     | 3.11 sec: 1.00x slower                                                       |
| tornado_http   | 122 ms                                                                       | 125 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 101 ms                                                                       | 95.6 ms: 1.06x faster                                                        |
| float          | 75.9 ms                                                                      | 76.6 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                      | 25.9 ms: 1.00x faster                                                        |
| regex_dna      | 247 ms                                                                       | 249 ms: 1.01x slower                                                         |
| regex_compile  | 148 ms                                                                       | 150 ms: 1.01x slower                                                         |
| regex_effbot   | 3.45 ms                                                                      | 3.51 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.1 us                                                                      | 14.5 us: 1.04x faster                                                        |
| xml_etree_parse      | 149 ms                                                                       | 145 ms: 1.03x faster                                                         |
| unpickle_pure_python | 239 us                                                                       | 232 us: 1.03x faster                                                         |
| pickle_dict          | 33.7 us                                                                      | 32.8 us: 1.03x faster                                                        |
| xml_etree_iterparse  | 104 ms                                                                       | 102 ms: 1.01x faster                                                         |
| json_dumps           | 10.6 ms                                                                      | 10.5 ms: 1.01x faster                                                        |
| tomli_loads          | 2.15 sec                                                                     | 2.13 sec: 1.01x faster                                                       |
| pickle_pure_python   | 309 us                                                                       | 311 us: 1.01x slower                                                         |
| xml_etree_generate   | 84.0 ms                                                                      | 84.9 ms: 1.01x slower                                                        |
| unpickle_list        | 4.58 us                                                                      | 4.69 us: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (4): pickle_list, pickle, json_loads, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.9 ms: 1.01x slower                                                        |
| python_startup         | 13.5 ms                                                                      | 13.7 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 9.91 ms                                                                      | 9.96 ms: 1.00x slower                                                        |
| genshi_xml     | 58.5 ms                                                                      | 61.8 ms: 1.06x slower                                                        |
| genshi_text    | 26.8 ms                                                                      | 28.5 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.04x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|--------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody                    | 101 ms                                                                       | 95.6 ms: 1.06x faster                                                        |
| unpickle                 | 15.1 us                                                                      | 14.5 us: 1.04x faster                                                        |
| xml_etree_parse          | 149 ms                                                                       | 145 ms: 1.03x faster                                                         |
| unpickle_pure_python     | 239 us                                                                       | 232 us: 1.03x faster                                                         |
| pickle_dict              | 33.7 us                                                                      | 32.8 us: 1.03x faster                                                        |
| thrift                   | 890 us                                                                       | 871 us: 1.02x faster                                                         |
| logging_simple           | 6.54 us                                                                      | 6.43 us: 1.02x faster                                                        |
| logging_format           | 7.21 us                                                                      | 7.10 us: 1.02x faster                                                        |
| comprehensions           | 19.5 us                                                                      | 19.2 us: 1.02x faster                                                        |
| xml_etree_iterparse      | 104 ms                                                                       | 102 ms: 1.01x faster                                                         |
| scimark_monte_carlo      | 71.5 ms                                                                      | 70.6 ms: 1.01x faster                                                        |
| mdp                      | 2.64 sec                                                                     | 2.60 sec: 1.01x faster                                                       |
| scimark_sor              | 154 ms                                                                       | 152 ms: 1.01x faster                                                         |
| json_dumps               | 10.6 ms                                                                      | 10.5 ms: 1.01x faster                                                        |
| tomli_loads              | 2.15 sec                                                                     | 2.13 sec: 1.01x faster                                                       |
| hexiom                   | 7.39 ms                                                                      | 7.33 ms: 1.01x faster                                                        |
| sqlglot_normalize        | 122 ms                                                                       | 122 ms: 1.01x faster                                                         |
| spectral_norm            | 93.2 ms                                                                      | 92.6 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult  | 4.13 ms                                                                      | 4.11 ms: 1.01x faster                                                        |
| regex_v8                 | 26.0 ms                                                                      | 25.9 ms: 1.00x faster                                                        |
| crypto_pyaes             | 77.1 ms                                                                      | 76.9 ms: 1.00x faster                                                        |
| scimark_fft              | 314 ms                                                                       | 313 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x faster                                                       |
| mako                     | 9.91 ms                                                                      | 9.96 ms: 1.00x slower                                                        |
| docutils                 | 3.09 sec                                                                     | 3.11 sec: 1.00x slower                                                       |
| pyflate                  | 482 ms                                                                       | 485 ms: 1.01x slower                                                         |
| pickle_pure_python       | 309 us                                                                       | 311 us: 1.01x slower                                                         |
| asyncio_websockets       | 392 ms                                                                       | 395 ms: 1.01x slower                                                         |
| regex_dna                | 247 ms                                                                       | 249 ms: 1.01x slower                                                         |
| raytrace                 | 285 ms                                                                       | 287 ms: 1.01x slower                                                         |
| asyncio_tcp              | 373 ms                                                                       | 376 ms: 1.01x slower                                                         |
| float                    | 75.9 ms                                                                      | 76.6 ms: 1.01x slower                                                        |
| sympy_expand             | 514 ms                                                                       | 518 ms: 1.01x slower                                                         |
| 2to3                     | 297 ms                                                                       | 300 ms: 1.01x slower                                                         |
| python_startup_no_site   | 11.8 ms                                                                      | 11.9 ms: 1.01x slower                                                        |
| xml_etree_generate       | 84.0 ms                                                                      | 84.9 ms: 1.01x slower                                                        |
| sqlglot_transpile        | 1.82 ms                                                                      | 1.84 ms: 1.01x slower                                                        |
| pylint                   | 336 ms                                                                       | 340 ms: 1.01x slower                                                         |
| python_startup           | 13.5 ms                                                                      | 13.7 ms: 1.01x slower                                                        |
| aiohttp                  | 1.13 ms                                                                      | 1.14 ms: 1.01x slower                                                        |
| async_generators         | 388 ms                                                                       | 393 ms: 1.01x slower                                                         |
| coverage                 | 81.8 ms                                                                      | 82.9 ms: 1.01x slower                                                        |
| regex_compile            | 148 ms                                                                       | 150 ms: 1.01x slower                                                         |
| sqlglot_parse            | 1.41 ms                                                                      | 1.43 ms: 1.01x slower                                                        |
| pathlib                  | 19.4 ms                                                                      | 19.7 ms: 1.01x slower                                                        |
| pprint_pformat           | 1.74 sec                                                                     | 1.76 sec: 1.01x slower                                                       |
| regex_effbot             | 3.45 ms                                                                      | 3.51 ms: 1.02x slower                                                        |
| sympy_integrate          | 25.5 ms                                                                      | 25.9 ms: 1.02x slower                                                        |
| chameleon                | 7.41 ms                                                                      | 7.54 ms: 1.02x slower                                                        |
| sympy_sum                | 164 ms                                                                       | 167 ms: 1.02x slower                                                         |
| sympy_str                | 306 ms                                                                       | 312 ms: 1.02x slower                                                         |
| deepcopy_memo            | 38.6 us                                                                      | 39.4 us: 1.02x slower                                                        |
| gunicorn                 | 1.09 ms                                                                      | 1.12 ms: 1.02x slower                                                        |
| create_gc_cycles         | 1.84 ms                                                                      | 1.88 ms: 1.02x slower                                                        |
| tornado_http             | 122 ms                                                                       | 125 ms: 1.02x slower                                                         |
| unpickle_list            | 4.58 us                                                                      | 4.69 us: 1.02x slower                                                        |
| richards_super           | 56.8 ms                                                                      | 58.3 ms: 1.03x slower                                                        |
| dulwich_log              | 69.8 ms                                                                      | 71.7 ms: 1.03x slower                                                        |
| meteor_contest           | 131 ms                                                                       | 134 ms: 1.03x slower                                                         |
| deepcopy_reduce          | 3.42 us                                                                      | 3.51 us: 1.03x slower                                                        |
| typing_runtime_protocols | 119 us                                                                       | 124 us: 1.04x slower                                                         |
| scimark_lu               | 121 ms                                                                       | 126 ms: 1.05x slower                                                         |
| genshi_xml               | 58.5 ms                                                                      | 61.8 ms: 1.06x slower                                                        |
| genshi_text              | 26.8 ms                                                                      | 28.5 ms: 1.06x slower                                                        |
| gc_traversal             | 4.54 ms                                                                      | 4.84 ms: 1.07x slower                                                        |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (34): async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, json, async_tree_none_tg, pickle_list, async_tree_io_tg, generators, nqueens, sqlite_synth, logging_silent, pycparser, pickle, json_loads, pidigits, chaos, coroutines, go, sqlglot_optimize, richards, pprint_safe_repr, fannkuch, deltablue, dask, bench_mp_pool, xml_etree_process, html5lib, deepcopy, telco, bench_thread_pool, mypy2, async_tree_io

# HPT report

- Reliability score: 96.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x