# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.02x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 320 ms                                                                       | 316 ms: 1.01x faster                                                    |
| chameleon      | 8.00 ms                                                                      | 7.77 ms: 1.03x faster                                                   |
| docutils       | 3.29 sec                                                                     | 3.24 sec: 1.02x faster                                                  |
| html5lib       | 79.1 ms                                                                      | 79.7 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|---------------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg        | 346 ms                                                                       | 354 ms: 1.02x slower                                                    |
| async_tree_memoization_tg | 436 ms                                                                       | 447 ms: 1.02x slower                                                    |
| Geometric mean            | (ref)                                                                        | 1.01x slower                                                            |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 130 ms                                                                       | 114 ms: 1.14x faster                                                    |
| float          | 101 ms                                                                       | 91.6 ms: 1.10x faster                                                   |
| pidigits       | 265 ms                                                                       | 266 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                        | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 208 ms                                                                       | 196 ms: 1.06x faster                                                    |
| regex_v8       | 26.6 ms                                                                      | 25.6 ms: 1.04x faster                                                   |
| regex_dna      | 239 ms                                                                       | 236 ms: 1.01x faster                                                    |
| regex_effbot   | 3.54 ms                                                                      | 3.58 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                        | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 310 us                                                                       | 293 us: 1.06x faster                                                    |
| tomli_loads          | 2.89 sec                                                                     | 2.74 sec: 1.06x faster                                                  |
| xml_etree_iterparse  | 114 ms                                                                       | 108 ms: 1.05x faster                                                    |
| pickle_dict          | 32.7 us                                                                      | 31.2 us: 1.05x faster                                                   |
| pickle               | 10.8 us                                                                      | 10.4 us: 1.04x faster                                                   |
| xml_etree_generate   | 93.8 ms                                                                      | 90.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 64.6 ms                                                                      | 62.5 ms: 1.03x faster                                                   |
| unpickle             | 15.3 us                                                                      | 14.8 us: 1.03x faster                                                   |
| xml_etree_parse      | 147 ms                                                                       | 144 ms: 1.02x faster                                                    |
| pickle_list          | 4.46 us                                                                      | 4.38 us: 1.02x faster                                                   |
| pickle_pure_python   | 324 us                                                                       | 326 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                        | 1.03x faster                                                            |

