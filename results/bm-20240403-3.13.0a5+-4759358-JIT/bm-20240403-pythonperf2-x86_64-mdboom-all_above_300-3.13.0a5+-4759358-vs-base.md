# Results vs. base

- fork: mdboom
- ref: all_above_300
- machine: linux-x86_64
- commit hash: 4759358
- commit date: 2024-04-03
- overall geometric mean: 1.00x slower
- HPT reliability: 97.02%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                       | 301 ms: 1.01x slower                                                  |
| chameleon      | 7.43 ms                                                                      | 7.23 ms: 1.03x faster                                                 |
| docutils       | 3.07 sec                                                                     | 3.05 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none | 377 ms                                                                       | 380 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 98.3 ms                                                                      | 95.4 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                      | 25.9 ms: 1.01x faster                                                 |
| regex_compile  | 148 ms                                                                       | 149 ms: 1.01x slower                                                  |
| regex_dna      | 244 ms                                                                       | 246 ms: 1.01x slower                                                  |
| regex_effbot   | 3.42 ms                                                                      | 3.50 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle             | 15.5 us                                                                      | 14.9 us: 1.04x faster                                                 |
| pickle_pure_python   | 316 us                                                                       | 308 us: 1.03x faster                                                  |
| json_loads           | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 104 ms                                                                       | 102 ms: 1.02x faster                                                  |
| xml_etree_parse      | 144 ms                                                                       | 142 ms: 1.01x faster                                                  |
| pickle_dict          | 33.0 us                                                                      | 32.7 us: 1.01x faster                                                 |
| xml_etree_process    | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                                 |
| xml_etree_generate   | 83.9 ms                                                                      | 84.3 ms: 1.00x slower                                                 |
| unpickle_list        | 4.62 us                                                                      | 4.71 us: 1.02x slower                                                 |
| tomli_loads          | 2.16 sec                                                                     | 2.21 sec: 1.02x slower                                                |
| unpickle_pure_python | 235 us                                                                       | 241 us: 1.02x slower                                                  |
| json_dumps           | 10.5 ms                                                                      | 10.8 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 41.2 ms                                                                      | 40.2 ms: 1.02x faster                                                 |
| mako            | 10.0 ms                                                                      | 9.92 ms: 1.01x faster                                                 |
| genshi_xml      | 59.1 ms                                                                      | 60.3 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|--------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle                 | 15.5 us                                                                      | 14.9 us: 1.04x faster                                                 |
| generators               | 34.6 ms                                                                      | 33.4 ms: 1.04x faster                                                 |
| nbody                    | 98.3 ms                                                                      | 95.4 ms: 1.03x faster                                                 |
| chameleon                | 7.43 ms                                                                      | 7.23 ms: 1.03x faster                                                 |
| pickle_pure_python       | 316 us                                                                       | 308 us: 1.03x faster                                                  |
| logging_format           | 7.33 us                                                                      | 7.15 us: 1.02x faster                                                 |
| django_template          | 41.2 ms                                                                      | 40.2 ms: 1.02x faster                                                 |
| deltablue                | 3.85 ms                                                                      | 3.76 ms: 1.02x faster                                                 |
| logging_simple           | 6.80 us                                                                      | 6.66 us: 1.02x faster                                                 |
| typing_runtime_protocols | 122 us                                                                       | 120 us: 1.02x faster                                                  |
| json_loads               | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                 |
| xml_etree_iterparse      | 104 ms                                                                       | 102 ms: 1.02x faster                                                  |
| dask                     | 408 ms                                                                       | 403 ms: 1.01x faster                                                  |
| sqlglot_normalize        | 125 ms                                                                       | 123 ms: 1.01x faster                                                  |
| xml_etree_parse          | 144 ms                                                                       | 142 ms: 1.01x faster                                                  |
| sqlglot_parse            | 1.45 ms                                                                      | 1.43 ms: 1.01x faster                                                 |
| pickle_dict              | 33.0 us                                                                      | 32.7 us: 1.01x faster                                                 |
| sqlglot_transpile        | 1.84 ms                                                                      | 1.83 ms: 1.01x faster                                                 |
| regex_v8                 | 26.1 ms                                                                      | 25.9 ms: 1.01x faster                                                 |
| xml_etree_process        | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                                 |
| mako                     | 10.0 ms                                                                      | 9.92 ms: 1.01x faster                                                 |
| json                     | 5.41 ms                                                                      | 5.36 ms: 1.01x faster                                                 |
| docutils                 | 3.07 sec                                                                     | 3.05 sec: 1.01x faster                                                |
| raytrace                 | 308 ms                                                                       | 306 ms: 1.01x faster                                                  |
| aiohttp                  | 1.12 ms                                                                      | 1.12 ms: 1.01x faster                                                 |
| dulwich_log              | 69.8 ms                                                                      | 69.4 ms: 1.01x faster                                                 |
| deepcopy_reduce          | 3.40 us                                                                      | 3.37 us: 1.01x faster                                                 |
| sqlite_synth             | 2.71 us                                                                      | 2.70 us: 1.01x faster                                                 |
| sqlglot_optimize         | 63.6 ms                                                                      | 63.2 ms: 1.01x faster                                                 |
| asyncio_tcp              | 372 ms                                                                       | 370 ms: 1.00x faster                                                  |
| gc_traversal             | 4.38 ms                                                                      | 4.37 ms: 1.00x faster                                                 |
| python_startup_no_site   | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                 |
| sympy_sum                | 163 ms                                                                       | 163 ms: 1.00x slower                                                  |
| xml_etree_generate       | 83.9 ms                                                                      | 84.3 ms: 1.00x slower                                                 |
| 2to3                     | 300 ms                                                                       | 301 ms: 1.01x slower                                                  |
| logging_silent           | 97.2 ns                                                                      | 97.7 ns: 1.01x slower                                                 |
| regex_compile            | 148 ms                                                                       | 149 ms: 1.01x slower                                                  |
| sympy_str                | 304 ms                                                                       | 305 ms: 1.01x slower                                                  |
| richards_super           | 58.0 ms                                                                      | 58.3 ms: 1.01x slower                                                 |
| create_gc_cycles         | 1.79 ms                                                                      | 1.80 ms: 1.01x slower                                                 |
| scimark_sor              | 154 ms                                                                       | 155 ms: 1.01x slower                                                  |
| telco                    | 7.97 ms                                                                      | 8.03 ms: 1.01x slower                                                 |
| async_tree_none          | 377 ms                                                                       | 380 ms: 1.01x slower                                                  |
| regex_dna                | 244 ms                                                                       | 246 ms: 1.01x slower                                                  |
| async_generators         | 390 ms                                                                       | 394 ms: 1.01x slower                                                  |
| pyflate                  | 519 ms                                                                       | 525 ms: 1.01x slower                                                  |
| thrift                   | 882 us                                                                       | 893 us: 1.01x slower                                                  |
| crypto_pyaes             | 77.5 ms                                                                      | 78.7 ms: 1.02x slower                                                 |
| pprint_pformat           | 1.72 sec                                                                     | 1.75 sec: 1.02x slower                                                |
| unpickle_list            | 4.62 us                                                                      | 4.71 us: 1.02x slower                                                 |
| pprint_safe_repr         | 841 ms                                                                       | 858 ms: 1.02x slower                                                  |
| genshi_xml               | 59.1 ms                                                                      | 60.3 ms: 1.02x slower                                                 |
| tomli_loads              | 2.16 sec                                                                     | 2.21 sec: 1.02x slower                                                |
| unpickle_pure_python     | 235 us                                                                       | 241 us: 1.02x slower                                                  |
| hexiom                   | 7.57 ms                                                                      | 7.75 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult  | 4.15 ms                                                                      | 4.25 ms: 1.02x slower                                                 |
| regex_effbot             | 3.42 ms                                                                      | 3.50 ms: 1.02x slower                                                 |
| scimark_fft              | 312 ms                                                                       | 320 ms: 1.03x slower                                                  |
| scimark_monte_carlo      | 72.9 ms                                                                      | 74.8 ms: 1.03x slower                                                 |
| json_dumps               | 10.5 ms                                                                      | 10.8 ms: 1.03x slower                                                 |
| meteor_contest           | 131 ms                                                                       | 135 ms: 1.03x slower                                                  |
| nqueens                  | 103 ms                                                                       | 107 ms: 1.04x slower                                                  |
| fannkuch                 | 379 ms                                                                       | 393 ms: 1.04x slower                                                  |
| spectral_norm            | 93.2 ms                                                                      | 96.8 ms: 1.04x slower                                                 |
| scimark_lu               | 120 ms                                                                       | 126 ms: 1.05x slower                                                  |
| coverage                 | 83.0 ms                                                                      | 88.1 ms: 1.06x slower                                                 |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (34): async_tree_cpu_io_mixed_tg, mypy2, genshi_text, gunicorn, pycparser, pickle, go, richards, sympy_integrate, mdp, python_startup, pathlib, pidigits, float, html5lib, async_tree_cpu_io_mixed, sympy_expand, asyncio_tcp_ssl, comprehensions, pickle_list, deepcopy_memo, async_tree_io, async_tree_memoization_tg, pylint, deepcopy, bench_thread_pool, coroutines, async_tree_memoization, asyncio_websockets, tornado_http, async_tree_none_tg, chaos, async_tree_io_tg, bench_mp_pool
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 97.02% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x