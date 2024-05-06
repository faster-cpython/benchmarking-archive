# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: darwin-arm64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.00x faster
- HPT reliability: 98.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 173 ms                                                                 | 171 ms: 1.01x faster                                              |
| html5lib       | 33.3 ms                                                                | 32.9 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (3): chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 467 ms                                                                 | 454 ms: 1.03x faster                                              |
| async_tree_eager           | 64.9 ms                                                                | 64.5 ms: 1.01x faster                                             |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (14): async_tree_none, async_tree_eager_io, async_tree_eager_memoization, async_tree_none_tg, async_tree_eager_io_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_io_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed, async_tree_eager_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 70.5 ms                                                                | 70.7 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 152 ms                                                                 | 152 ms: 1.00x slower                                              |
| regex_effbot   | 2.61 ms                                                                | 2.63 ms: 1.01x slower                                             |
| regex_compile  | 80.5 ms                                                                | 86.4 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 141 us                                                                 | 139 us: 1.01x faster                                              |
| json_dumps           | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                             |
| tomli_loads          | 1.29 sec                                                               | 1.28 sec: 1.01x faster                                            |
| unpickle_list        | 3.02 us                                                                | 3.00 us: 1.01x faster                                             |
| json_loads           | 16.9 us                                                                | 16.9 us: 1.00x faster                                             |
| xml_etree_process    | 37.0 ms                                                                | 37.3 ms: 1.01x slower                                             |
| pickle_dict          | 18.0 us                                                                | 18.2 us: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (7): xml_etree_parse, pickle_pure_python, unpickle, pickle_list, pickle, xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup | 13.4 ms                                                                | 13.3 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (3): genshi_text, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| richards                   | 31.7 ms                                                                | 29.7 ms: 1.07x faster                                             |
| richards_super             | 35.1 ms                                                                | 33.3 ms: 1.05x faster                                             |
| raytrace                   | 172 ms                                                                 | 163 ms: 1.05x faster                                              |
| async_tree_cpu_io_mixed_tg | 467 ms                                                                 | 454 ms: 1.03x faster                                              |
| pyflate                    | 324 ms                                                                 | 317 ms: 1.02x faster                                              |
| async_generators           | 302 ms                                                                 | 297 ms: 1.02x faster                                              |
| html5lib                   | 33.3 ms                                                                | 32.9 ms: 1.01x faster                                             |
| deepcopy                   | 214 us                                                                 | 211 us: 1.01x faster                                              |
| unpickle_pure_python       | 141 us                                                                 | 139 us: 1.01x faster                                              |
| json_dumps                 | 6.39 ms                                                                | 6.33 ms: 1.01x faster                                             |
| tomli_loads                | 1.29 sec                                                               | 1.28 sec: 1.01x faster                                            |
| comprehensions             | 12.0 us                                                                | 11.9 us: 1.01x faster                                             |
| 2to3                       | 173 ms                                                                 | 171 ms: 1.01x faster                                              |
| unpickle_list              | 3.02 us                                                                | 3.00 us: 1.01x faster                                             |
| deepcopy_memo              | 24.4 us                                                                | 24.2 us: 1.01x faster                                             |
| async_tree_eager           | 64.9 ms                                                                | 64.5 ms: 1.01x faster                                             |
| sympy_integrate            | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                             |
| pylint                     | 155 ms                                                                 | 154 ms: 1.01x faster                                              |
| python_startup             | 13.4 ms                                                                | 13.3 ms: 1.01x faster                                             |
| gc_traversal               | 2.46 ms                                                                | 2.45 ms: 1.01x faster                                             |
| crypto_pyaes               | 46.6 ms                                                                | 46.3 ms: 1.01x faster                                             |
| scimark_monte_carlo        | 43.2 ms                                                                | 43.0 ms: 1.00x faster                                             |
| chaos                      | 38.3 ms                                                                | 38.2 ms: 1.00x faster                                             |
| json_loads                 | 16.9 us                                                                | 16.9 us: 1.00x faster                                             |
| dulwich_log                | 29.1 ms                                                                | 29.0 ms: 1.00x faster                                             |
| asyncio_websockets         | 410 ms                                                                 | 408 ms: 1.00x faster                                              |
| create_gc_cycles           | 896 us                                                                 | 894 us: 1.00x faster                                              |
| sympy_expand               | 238 ms                                                                 | 237 ms: 1.00x faster                                              |
| scimark_sor                | 106 ms                                                                 | 106 ms: 1.00x faster                                              |
| sqlglot_normalize          | 176 ms                                                                 | 176 ms: 1.00x faster                                              |
| scimark_sparse_mat_mult    | 3.13 ms                                                                | 3.12 ms: 1.00x faster                                             |
| sqlglot_optimize           | 33.7 ms                                                                | 33.7 ms: 1.00x faster                                             |
| regex_dna                  | 152 ms                                                                 | 152 ms: 1.00x slower                                              |
| go                         | 106 ms                                                                 | 107 ms: 1.00x slower                                              |
| nbody                      | 70.5 ms                                                                | 70.7 ms: 1.00x slower                                             |
| sqlglot_parse              | 774 us                                                                 | 776 us: 1.00x slower                                              |
| mdp                        | 1.57 sec                                                               | 1.58 sec: 1.00x slower                                            |
| generators                 | 26.1 ms                                                                | 26.3 ms: 1.01x slower                                             |
| telco                      | 4.51 ms                                                                | 4.54 ms: 1.01x slower                                             |
| regex_effbot               | 2.61 ms                                                                | 2.63 ms: 1.01x slower                                             |
| logging_simple             | 3.13 us                                                                | 3.15 us: 1.01x slower                                             |
| xml_etree_process          | 37.0 ms                                                                | 37.3 ms: 1.01x slower                                             |
| pickle_dict                | 18.0 us                                                                | 18.2 us: 1.01x slower                                             |
| coverage                   | 45.9 ms                                                                | 46.3 ms: 1.01x slower                                             |
| logging_format             | 3.41 us                                                                | 3.44 us: 1.01x slower                                             |
| meteor_contest             | 73.5 ms                                                                | 74.2 ms: 1.01x slower                                             |
| thrift                     | 439 us                                                                 | 444 us: 1.01x slower                                              |
| fannkuch                   | 259 ms                                                                 | 263 ms: 1.01x slower                                              |
| pprint_safe_repr           | 493 ms                                                                 | 499 ms: 1.01x slower                                              |
| sympy_str                  | 142 ms                                                                 | 145 ms: 1.03x slower                                              |
| regex_compile              | 80.5 ms                                                                | 86.4 ms: 1.07x slower                                             |
| deltablue                  | 2.27 ms                                                                | 2.48 ms: 1.09x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (55): asyncio_tcp, mypy2, pathlib, sqlite_synth, async_tree_none, async_tree_eager_io, bench_mp_pool, xml_etree_parse, async_tree_eager_memoization, async_tree_none_tg, json, docutils, pickle_pure_python, async_tree_eager_io_tg, async_tree_io, async_tree_memoization, unpickle, pickle_list, bench_thread_pool, dask, coroutines, async_tree_memoization_tg, typing_runtime_protocols, async_tree_eager_memoization_tg, deepcopy_reduce, genshi_text, sympy_sum, pickle, python_startup_no_site, logging_silent, async_tree_io_tg, async_tree_eager_cpu_io_mixed_tg, hexiom, chameleon, regex_v8, asyncio_tcp_ssl, async_tree_eager_cpu_io_mixed, pidigits, scimark_fft, async_tree_eager_tg, spectral_norm, scimark_lu, pycparser, mako, genshi_xml, pprint_pformat, xml_etree_generate, nqueens, async_tree_cpu_io_mixed, float, sqlglot_transpile, xml_etree_iterparse, gunicorn, tornado_http, aiohttp

# HPT report

- Reliability score: 98.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x