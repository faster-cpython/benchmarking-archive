# Results vs. base

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: 27267d7
- commit date: 2024-04-03
- overall geometric mean: 1.00x faster
- HPT reliability: 91.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                       | 300 ms: 1.00x slower                                                |
| html5lib       | 73.4 ms                                                                      | 73.8 ms: 1.01x slower                                               |
| tornado_http   | 124 ms                                                                       | 123 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 377 ms                                                                       | 361 ms: 1.05x faster                                                |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 579 ms: 1.03x faster                                                |
| async_tree_io              | 907 ms                                                                       | 889 ms: 1.02x faster                                                |
| async_tree_io_tg           | 880 ms                                                                       | 904 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 79.5 ms                                                                      | 77.6 ms: 1.02x faster                                               |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 244 ms                                                                       | 241 ms: 1.01x faster                                                |
| regex_compile  | 148 ms                                                                       | 150 ms: 1.01x slower                                                |
| regex_effbot   | 3.42 ms                                                                      | 3.57 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 33.0 us                                                                      | 31.0 us: 1.07x faster                                               |
| pickle_pure_python   | 316 us                                                                       | 306 us: 1.03x faster                                                |
| pickle               | 10.9 us                                                                      | 10.5 us: 1.03x faster                                               |
| unpickle             | 15.5 us                                                                      | 15.1 us: 1.03x faster                                               |
| json_loads           | 25.8 us                                                                      | 25.2 us: 1.02x faster                                               |
| unpickle_list        | 4.62 us                                                                      | 4.55 us: 1.02x faster                                               |
| tomli_loads          | 2.16 sec                                                                     | 2.15 sec: 1.01x faster                                              |
| xml_etree_process    | 58.5 ms                                                                      | 58.2 ms: 1.00x faster                                               |
| xml_etree_iterparse  | 104 ms                                                                       | 104 ms: 1.01x slower                                                |
| xml_etree_generate   | 83.9 ms                                                                      | 85.2 ms: 1.01x slower                                               |
| xml_etree_parse      | 144 ms                                                                       | 146 ms: 1.01x slower                                                |
| pickle_list          | 4.38 us                                                                      | 4.46 us: 1.02x slower                                               |
| unpickle_pure_python | 235 us                                                                       | 240 us: 1.02x slower                                                |
| json_dumps           | 10.5 ms                                                                      | 10.7 ms: 1.02x slower                                               |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                               |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                        |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-----------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 41.2 ms                                                                      | 40.1 ms: 1.03x faster                                               |
| mako            | 10.0 ms                                                                      | 10.1 ms: 1.01x slower                                               |
| genshi_text     | 26.8 ms                                                                      | 27.2 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict                | 33.0 us                                                                      | 31.0 us: 1.07x faster                                               |
| async_tree_none            | 377 ms                                                                       | 361 ms: 1.05x faster                                                |
| generators                 | 34.6 ms                                                                      | 33.3 ms: 1.04x faster                                               |
| go                         | 180 ms                                                                       | 174 ms: 1.04x faster                                                |
| sqlglot_parse              | 1.45 ms                                                                      | 1.40 ms: 1.03x faster                                               |
| pyflate                    | 519 ms                                                                       | 502 ms: 1.03x faster                                                |
| deltablue                  | 3.85 ms                                                                      | 3.73 ms: 1.03x faster                                               |
| pickle_pure_python         | 316 us                                                                       | 306 us: 1.03x faster                                                |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 579 ms: 1.03x faster                                                |
| pickle                     | 10.9 us                                                                      | 10.5 us: 1.03x faster                                               |
| django_template            | 41.2 ms                                                                      | 40.1 ms: 1.03x faster                                               |
| unpickle                   | 15.5 us                                                                      | 15.1 us: 1.03x faster                                               |
| sqlglot_transpile          | 1.84 ms                                                                      | 1.80 ms: 1.03x faster                                               |
| float                      | 79.5 ms                                                                      | 77.6 ms: 1.02x faster                                               |
| json_loads                 | 25.8 us                                                                      | 25.2 us: 1.02x faster                                               |
| pycparser                  | 1.29 sec                                                                     | 1.26 sec: 1.02x faster                                              |
| raytrace                   | 308 ms                                                                       | 302 ms: 1.02x faster                                                |
| async_tree_io              | 907 ms                                                                       | 889 ms: 1.02x faster                                                |
| sqlglot_normalize          | 125 ms                                                                       | 123 ms: 1.02x faster                                                |
| pprint_safe_repr           | 841 ms                                                                       | 827 ms: 1.02x faster                                                |
| unpickle_list              | 4.62 us                                                                      | 4.55 us: 1.02x faster                                               |
| sqlglot_optimize           | 63.6 ms                                                                      | 62.6 ms: 1.01x faster                                               |
| dask                       | 408 ms                                                                       | 403 ms: 1.01x faster                                                |
| chaos                      | 67.5 ms                                                                      | 66.8 ms: 1.01x faster                                               |
| sqlite_synth               | 2.71 us                                                                      | 2.69 us: 1.01x faster                                               |
| tornado_http               | 124 ms                                                                       | 123 ms: 1.01x faster                                                |
| regex_dna                  | 244 ms                                                                       | 241 ms: 1.01x faster                                                |
| dulwich_log                | 69.8 ms                                                                      | 69.2 ms: 1.01x faster                                               |
| deepcopy_reduce            | 3.40 us                                                                      | 3.37 us: 1.01x faster                                               |
| tomli_loads                | 2.16 sec                                                                     | 2.15 sec: 1.01x faster                                              |
| sympy_expand               | 512 ms                                                                       | 510 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult    | 4.15 ms                                                                      | 4.13 ms: 1.00x faster                                               |
| xml_etree_process          | 58.5 ms                                                                      | 58.2 ms: 1.00x faster                                               |
| sympy_str                  | 304 ms                                                                       | 302 ms: 1.00x faster                                                |
| asyncio_tcp_ssl            | 1.58 sec                                                                     | 1.58 sec: 1.00x slower                                              |
| 2to3                       | 300 ms                                                                       | 300 ms: 1.00x slower                                                |
| python_startup             | 13.5 ms                                                                      | 13.5 ms: 1.00x slower                                               |
| deepcopy_memo              | 38.3 us                                                                      | 38.5 us: 1.00x slower                                               |
| html5lib                   | 73.4 ms                                                                      | 73.8 ms: 1.01x slower                                               |
| crypto_pyaes               | 77.5 ms                                                                      | 77.9 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 104 ms                                                                       | 104 ms: 1.01x slower                                                |
| scimark_sor                | 154 ms                                                                       | 155 ms: 1.01x slower                                                |
| thrift                     | 882 us                                                                       | 887 us: 1.01x slower                                                |
| mako                       | 10.0 ms                                                                      | 10.1 ms: 1.01x slower                                               |
| coverage                   | 83.0 ms                                                                      | 83.6 ms: 1.01x slower                                               |
| regex_compile              | 148 ms                                                                       | 150 ms: 1.01x slower                                                |
| comprehensions             | 19.7 us                                                                      | 20.0 us: 1.01x slower                                               |
| nqueens                    | 103 ms                                                                       | 104 ms: 1.01x slower                                                |
| meteor_contest             | 131 ms                                                                       | 132 ms: 1.01x slower                                                |
| scimark_fft                | 312 ms                                                                       | 316 ms: 1.01x slower                                                |
| xml_etree_generate         | 83.9 ms                                                                      | 85.2 ms: 1.01x slower                                               |
| xml_etree_parse            | 144 ms                                                                       | 146 ms: 1.01x slower                                                |
| genshi_text                | 26.8 ms                                                                      | 27.2 ms: 1.01x slower                                               |
| pathlib                    | 19.4 ms                                                                      | 19.8 ms: 1.02x slower                                               |
| pickle_list                | 4.38 us                                                                      | 4.46 us: 1.02x slower                                               |
| unpickle_pure_python       | 235 us                                                                       | 240 us: 1.02x slower                                                |
| richards                   | 51.9 ms                                                                      | 52.9 ms: 1.02x slower                                               |
| coroutines                 | 22.5 ms                                                                      | 22.9 ms: 1.02x slower                                               |
| scimark_monte_carlo        | 72.9 ms                                                                      | 74.4 ms: 1.02x slower                                               |
| create_gc_cycles           | 1.79 ms                                                                      | 1.82 ms: 1.02x slower                                               |
| json_dumps                 | 10.5 ms                                                                      | 10.7 ms: 1.02x slower                                               |
| richards_super             | 58.0 ms                                                                      | 59.4 ms: 1.03x slower                                               |
| telco                      | 7.97 ms                                                                      | 8.18 ms: 1.03x slower                                               |
| spectral_norm              | 93.2 ms                                                                      | 95.7 ms: 1.03x slower                                               |
| async_tree_io_tg           | 880 ms                                                                       | 904 ms: 1.03x slower                                                |
| scimark_lu                 | 120 ms                                                                       | 125 ms: 1.04x slower                                                |
| regex_effbot               | 3.42 ms                                                                      | 3.57 ms: 1.04x slower                                               |
| gc_traversal               | 4.38 ms                                                                      | 4.80 ms: 1.10x slower                                               |
| Geometric mean             | (ref)                                                                        | 1.00x faster                                                        |

Benchmark hidden because not significant (32): async_tree_memoization, bench_mp_pool, mypy2, gunicorn, genshi_xml, json, typing_runtime_protocols, async_tree_cpu_io_mixed, bench_thread_pool, deepcopy, fannkuch, sympy_sum, docutils, asyncio_tcp, mdp, hexiom, pidigits, sympy_integrate, logging_silent, async_tree_none_tg, regex_v8, python_startup_no_site, nbody, chameleon, async_generators, aiohttp, logging_simple, pylint, asyncio_websockets, pprint_pformat, logging_format, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 91.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x