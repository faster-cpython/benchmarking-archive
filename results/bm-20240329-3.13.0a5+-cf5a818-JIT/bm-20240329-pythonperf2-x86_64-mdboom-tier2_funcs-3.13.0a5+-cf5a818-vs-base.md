# Results vs. base

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: cf5a818
- commit date: 2024-03-29
- overall geometric mean: 1.01x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| chameleon      | 7.43 ms                                                                      | 7.54 ms: 1.02x slower                                               |
| docutils       | 3.07 sec                                                                     | 3.06 sec: 1.01x faster                                              |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                        |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 377 ms                                                                       | 358 ms: 1.05x faster                                                |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 578 ms: 1.03x faster                                                |
| async_tree_io              | 907 ms                                                                       | 886 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 594 ms: 1.01x faster                                                |
| async_tree_io_tg           | 880 ms                                                                       | 908 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 79.5 ms                                                                      | 76.7 ms: 1.04x faster                                               |
| nbody          | 98.3 ms                                                                      | 96.2 ms: 1.02x faster                                               |
| Geometric mean | (ref)                                                                        | 1.02x faster                                                        |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                      | 25.4 ms: 1.03x faster                                               |
| regex_dna      | 244 ms                                                                       | 241 ms: 1.01x faster                                                |
| regex_effbot   | 3.42 ms                                                                      | 3.61 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 33.0 us                                                                      | 30.7 us: 1.08x faster                                               |
| unpickle             | 15.5 us                                                                      | 15.1 us: 1.03x faster                                               |
| pickle               | 10.9 us                                                                      | 10.6 us: 1.02x faster                                               |
| json_loads           | 25.8 us                                                                      | 25.3 us: 1.02x faster                                               |
| unpickle_pure_python | 235 us                                                                       | 232 us: 1.01x faster                                                |
| xml_etree_iterparse  | 104 ms                                                                       | 103 ms: 1.01x faster                                                |
| xml_etree_parse      | 144 ms                                                                       | 143 ms: 1.01x faster                                                |
| pickle_pure_python   | 316 us                                                                       | 313 us: 1.01x faster                                                |
| xml_etree_process    | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                               |
| unpickle_list        | 4.62 us                                                                      | 4.65 us: 1.01x slower                                               |
| json_dumps           | 10.5 ms                                                                      | 10.6 ms: 1.01x slower                                               |
| xml_etree_generate   | 83.9 ms                                                                      | 84.7 ms: 1.01x slower                                               |
| tomli_loads          | 2.16 sec                                                                     | 2.19 sec: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                               |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|-----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 41.2 ms                                                                      | 40.0 ms: 1.03x faster                                               |
| mako            | 10.0 ms                                                                      | 9.97 ms: 1.00x faster                                               |
| genshi_xml      | 59.1 ms                                                                      | 59.6 ms: 1.01x slower                                               |
| genshi_text     | 26.8 ms                                                                      | 27.1 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                                        | 1.00x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict                | 33.0 us                                                                      | 30.7 us: 1.08x faster                                               |
| async_tree_none            | 377 ms                                                                       | 358 ms: 1.05x faster                                                |
| richards                   | 51.9 ms                                                                      | 50.0 ms: 1.04x faster                                               |
| raytrace                   | 308 ms                                                                       | 297 ms: 1.04x faster                                                |
| float                      | 79.5 ms                                                                      | 76.7 ms: 1.04x faster                                               |
| logging_simple             | 6.80 us                                                                      | 6.56 us: 1.04x faster                                               |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 578 ms: 1.03x faster                                                |
| django_template            | 41.2 ms                                                                      | 40.0 ms: 1.03x faster                                               |
| generators                 | 34.6 ms                                                                      | 33.6 ms: 1.03x faster                                               |
| unpickle                   | 15.5 us                                                                      | 15.1 us: 1.03x faster                                               |
| logging_format             | 7.33 us                                                                      | 7.14 us: 1.03x faster                                               |
| deltablue                  | 3.85 ms                                                                      | 3.74 ms: 1.03x faster                                               |
| regex_v8                   | 26.1 ms                                                                      | 25.4 ms: 1.03x faster                                               |
| sqlglot_parse              | 1.45 ms                                                                      | 1.41 ms: 1.03x faster                                               |
| async_tree_io              | 907 ms                                                                       | 886 ms: 1.02x faster                                                |
| gunicorn                   | 1.10 ms                                                                      | 1.08 ms: 1.02x faster                                               |
| pprint_safe_repr           | 841 ms                                                                       | 823 ms: 1.02x faster                                                |
| nbody                      | 98.3 ms                                                                      | 96.2 ms: 1.02x faster                                               |
| pickle                     | 10.9 us                                                                      | 10.6 us: 1.02x faster                                               |
| chaos                      | 67.5 ms                                                                      | 66.2 ms: 1.02x faster                                               |
| sqlglot_transpile          | 1.84 ms                                                                      | 1.81 ms: 1.02x faster                                               |
| json_loads                 | 25.8 us                                                                      | 25.3 us: 1.02x faster                                               |
| dulwich_log                | 69.8 ms                                                                      | 68.7 ms: 1.02x faster                                               |
| pprint_pformat             | 1.72 sec                                                                     | 1.70 sec: 1.02x faster                                              |
| sympy_sum                  | 163 ms                                                                       | 161 ms: 1.01x faster                                                |
| unpickle_pure_python       | 235 us                                                                       | 232 us: 1.01x faster                                                |
| sympy_integrate            | 25.3 ms                                                                      | 25.0 ms: 1.01x faster                                               |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 594 ms: 1.01x faster                                                |
| xml_etree_iterparse        | 104 ms                                                                       | 103 ms: 1.01x faster                                                |
| deepcopy_reduce            | 3.40 us                                                                      | 3.36 us: 1.01x faster                                               |
| regex_dna                  | 244 ms                                                                       | 241 ms: 1.01x faster                                                |
| xml_etree_parse            | 144 ms                                                                       | 143 ms: 1.01x faster                                                |
| pickle_pure_python         | 316 us                                                                       | 313 us: 1.01x faster                                                |
| async_generators           | 390 ms                                                                       | 387 ms: 1.01x faster                                                |
| sqlglot_optimize           | 63.6 ms                                                                      | 63.1 ms: 1.01x faster                                               |
| hexiom                     | 7.57 ms                                                                      | 7.52 ms: 1.01x faster                                               |
| xml_etree_process          | 58.5 ms                                                                      | 58.0 ms: 1.01x faster                                               |
| sympy_str                  | 304 ms                                                                       | 302 ms: 1.01x faster                                                |
| sympy_expand               | 512 ms                                                                       | 509 ms: 1.01x faster                                                |
| pathlib                    | 19.4 ms                                                                      | 19.3 ms: 1.01x faster                                               |
| pyflate                    | 519 ms                                                                       | 516 ms: 1.01x faster                                                |
| sqlite_synth               | 2.71 us                                                                      | 2.70 us: 1.01x faster                                               |
| docutils                   | 3.07 sec                                                                     | 3.06 sec: 1.01x faster                                              |
| mdp                        | 2.62 sec                                                                     | 2.61 sec: 1.01x faster                                              |
| deepcopy_memo              | 38.3 us                                                                      | 38.1 us: 1.00x faster                                               |
| go                         | 180 ms                                                                       | 179 ms: 1.00x faster                                                |
| mako                       | 10.0 ms                                                                      | 9.97 ms: 1.00x faster                                               |
| python_startup             | 13.5 ms                                                                      | 13.5 ms: 1.00x faster                                               |
| create_gc_cycles           | 1.79 ms                                                                      | 1.80 ms: 1.01x slower                                               |
| sqlglot_normalize          | 125 ms                                                                       | 126 ms: 1.01x slower                                                |
| unpickle_list              | 4.62 us                                                                      | 4.65 us: 1.01x slower                                               |
| meteor_contest             | 131 ms                                                                       | 132 ms: 1.01x slower                                                |
| json_dumps                 | 10.5 ms                                                                      | 10.6 ms: 1.01x slower                                               |
| scimark_monte_carlo        | 72.9 ms                                                                      | 73.5 ms: 1.01x slower                                               |
| genshi_xml                 | 59.1 ms                                                                      | 59.6 ms: 1.01x slower                                               |
| xml_etree_generate         | 83.9 ms                                                                      | 84.7 ms: 1.01x slower                                               |
| comprehensions             | 19.7 us                                                                      | 19.9 us: 1.01x slower                                               |
| spectral_norm              | 93.2 ms                                                                      | 94.0 ms: 1.01x slower                                               |
| scimark_fft                | 312 ms                                                                       | 315 ms: 1.01x slower                                                |
| genshi_text                | 26.8 ms                                                                      | 27.1 ms: 1.01x slower                                               |
| tomli_loads                | 2.16 sec                                                                     | 2.19 sec: 1.01x slower                                              |
| fannkuch                   | 379 ms                                                                       | 384 ms: 1.01x slower                                                |
| chameleon                  | 7.43 ms                                                                      | 7.54 ms: 1.02x slower                                               |
| unpack_sequence            | 58.5 ns                                                                      | 59.6 ns: 1.02x slower                                               |
| telco                      | 7.97 ms                                                                      | 8.15 ms: 1.02x slower                                               |
| async_tree_io_tg           | 880 ms                                                                       | 908 ms: 1.03x slower                                                |
| coverage                   | 83.0 ms                                                                      | 86.4 ms: 1.04x slower                                               |
| gc_traversal               | 4.38 ms                                                                      | 4.56 ms: 1.04x slower                                               |
| regex_effbot               | 3.42 ms                                                                      | 3.61 ms: 1.06x slower                                               |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (32): async_tree_memoization, bench_mp_pool, bench_thread_pool, dask, mypy2, tornado_http, pycparser, typing_runtime_protocols, richards_super, async_tree_none_tg, asyncio_websockets, pylint, pickle_list, logging_silent, crypto_pyaes, aiohttp, json, python_startup_no_site, scimark_lu, asyncio_tcp_ssl, 2to3, deepcopy, pidigits, scimark_sor, nqueens, regex_compile, html5lib, asyncio_tcp, thrift, scimark_sparse_mat_mult, coroutines, async_tree_memoization_tg

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x