# Results vs. base

- fork: mdboom
- ref: all_above_200
- machine: linux-x86_64
- commit hash: d42ae28
- commit date: 2024-04-03
- overall geometric mean: 1.00x slower
- HPT reliability: 57.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                       | 302 ms: 1.01x slower                                                  |
| chameleon      | 7.43 ms                                                                      | 7.31 ms: 1.02x faster                                                 |
| docutils       | 3.07 sec                                                                     | 3.06 sec: 1.00x faster                                                |
| html5lib       | 73.4 ms                                                                      | 72.5 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 98.3 ms                                                                      | 94.7 ms: 1.04x faster                                                 |
| float          | 79.5 ms                                                                      | 77.7 ms: 1.02x faster                                                 |
| pidigits       | 261 ms                                                                       | 264 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                        | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                      | 25.9 ms: 1.01x faster                                                 |
| regex_compile  | 148 ms                                                                       | 150 ms: 1.01x slower                                                  |
| regex_dna      | 244 ms                                                                       | 247 ms: 1.01x slower                                                  |
| regex_effbot   | 3.42 ms                                                                      | 3.50 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle             | 15.5 us                                                                      | 14.6 us: 1.06x faster                                                 |
| pickle_pure_python   | 316 us                                                                       | 310 us: 1.02x faster                                                  |
| unpickle_list        | 4.62 us                                                                      | 4.60 us: 1.00x faster                                                 |
| pickle_dict          | 33.0 us                                                                      | 33.1 us: 1.00x slower                                                 |
| xml_etree_process    | 58.5 ms                                                                      | 58.9 ms: 1.01x slower                                                 |
| xml_etree_parse      | 144 ms                                                                       | 146 ms: 1.01x slower                                                  |
| pickle_list          | 4.38 us                                                                      | 4.45 us: 1.01x slower                                                 |
| xml_etree_generate   | 83.9 ms                                                                      | 85.5 ms: 1.02x slower                                                 |
| json_dumps           | 10.5 ms                                                                      | 10.7 ms: 1.02x slower                                                 |
| tomli_loads          | 2.16 sec                                                                     | 2.21 sec: 1.02x slower                                                |
| unpickle_pure_python | 235 us                                                                       | 241 us: 1.02x slower                                                  |
| pickle               | 10.9 us                                                                      | 11.1 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 13.5 ms                                                                      | 13.6 ms: 1.00x slower                                                 |
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 41.2 ms                                                                      | 40.1 ms: 1.03x faster                                                 |
| mako            | 10.0 ms                                                                      | 9.84 ms: 1.02x faster                                                 |
| genshi_text     | 26.8 ms                                                                      | 27.7 ms: 1.03x slower                                                 |
| genshi_xml      | 59.1 ms                                                                      | 62.7 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                                        | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark               | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle                | 15.5 us                                                                      | 14.6 us: 1.06x faster                                                 |
| thrift                  | 882 us                                                                       | 845 us: 1.04x faster                                                  |
| nbody                   | 98.3 ms                                                                      | 94.7 ms: 1.04x faster                                                 |
| django_template         | 41.2 ms                                                                      | 40.1 ms: 1.03x faster                                                 |
| pyflate                 | 519 ms                                                                       | 506 ms: 1.03x faster                                                  |
| float                   | 79.5 ms                                                                      | 77.7 ms: 1.02x faster                                                 |
| sqlglot_parse           | 1.45 ms                                                                      | 1.42 ms: 1.02x faster                                                 |
| sqlglot_transpile       | 1.84 ms                                                                      | 1.81 ms: 1.02x faster                                                 |
| pickle_pure_python      | 316 us                                                                       | 310 us: 1.02x faster                                                  |
| deltablue               | 3.85 ms                                                                      | 3.77 ms: 1.02x faster                                                 |
| coverage                | 83.0 ms                                                                      | 81.6 ms: 1.02x faster                                                 |
| mako                    | 10.0 ms                                                                      | 9.84 ms: 1.02x faster                                                 |
| chameleon               | 7.43 ms                                                                      | 7.31 ms: 1.02x faster                                                 |
| pprint_safe_repr        | 841 ms                                                                       | 828 ms: 1.02x faster                                                  |
| richards                | 51.9 ms                                                                      | 51.2 ms: 1.01x faster                                                 |
| dask                    | 408 ms                                                                       | 403 ms: 1.01x faster                                                  |
| pprint_pformat          | 1.72 sec                                                                     | 1.70 sec: 1.01x faster                                                |
| html5lib                | 73.4 ms                                                                      | 72.5 ms: 1.01x faster                                                 |
| sqlglot_normalize       | 125 ms                                                                       | 123 ms: 1.01x faster                                                  |
| go                      | 180 ms                                                                       | 178 ms: 1.01x faster                                                  |
| logging_simple          | 6.80 us                                                                      | 6.73 us: 1.01x faster                                                 |
| aiohttp                 | 1.12 ms                                                                      | 1.11 ms: 1.01x faster                                                 |
| comprehensions          | 19.7 us                                                                      | 19.5 us: 1.01x faster                                                 |
| sqlglot_optimize        | 63.6 ms                                                                      | 62.9 ms: 1.01x faster                                                 |
| sympy_sum               | 163 ms                                                                       | 161 ms: 1.01x faster                                                  |
| scimark_sor             | 154 ms                                                                       | 153 ms: 1.01x faster                                                  |
| regex_v8                | 26.1 ms                                                                      | 25.9 ms: 1.01x faster                                                 |
| asyncio_tcp             | 372 ms                                                                       | 369 ms: 1.01x faster                                                  |
| sympy_integrate         | 25.3 ms                                                                      | 25.1 ms: 1.01x faster                                                 |
| generators              | 34.6 ms                                                                      | 34.4 ms: 1.01x faster                                                 |
| pathlib                 | 19.4 ms                                                                      | 19.3 ms: 1.00x faster                                                 |
| unpickle_list           | 4.62 us                                                                      | 4.60 us: 1.00x faster                                                 |
| docutils                | 3.07 sec                                                                     | 3.06 sec: 1.00x faster                                                |
| scimark_sparse_mat_mult | 4.15 ms                                                                      | 4.14 ms: 1.00x faster                                                 |
| pickle_dict             | 33.0 us                                                                      | 33.1 us: 1.00x slower                                                 |
| python_startup          | 13.5 ms                                                                      | 13.6 ms: 1.00x slower                                                 |
| crypto_pyaes            | 77.5 ms                                                                      | 77.9 ms: 1.00x slower                                                 |
| python_startup_no_site  | 11.8 ms                                                                      | 11.8 ms: 1.01x slower                                                 |
| mdp                     | 2.62 sec                                                                     | 2.63 sec: 1.01x slower                                                |
| scimark_fft             | 312 ms                                                                       | 314 ms: 1.01x slower                                                  |
| 2to3                    | 300 ms                                                                       | 302 ms: 1.01x slower                                                  |
| xml_etree_process       | 58.5 ms                                                                      | 58.9 ms: 1.01x slower                                                 |
| deepcopy                | 388 us                                                                       | 391 us: 1.01x slower                                                  |
| regex_compile           | 148 ms                                                                       | 150 ms: 1.01x slower                                                  |
| pidigits                | 261 ms                                                                       | 264 ms: 1.01x slower                                                  |
| scimark_monte_carlo     | 72.9 ms                                                                      | 73.7 ms: 1.01x slower                                                 |
| regex_dna               | 244 ms                                                                       | 247 ms: 1.01x slower                                                  |
| xml_etree_parse         | 144 ms                                                                       | 146 ms: 1.01x slower                                                  |
| pickle_list             | 4.38 us                                                                      | 4.45 us: 1.01x slower                                                 |
| create_gc_cycles        | 1.79 ms                                                                      | 1.81 ms: 1.02x slower                                                 |
| richards_super          | 58.0 ms                                                                      | 58.9 ms: 1.02x slower                                                 |
| hexiom                  | 7.57 ms                                                                      | 7.70 ms: 1.02x slower                                                 |
| xml_etree_generate      | 83.9 ms                                                                      | 85.5 ms: 1.02x slower                                                 |
| async_generators        | 390 ms                                                                       | 398 ms: 1.02x slower                                                  |
| nqueens                 | 103 ms                                                                       | 105 ms: 1.02x slower                                                  |
| json_dumps              | 10.5 ms                                                                      | 10.7 ms: 1.02x slower                                                 |
| tomli_loads             | 2.16 sec                                                                     | 2.21 sec: 1.02x slower                                                |
| unpickle_pure_python    | 235 us                                                                       | 241 us: 1.02x slower                                                  |
| pickle                  | 10.9 us                                                                      | 11.1 us: 1.02x slower                                                 |
| regex_effbot            | 3.42 ms                                                                      | 3.50 ms: 1.02x slower                                                 |
| meteor_contest          | 131 ms                                                                       | 134 ms: 1.03x slower                                                  |
| telco                   | 7.97 ms                                                                      | 8.19 ms: 1.03x slower                                                 |
| spectral_norm           | 93.2 ms                                                                      | 96.2 ms: 1.03x slower                                                 |
| deepcopy_memo           | 38.3 us                                                                      | 39.6 us: 1.03x slower                                                 |
| genshi_text             | 26.8 ms                                                                      | 27.7 ms: 1.03x slower                                                 |
| fannkuch                | 379 ms                                                                       | 396 ms: 1.05x slower                                                  |
| genshi_xml              | 59.1 ms                                                                      | 62.7 ms: 1.06x slower                                                 |
| gc_traversal            | 4.38 ms                                                                      | 4.85 ms: 1.11x slower                                                 |
| Geometric mean          | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (32): bench_mp_pool, mypy2, async_tree_none_tg, tornado_http, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, pycparser, sqlite_synth, bench_thread_pool, async_tree_memoization, logging_format, async_tree_io, sympy_expand, async_tree_io_tg, pylint, gunicorn, scimark_lu, asyncio_tcp_ssl, asyncio_websockets, sympy_str, coroutines, json_loads, async_tree_none, dulwich_log, logging_silent, xml_etree_iterparse, deepcopy_reduce, raytrace, json, chaos, async_tree_cpu_io_mixed, typing_runtime_protocols
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 57.36% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x