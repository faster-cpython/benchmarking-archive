# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                       | 302 ms: 1.01x slower                                                           |
| chameleon      | 7.72 ms                                                                      | 7.46 ms: 1.04x faster                                                          |
| docutils       | 3.07 sec                                                                     | 3.12 sec: 1.01x slower                                                         |
| html5lib       | 75.4 ms                                                                      | 74.9 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                   |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io      | 846 ms                                                                       | 854 ms: 1.01x slower                                                           |
| async_tree_none_tg | 332 ms                                                                       | 338 ms: 1.02x slower                                                           |
| Geometric mean     | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 261 ms                                                                       | 261 ms: 1.00x slower                                                           |
| float          | 75.3 ms                                                                      | 75.9 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                                      | 3.50 ms: 1.03x faster                                                          |
| regex_compile  | 147 ms                                                                       | 145 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                                   |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 313 us                                                                       | 307 us: 1.02x faster                                                           |
| xml_etree_iterparse  | 103 ms                                                                       | 102 ms: 1.01x faster                                                           |
| xml_etree_parse      | 148 ms                                                                       | 147 ms: 1.01x faster                                                           |
| xml_etree_process    | 58.9 ms                                                                      | 59.2 ms: 1.00x slower                                                          |
| json_loads           | 25.2 us                                                                      | 25.3 us: 1.00x slower                                                          |
| unpickle_pure_python | 225 us                                                                       | 227 us: 1.01x slower                                                           |
| xml_etree_generate   | 84.7 ms                                                                      | 85.8 ms: 1.01x slower                                                          |
| pickle               | 10.4 us                                                                      | 10.7 us: 1.04x slower                                                          |
| pickle_dict          | 30.6 us                                                                      | 33.7 us: 1.10x slower                                                          |
| Geometric mean       | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (5): pickle_list, json_dumps, tomli_loads, unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                          |
| python_startup         | 13.4 ms                                                                      | 13.5 ms: 1.01x slower                                                          |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako           | 10.0 ms                                                                      | 9.98 ms: 1.00x faster                                                          |
| genshi_text    | 26.7 ms                                                                      | 27.2 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                   |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 128 us                                                                       | 121 us: 1.06x faster                                                           |
| deepcopy_memo            | 38.8 us                                                                      | 37.0 us: 1.05x faster                                                          |
| chameleon                | 7.72 ms                                                                      | 7.46 ms: 1.04x faster                                                          |
| scimark_lu               | 119 ms                                                                       | 115 ms: 1.03x faster                                                           |
| regex_effbot             | 3.61 ms                                                                      | 3.50 ms: 1.03x faster                                                          |
| pyflate                  | 501 ms                                                                       | 486 ms: 1.03x faster                                                           |
| deepcopy                 | 398 us                                                                       | 390 us: 1.02x faster                                                           |
| pickle_pure_python       | 313 us                                                                       | 307 us: 1.02x faster                                                           |
| deepcopy_reduce          | 3.51 us                                                                      | 3.45 us: 1.02x faster                                                          |
| fannkuch                 | 388 ms                                                                       | 381 ms: 1.02x faster                                                           |
| regex_compile            | 147 ms                                                                       | 145 ms: 1.02x faster                                                           |
| generators               | 33.4 ms                                                                      | 33.0 ms: 1.01x faster                                                          |
| xml_etree_iterparse      | 103 ms                                                                       | 102 ms: 1.01x faster                                                           |
| pycparser                | 1.25 sec                                                                     | 1.24 sec: 1.01x faster                                                         |
| nqueens                  | 102 ms                                                                       | 101 ms: 1.01x faster                                                           |
| scimark_sor              | 151 ms                                                                       | 150 ms: 1.01x faster                                                           |
| xml_etree_parse          | 148 ms                                                                       | 147 ms: 1.01x faster                                                           |
| html5lib                 | 75.4 ms                                                                      | 74.9 ms: 1.01x faster                                                          |
| sqlglot_parse            | 1.42 ms                                                                      | 1.41 ms: 1.01x faster                                                          |
| spectral_norm            | 93.2 ms                                                                      | 92.8 ms: 1.00x faster                                                          |
| mako                     | 10.0 ms                                                                      | 9.98 ms: 1.00x faster                                                          |
| sqlglot_transpile        | 1.82 ms                                                                      | 1.81 ms: 1.00x faster                                                          |
| sqlite_synth             | 2.69 us                                                                      | 2.68 us: 1.00x faster                                                          |
| pidigits                 | 261 ms                                                                       | 261 ms: 1.00x slower                                                           |
| python_startup_no_site   | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                          |
| create_gc_cycles         | 1.86 ms                                                                      | 1.87 ms: 1.00x slower                                                          |
| xml_etree_process        | 58.9 ms                                                                      | 59.2 ms: 1.00x slower                                                          |
| crypto_pyaes             | 77.2 ms                                                                      | 77.6 ms: 1.00x slower                                                          |
| json_loads               | 25.2 us                                                                      | 25.3 us: 1.00x slower                                                          |
| coroutines               | 22.1 ms                                                                      | 22.2 ms: 1.01x slower                                                          |
| python_startup           | 13.4 ms                                                                      | 13.5 ms: 1.01x slower                                                          |
| dulwich_log              | 67.8 ms                                                                      | 68.2 ms: 1.01x slower                                                          |
| float                    | 75.3 ms                                                                      | 75.9 ms: 1.01x slower                                                          |
| unpickle_pure_python     | 225 us                                                                       | 227 us: 1.01x slower                                                           |
| pprint_safe_repr         | 834 ms                                                                       | 841 ms: 1.01x slower                                                           |
| scimark_sparse_mat_mult  | 4.14 ms                                                                      | 4.18 ms: 1.01x slower                                                          |
| async_tree_io            | 846 ms                                                                       | 854 ms: 1.01x slower                                                           |
| logging_silent           | 97.2 ns                                                                      | 98.2 ns: 1.01x slower                                                          |
| telco                    | 8.22 ms                                                                      | 8.32 ms: 1.01x slower                                                          |
| xml_etree_generate       | 84.7 ms                                                                      | 85.8 ms: 1.01x slower                                                          |
| raytrace                 | 272 ms                                                                       | 275 ms: 1.01x slower                                                           |
| 2to3                     | 298 ms                                                                       | 302 ms: 1.01x slower                                                           |
| thrift                   | 885 us                                                                       | 897 us: 1.01x slower                                                           |
| docutils                 | 3.07 sec                                                                     | 3.12 sec: 1.01x slower                                                         |
| sqlglot_normalize        | 125 ms                                                                       | 126 ms: 1.01x slower                                                           |
| gunicorn                 | 1.10 ms                                                                      | 1.11 ms: 1.01x slower                                                          |
| logging_simple           | 6.34 us                                                                      | 6.43 us: 1.01x slower                                                          |
| dask                     | 400 ms                                                                       | 407 ms: 1.02x slower                                                           |
| async_tree_none_tg       | 332 ms                                                                       | 338 ms: 1.02x slower                                                           |
| logging_format           | 7.00 us                                                                      | 7.12 us: 1.02x slower                                                          |
| gc_traversal             | 4.58 ms                                                                      | 4.66 ms: 1.02x slower                                                          |
| meteor_contest           | 133 ms                                                                       | 136 ms: 1.02x slower                                                           |
| sympy_sum                | 163 ms                                                                       | 165 ms: 1.02x slower                                                           |
| genshi_text              | 26.7 ms                                                                      | 27.2 ms: 1.02x slower                                                          |
| hexiom                   | 7.15 ms                                                                      | 7.30 ms: 1.02x slower                                                          |
| aiohttp                  | 1.12 ms                                                                      | 1.14 ms: 1.02x slower                                                          |
| pathlib                  | 19.3 ms                                                                      | 19.7 ms: 1.02x slower                                                          |
| sympy_str                | 305 ms                                                                       | 311 ms: 1.02x slower                                                           |
| sympy_integrate          | 25.2 ms                                                                      | 25.7 ms: 1.02x slower                                                          |
| pylint                   | 334 ms                                                                       | 341 ms: 1.02x slower                                                           |
| json                     | 5.30 ms                                                                      | 5.41 ms: 1.02x slower                                                          |
| sqlglot_optimize         | 63.1 ms                                                                      | 64.5 ms: 1.02x slower                                                          |
| chaos                    | 64.6 ms                                                                      | 66.1 ms: 1.02x slower                                                          |
| mdp                      | 2.57 sec                                                                     | 2.63 sec: 1.03x slower                                                         |
| scimark_fft              | 314 ms                                                                       | 322 ms: 1.03x slower                                                           |
| scimark_monte_carlo      | 70.2 ms                                                                      | 72.1 ms: 1.03x slower                                                          |
| comprehensions           | 19.1 us                                                                      | 19.7 us: 1.03x slower                                                          |
| sympy_expand             | 507 ms                                                                       | 522 ms: 1.03x slower                                                           |
| pickle                   | 10.4 us                                                                      | 10.7 us: 1.04x slower                                                          |
| mypy2                    | 819 ms                                                                       | 849 ms: 1.04x slower                                                           |
| coverage                 | 81.6 ms                                                                      | 86.4 ms: 1.06x slower                                                          |
| pickle_dict              | 30.6 us                                                                      | 33.7 us: 1.10x slower                                                          |
| Geometric mean           | (ref)                                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (27): richards, pickle_list, asyncio_websockets, json_dumps, asyncio_tcp, genshi_xml, tomli_loads, unpickle_list, async_generators, asyncio_tcp_ssl, richards_super, regex_v8, go, regex_dna, unpickle, tornado_http, bench_thread_pool, pprint_pformat, deltablue, bench_mp_pool, nbody, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x