Benchmark hidden because not significant (3): json_dumps, unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                      | 11.2 ms: 1.01x slower                                                   |
| python_startup         | 12.9 ms                                                                      | 13.0 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                        | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 14.0 ms                                                                      | 13.2 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                                        | 1.02x faster                                                            |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|---------------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| bench_thread_pool         | 1.14 ms                                                                      | 954 us: 1.19x faster                                                    |
| nbody                     | 130 ms                                                                       | 114 ms: 1.14x faster                                                    |
| richards                  | 61.0 ms                                                                      | 54.2 ms: 1.13x faster                                                   |
| fannkuch                  | 520 ms                                                                       | 466 ms: 1.12x faster                                                    |
| richards_super            | 67.4 ms                                                                      | 60.9 ms: 1.11x faster                                                   |
| raytrace                  | 336 ms                                                                       | 304 ms: 1.11x faster                                                    |
| hexiom                    | 10.8 ms                                                                      | 9.76 ms: 1.11x faster                                                   |
| spectral_norm             | 154 ms                                                                       | 140 ms: 1.10x faster                                                    |
| scimark_lu                | 149 ms                                                                       | 135 ms: 1.10x faster                                                    |
| float                     | 101 ms                                                                       | 91.6 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult   | 6.68 ms                                                                      | 6.14 ms: 1.09x faster                                                   |
| scimark_fft               | 437 ms                                                                       | 404 ms: 1.08x faster                                                    |
| comprehensions            | 26.7 us                                                                      | 24.7 us: 1.08x faster                                                   |
| scimark_sor               | 172 ms                                                                       | 159 ms: 1.08x faster                                                    |
| pyflate                   | 649 ms                                                                       | 604 ms: 1.08x faster                                                    |
| scimark_monte_carlo       | 99.0 ms                                                                      | 92.2 ms: 1.07x faster                                                   |
| nqueens                   | 122 ms                                                                       | 114 ms: 1.07x faster                                                    |
| regex_compile             | 208 ms                                                                       | 196 ms: 1.06x faster                                                    |
| unpickle_pure_python      | 310 us                                                                       | 293 us: 1.06x faster                                                    |
| tomli_loads               | 2.89 sec                                                                     | 2.74 sec: 1.06x faster                                                  |
| mako                      | 14.0 ms                                                                      | 13.2 ms: 1.06x faster                                                   |
| xml_etree_iterparse       | 114 ms                                                                       | 108 ms: 1.05x faster                                                    |
| crypto_pyaes              | 92.2 ms                                                                      | 87.7 ms: 1.05x faster                                                   |
| pickle_dict               | 32.7 us                                                                      | 31.2 us: 1.05x faster                                                   |
| chaos                     | 75.9 ms                                                                      | 72.5 ms: 1.05x faster                                                   |
| create_gc_cycles          | 1.94 ms                                                                      | 1.85 ms: 1.05x faster                                                   |
| pickle                    | 10.8 us                                                                      | 10.4 us: 1.04x faster                                                   |
| bench_mp_pool             | 4.97 ms                                                                      | 4.77 ms: 1.04x faster                                                   |
| xml_etree_generate        | 93.8 ms                                                                      | 90.3 ms: 1.04x faster                                                   |
| regex_v8                  | 26.6 ms                                                                      | 25.6 ms: 1.04x faster                                                   |
| deepcopy_memo             | 45.1 us                                                                      | 43.7 us: 1.03x faster                                                   |
| xml_etree_process         | 64.6 ms                                                                      | 62.5 ms: 1.03x faster                                                   |
| unpickle                  | 15.3 us                                                                      | 14.8 us: 1.03x faster                                                   |
| sqlite_synth              | 2.87 us                                                                      | 2.78 us: 1.03x faster                                                   |
| chameleon                 | 8.00 ms                                                                      | 7.77 ms: 1.03x faster                                                   |
| xml_etree_parse           | 147 ms                                                                       | 144 ms: 1.02x faster                                                    |
| sqlglot_transpile         | 1.99 ms                                                                      | 1.95 ms: 1.02x faster                                                   |
| pickle_list               | 4.46 us                                                                      | 4.38 us: 1.02x faster                                                   |
| async_generators          | 391 ms                                                                       | 385 ms: 1.02x faster                                                    |
| docutils                  | 3.29 sec                                                                     | 3.24 sec: 1.02x faster                                                  |
| pprint_pformat            | 2.01 sec                                                                     | 1.98 sec: 1.01x faster                                                  |
| sympy_integrate           | 26.9 ms                                                                      | 26.5 ms: 1.01x faster                                                   |
| regex_dna                 | 239 ms                                                                       | 236 ms: 1.01x faster                                                    |
| sympy_expand              | 584 ms                                                                       | 577 ms: 1.01x faster                                                    |
| pycparser                 | 1.36 sec                                                                     | 1.35 sec: 1.01x faster                                                  |
| pprint_safe_repr          | 983 ms                                                                       | 971 ms: 1.01x faster                                                    |
| thrift                    | 893 us                                                                       | 882 us: 1.01x faster                                                    |
| 2to3                      | 320 ms                                                                       | 316 ms: 1.01x faster                                                    |
| sqlglot_parse             | 1.57 ms                                                                      | 1.55 ms: 1.01x faster                                                   |
| dulwich_log               | 77.8 ms                                                                      | 77.1 ms: 1.01x faster                                                   |
| sympy_str                 | 350 ms                                                                       | 347 ms: 1.01x faster                                                    |
| asyncio_websockets        | 395 ms                                                                       | 392 ms: 1.01x faster                                                    |
| mdp                       | 2.68 sec                                                                     | 2.67 sec: 1.01x faster                                                  |
| sqlglot_optimize          | 67.5 ms                                                                      | 67.0 ms: 1.01x faster                                                   |
| logging_simple            | 6.63 us                                                                      | 6.59 us: 1.01x faster                                                   |
| meteor_contest            | 143 ms                                                                       | 142 ms: 1.01x faster                                                    |
| logging_format            | 7.33 us                                                                      | 7.29 us: 1.01x faster                                                   |
| sqlglot_normalize         | 130 ms                                                                       | 129 ms: 1.00x faster                                                    |
| pidigits                  | 265 ms                                                                       | 266 ms: 1.00x slower                                                    |
| python_startup_no_site    | 11.2 ms                                                                      | 11.2 ms: 1.01x slower                                                   |
| python_startup            | 12.9 ms                                                                      | 13.0 ms: 1.01x slower                                                   |
| html5lib                  | 79.1 ms                                                                      | 79.7 ms: 1.01x slower                                                   |
| pickle_pure_python        | 324 us                                                                       | 326 us: 1.01x slower                                                    |
| json                      | 5.38 ms                                                                      | 5.43 ms: 1.01x slower                                                   |
| asyncio_tcp               | 379 ms                                                                       | 383 ms: 1.01x slower                                                    |
| aiohttp                   | 1.13 ms                                                                      | 1.14 ms: 1.01x slower                                                   |
| coroutines                | 22.3 ms                                                                      | 22.6 ms: 1.01x slower                                                   |
| regex_effbot              | 3.54 ms                                                                      | 3.58 ms: 1.01x slower                                                   |
| pathlib                   | 20.3 ms                                                                      | 20.6 ms: 1.02x slower                                                   |
| deepcopy_reduce           | 3.59 us                                                                      | 3.66 us: 1.02x slower                                                   |
| generators                | 33.0 ms                                                                      | 33.7 ms: 1.02x slower                                                   |
| async_tree_none_tg        | 346 ms                                                                       | 354 ms: 1.02x slower                                                    |
| async_tree_memoization_tg | 436 ms                                                                       | 447 ms: 1.02x slower                                                    |
| go                        | 205 ms                                                                       | 210 ms: 1.03x slower                                                    |
| telco                     | 8.29 ms                                                                      | 8.59 ms: 1.04x slower                                                   |
| logging_silent            | 99.4 ns                                                                      | 103 ns: 1.04x slower                                                    |
| deltablue                 | 3.97 ms                                                                      | 4.14 ms: 1.04x slower                                                   |
| gc_traversal              | 4.35 ms                                                                      | 4.69 ms: 1.08x slower                                                   |
| Geometric mean            | (ref)                                                                        | 1.02x faster                                                            |

Benchmark hidden because not significant (21): mypy2, json_dumps, asyncio_tcp_ssl, deepcopy, genshi_xml, genshi_text, unpickle_list, pylint, coverage, gunicorn, json_loads, sympy_sum, async_tree_none, typing_runtime_protocols, dask, tornado_http, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x