# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.01x slower
- HPT reliability: 99.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 300 ms: 1.01x slower                                                         |
| chameleon      | 7.43 ms                                                                      | 7.65 ms: 1.03x slower                                                        |
| docutils       | 3.08 sec                                                                     | 3.10 sec: 1.01x slower                                                       |
| html5lib       | 74.4 ms                                                                      | 75.3 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io  | 852 ms                                                                       | 871 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 77.2 ms                                                                      | 76.1 ms: 1.01x faster                                                        |
| nbody          | 94.5 ms                                                                      | 96.2 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                      | 25.5 ms: 1.02x faster                                                        |
| regex_dna      | 249 ms                                                                       | 245 ms: 1.02x faster                                                         |
| regex_compile  | 146 ms                                                                       | 148 ms: 1.01x slower                                                         |
| regex_effbot   | 3.53 ms                                                                      | 3.71 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.3 us                                                                      | 15.0 us: 1.02x faster                                                        |
| tomli_loads          | 2.14 sec                                                                     | 2.13 sec: 1.01x faster                                                       |
| json_dumps           | 10.5 ms                                                                      | 10.4 ms: 1.00x faster                                                        |
| xml_etree_generate   | 84.8 ms                                                                      | 84.6 ms: 1.00x faster                                                        |
| pickle_dict          | 32.5 us                                                                      | 32.6 us: 1.00x slower                                                        |
| pickle_pure_python   | 309 us                                                                       | 311 us: 1.01x slower                                                         |
| xml_etree_parse      | 147 ms                                                                       | 148 ms: 1.01x slower                                                         |
| json_loads           | 25.3 us                                                                      | 25.5 us: 1.01x slower                                                        |
| unpickle_pure_python | 230 us                                                                       | 232 us: 1.01x slower                                                         |
| xml_etree_process    | 58.1 ms                                                                      | 59.0 ms: 1.01x slower                                                        |
| unpickle_list        | 4.57 us                                                                      | 4.66 us: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (3): pickle_list, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup | 13.4 ms                                                                      | 13.4 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.00 ms                                                                     | 10.1 ms: 1.01x slower                                                        |
| genshi_xml     | 57.1 ms                                                                      | 61.8 ms: 1.08x slower                                                        |
| genshi_text    | 25.7 ms                                                                      | 28.0 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.06x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf2-x86_64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coverage                 | 84.2 ms                                                                      | 78.8 ms: 1.07x faster                                                        |
| nqueens                  | 103 ms                                                                       | 99.8 ms: 1.03x faster                                                        |
| pyflate                  | 498 ms                                                                       | 483 ms: 1.03x faster                                                         |
| regex_v8                 | 26.0 ms                                                                      | 25.5 ms: 1.02x faster                                                        |
| logging_format           | 7.09 us                                                                      | 6.95 us: 1.02x faster                                                        |
| unpickle                 | 15.3 us                                                                      | 15.0 us: 1.02x faster                                                        |
| coroutines               | 22.5 ms                                                                      | 22.1 ms: 1.02x faster                                                        |
| logging_simple           | 6.37 us                                                                      | 6.27 us: 1.02x faster                                                        |
| json                     | 5.48 ms                                                                      | 5.40 ms: 1.02x faster                                                        |
| regex_dna                | 249 ms                                                                       | 245 ms: 1.02x faster                                                         |
| float                    | 77.2 ms                                                                      | 76.1 ms: 1.01x faster                                                        |
| mdp                      | 2.63 sec                                                                     | 2.59 sec: 1.01x faster                                                       |
| richards_super           | 54.4 ms                                                                      | 53.7 ms: 1.01x faster                                                        |
| gc_traversal             | 4.42 ms                                                                      | 4.38 ms: 1.01x faster                                                        |
| go                       | 176 ms                                                                       | 175 ms: 1.01x faster                                                         |
| tomli_loads              | 2.14 sec                                                                     | 2.13 sec: 1.01x faster                                                       |
| richards                 | 46.9 ms                                                                      | 46.7 ms: 1.00x faster                                                        |
| fannkuch                 | 391 ms                                                                       | 389 ms: 1.00x faster                                                         |
| asyncio_tcp              | 375 ms                                                                       | 374 ms: 1.00x faster                                                         |
| json_dumps               | 10.5 ms                                                                      | 10.4 ms: 1.00x faster                                                        |
| meteor_contest           | 133 ms                                                                       | 132 ms: 1.00x faster                                                         |
| crypto_pyaes             | 77.1 ms                                                                      | 76.9 ms: 1.00x faster                                                        |
| xml_etree_generate       | 84.8 ms                                                                      | 84.6 ms: 1.00x faster                                                        |
| python_startup           | 13.4 ms                                                                      | 13.4 ms: 1.00x faster                                                        |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x slower                                                       |
| sympy_expand             | 516 ms                                                                       | 518 ms: 1.00x slower                                                         |
| sympy_str                | 308 ms                                                                       | 309 ms: 1.00x slower                                                         |
| pickle_dict              | 32.5 us                                                                      | 32.6 us: 1.00x slower                                                        |
| sqlite_synth             | 2.70 us                                                                      | 2.71 us: 1.00x slower                                                        |
| docutils                 | 3.08 sec                                                                     | 3.10 sec: 1.01x slower                                                       |
| generators               | 33.0 ms                                                                      | 33.2 ms: 1.01x slower                                                        |
| 2to3                     | 298 ms                                                                       | 300 ms: 1.01x slower                                                         |
| comprehensions           | 19.0 us                                                                      | 19.1 us: 1.01x slower                                                        |
| sqlglot_transpile        | 1.81 ms                                                                      | 1.82 ms: 1.01x slower                                                        |
| mako                     | 10.00 ms                                                                     | 10.1 ms: 1.01x slower                                                        |
| pickle_pure_python       | 309 us                                                                       | 311 us: 1.01x slower                                                         |
| create_gc_cycles         | 1.86 ms                                                                      | 1.87 ms: 1.01x slower                                                        |
| xml_etree_parse          | 147 ms                                                                       | 148 ms: 1.01x slower                                                         |
| sqlglot_optimize         | 62.3 ms                                                                      | 62.9 ms: 1.01x slower                                                        |
| scimark_lu               | 120 ms                                                                       | 121 ms: 1.01x slower                                                         |
| json_loads               | 25.3 us                                                                      | 25.5 us: 1.01x slower                                                        |
| unpickle_pure_python     | 230 us                                                                       | 232 us: 1.01x slower                                                         |
| html5lib                 | 74.4 ms                                                                      | 75.3 ms: 1.01x slower                                                        |
| scimark_sparse_mat_mult  | 4.13 ms                                                                      | 4.18 ms: 1.01x slower                                                        |
| pathlib                  | 19.4 ms                                                                      | 19.6 ms: 1.01x slower                                                        |
| scimark_monte_carlo      | 71.2 ms                                                                      | 72.0 ms: 1.01x slower                                                        |
| scimark_fft              | 313 ms                                                                       | 317 ms: 1.01x slower                                                         |
| scimark_sor              | 150 ms                                                                       | 152 ms: 1.01x slower                                                         |
| regex_compile            | 146 ms                                                                       | 148 ms: 1.01x slower                                                         |
| logging_silent           | 97.6 ns                                                                      | 98.9 ns: 1.01x slower                                                        |
| xml_etree_process        | 58.1 ms                                                                      | 59.0 ms: 1.01x slower                                                        |
| spectral_norm            | 92.3 ms                                                                      | 93.8 ms: 1.02x slower                                                        |
| unpickle_list            | 4.57 us                                                                      | 4.66 us: 1.02x slower                                                        |
| nbody                    | 94.5 ms                                                                      | 96.2 ms: 1.02x slower                                                        |
| async_generators         | 376 ms                                                                       | 384 ms: 1.02x slower                                                         |
| async_tree_io            | 852 ms                                                                       | 871 ms: 1.02x slower                                                         |
| telco                    | 8.09 ms                                                                      | 8.29 ms: 1.02x slower                                                        |
| sqlglot_normalize        | 121 ms                                                                       | 124 ms: 1.02x slower                                                         |
| aiohttp                  | 1.11 ms                                                                      | 1.15 ms: 1.03x slower                                                        |
| chameleon                | 7.43 ms                                                                      | 7.65 ms: 1.03x slower                                                        |
| deepcopy_memo            | 37.3 us                                                                      | 38.8 us: 1.04x slower                                                        |
| deepcopy                 | 385 us                                                                       | 401 us: 1.04x slower                                                         |
| typing_runtime_protocols | 119 us                                                                       | 124 us: 1.05x slower                                                         |
| regex_effbot             | 3.53 ms                                                                      | 3.71 ms: 1.05x slower                                                        |
| genshi_xml               | 57.1 ms                                                                      | 61.8 ms: 1.08x slower                                                        |
| genshi_text              | 25.7 ms                                                                      | 28.0 ms: 1.09x slower                                                        |
| deepcopy_reduce          | 3.39 us                                                                      | 3.72 us: 1.10x slower                                                        |
| Geometric mean           | (ref)                                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (32): chaos, pprint_safe_repr, hexiom, gunicorn, async_tree_none_tg, raytrace, pidigits, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, dulwich_log, thrift, async_tree_none, python_startup_no_site, dask, sympy_integrate, asyncio_websockets, pylint, pickle_list, sqlglot_parse, pickle, xml_etree_iterparse, sympy_sum, pycparser, async_tree_io_tg, bench_thread_pool, tornado_http, async_tree_memoization, async_tree_memoization_tg, pprint_pformat, mypy2, deltablue, bench_mp_pool

# HPT report

- Reliability score: 99.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x