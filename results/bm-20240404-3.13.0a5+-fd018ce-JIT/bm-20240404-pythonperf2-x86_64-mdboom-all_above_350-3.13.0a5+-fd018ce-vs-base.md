# Results vs. base

- fork: mdboom
- ref: all_above_350
- machine: linux-x86_64
- commit hash: fd018ce
- commit date: 2024-04-04
- overall geometric mean: 1.00x faster
- HPT reliability: 91.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                       | 302 ms: 1.01x slower                                                  |
| chameleon      | 7.43 ms                                                                      | 7.34 ms: 1.01x faster                                                 |
| html5lib       | 73.4 ms                                                                      | 72.8 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 377 ms                                                                       | 359 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 578 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 880 ms                                                                       | 910 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 98.3 ms                                                                      | 94.6 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 244 ms                                                                       | 242 ms: 1.01x faster                                                  |
| regex_compile  | 148 ms                                                                       | 150 ms: 1.01x slower                                                  |
| regex_effbot   | 3.42 ms                                                                      | 3.63 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 33.0 us                                                                      | 31.0 us: 1.06x faster                                                 |
| pickle               | 10.9 us                                                                      | 10.5 us: 1.04x faster                                                 |
| unpickle             | 15.5 us                                                                      | 15.0 us: 1.03x faster                                                 |
| pickle_pure_python   | 316 us                                                                       | 307 us: 1.03x faster                                                  |
| json_loads           | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                 |
| xml_etree_parse      | 144 ms                                                                       | 142 ms: 1.02x faster                                                  |
| xml_etree_iterparse  | 104 ms                                                                       | 103 ms: 1.01x faster                                                  |
| xml_etree_generate   | 83.9 ms                                                                      | 83.6 ms: 1.00x faster                                                 |
| pickle_list          | 4.38 us                                                                      | 4.45 us: 1.02x slower                                                 |
| unpickle_list        | 4.62 us                                                                      | 4.71 us: 1.02x slower                                                 |
| unpickle_pure_python | 235 us                                                                       | 243 us: 1.03x slower                                                  |
| json_dumps           | 10.5 ms                                                                      | 10.9 ms: 1.03x slower                                                 |
| tomli_loads          | 2.16 sec                                                                     | 2.24 sec: 1.04x slower                                                |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 59.1 ms                                                                      | 58.1 ms: 1.02x faster                                                 |
| mako           | 10.0 ms                                                                      | 9.87 ms: 1.01x faster                                                 |
| genshi_text    | 26.8 ms                                                                      | 27.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict                | 33.0 us                                                                      | 31.0 us: 1.06x faster                                                 |
| async_tree_none            | 377 ms                                                                       | 359 ms: 1.05x faster                                                  |
| nbody                      | 98.3 ms                                                                      | 94.6 ms: 1.04x faster                                                 |
| pickle                     | 10.9 us                                                                      | 10.5 us: 1.04x faster                                                 |
| coverage                   | 83.0 ms                                                                      | 80.3 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 596 ms                                                                       | 578 ms: 1.03x faster                                                  |
| unpickle                   | 15.5 us                                                                      | 15.0 us: 1.03x faster                                                 |
| generators                 | 34.6 ms                                                                      | 33.6 ms: 1.03x faster                                                 |
| pickle_pure_python         | 316 us                                                                       | 307 us: 1.03x faster                                                  |
| logging_simple             | 6.80 us                                                                      | 6.62 us: 1.03x faster                                                 |
| logging_format             | 7.33 us                                                                      | 7.15 us: 1.03x faster                                                 |
| pyflate                    | 519 ms                                                                       | 507 ms: 1.02x faster                                                  |
| coroutines                 | 22.5 ms                                                                      | 22.1 ms: 1.02x faster                                                 |
| json_loads                 | 25.8 us                                                                      | 25.3 us: 1.02x faster                                                 |
| genshi_xml                 | 59.1 ms                                                                      | 58.1 ms: 1.02x faster                                                 |
| pycparser                  | 1.29 sec                                                                     | 1.27 sec: 1.02x faster                                                |
| typing_runtime_protocols   | 122 us                                                                       | 120 us: 1.02x faster                                                  |
| xml_etree_parse            | 144 ms                                                                       | 142 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.84 ms                                                                      | 1.82 ms: 1.02x faster                                                 |
| sqlglot_parse              | 1.45 ms                                                                      | 1.43 ms: 1.02x faster                                                 |
| dask                       | 408 ms                                                                       | 402 ms: 1.02x faster                                                  |
| mako                       | 10.0 ms                                                                      | 9.87 ms: 1.01x faster                                                 |
| deltablue                  | 3.85 ms                                                                      | 3.79 ms: 1.01x faster                                                 |
| go                         | 180 ms                                                                       | 178 ms: 1.01x faster                                                  |
| json                       | 5.41 ms                                                                      | 5.34 ms: 1.01x faster                                                 |
| gunicorn                   | 1.10 ms                                                                      | 1.09 ms: 1.01x faster                                                 |
| chameleon                  | 7.43 ms                                                                      | 7.34 ms: 1.01x faster                                                 |
| deepcopy_reduce            | 3.40 us                                                                      | 3.36 us: 1.01x faster                                                 |
| html5lib                   | 73.4 ms                                                                      | 72.8 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 104 ms                                                                       | 103 ms: 1.01x faster                                                  |
| regex_dna                  | 244 ms                                                                       | 242 ms: 1.01x faster                                                  |
| chaos                      | 67.5 ms                                                                      | 67.0 ms: 1.01x faster                                                 |
| aiohttp                    | 1.12 ms                                                                      | 1.11 ms: 1.01x faster                                                 |
| deepcopy_memo              | 38.3 us                                                                      | 38.1 us: 1.01x faster                                                 |
| gc_traversal               | 4.38 ms                                                                      | 4.36 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.15 ms                                                                      | 4.13 ms: 1.01x faster                                                 |
| xml_etree_generate         | 83.9 ms                                                                      | 83.6 ms: 1.00x faster                                                 |
| dulwich_log                | 69.8 ms                                                                      | 69.6 ms: 1.00x faster                                                 |
| python_startup_no_site     | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                 |
| asyncio_tcp_ssl            | 1.58 sec                                                                     | 1.58 sec: 1.00x slower                                                |
| sympy_expand               | 512 ms                                                                       | 515 ms: 1.00x slower                                                  |
| pathlib                    | 19.4 ms                                                                      | 19.5 ms: 1.00x slower                                                 |
| create_gc_cycles           | 1.79 ms                                                                      | 1.79 ms: 1.01x slower                                                 |
| sqlglot_optimize           | 63.6 ms                                                                      | 63.9 ms: 1.01x slower                                                 |
| 2to3                       | 300 ms                                                                       | 302 ms: 1.01x slower                                                  |
| richards                   | 51.9 ms                                                                      | 52.4 ms: 1.01x slower                                                 |
| regex_compile              | 148 ms                                                                       | 150 ms: 1.01x slower                                                  |
| mdp                        | 2.62 sec                                                                     | 2.66 sec: 1.02x slower                                                |
| crypto_pyaes               | 77.5 ms                                                                      | 78.7 ms: 1.02x slower                                                 |
| pickle_list                | 4.38 us                                                                      | 4.45 us: 1.02x slower                                                 |
| telco                      | 7.97 ms                                                                      | 8.10 ms: 1.02x slower                                                 |
| richards_super             | 58.0 ms                                                                      | 58.9 ms: 1.02x slower                                                 |
| genshi_text                | 26.8 ms                                                                      | 27.3 ms: 1.02x slower                                                 |
| unpickle_list              | 4.62 us                                                                      | 4.71 us: 1.02x slower                                                 |
| hexiom                     | 7.57 ms                                                                      | 7.74 ms: 1.02x slower                                                 |
| spectral_norm              | 93.2 ms                                                                      | 95.4 ms: 1.02x slower                                                 |
| scimark_monte_carlo        | 72.9 ms                                                                      | 74.8 ms: 1.03x slower                                                 |
| scimark_fft                | 312 ms                                                                       | 321 ms: 1.03x slower                                                  |
| unpickle_pure_python       | 235 us                                                                       | 243 us: 1.03x slower                                                  |
| nqueens                    | 103 ms                                                                       | 106 ms: 1.03x slower                                                  |
| json_dumps                 | 10.5 ms                                                                      | 10.9 ms: 1.03x slower                                                 |
| fannkuch                   | 379 ms                                                                       | 392 ms: 1.03x slower                                                  |
| async_tree_io_tg           | 880 ms                                                                       | 910 ms: 1.03x slower                                                  |
| meteor_contest             | 131 ms                                                                       | 135 ms: 1.04x slower                                                  |
| tomli_loads                | 2.16 sec                                                                     | 2.24 sec: 1.04x slower                                                |
| scimark_lu                 | 120 ms                                                                       | 125 ms: 1.04x slower                                                  |
| regex_effbot               | 3.42 ms                                                                      | 3.63 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (33): async_tree_memoization, async_tree_io, bench_thread_pool, async_tree_none_tg, django_template, asyncio_websockets, async_tree_cpu_io_mixed, bench_mp_pool, thrift, deepcopy, xml_etree_process, comprehensions, mypy2, sympy_sum, tornado_http, pprint_pformat, sqlglot_normalize, sympy_integrate, raytrace, python_startup, docutils, pidigits, float, regex_v8, async_generators, pylint, sympy_str, asyncio_tcp, sqlite_synth, pprint_safe_repr, logging_silent, async_tree_memoization_tg, scimark_sor
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 91.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x