# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.00x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 290 ms                                                                       | 290 ms: 1.00x faster                                                                   |
| docutils       | 3.01 sec                                                                     | 2.98 sec: 1.01x faster                                                                 |
| Geometric mean | (ref)                                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (3): chameleon, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 93.5 ms                                                                      | 85.5 ms: 1.09x faster                                                                  |
| float          | 76.3 ms                                                                      | 75.4 ms: 1.01x faster                                                                  |
| Geometric mean | (ref)                                                                        | 1.03x faster                                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                      | 25.4 ms: 1.02x faster                                                                  |
| regex_dna      | 244 ms                                                                       | 243 ms: 1.01x faster                                                                   |
| regex_effbot   | 3.43 ms                                                                      | 3.57 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_dict          | 32.9 us                                                                      | 30.7 us: 1.07x faster                                                                  |
| pickle               | 10.7 us                                                                      | 10.3 us: 1.04x faster                                                                  |
| pickle_list          | 4.44 us                                                                      | 4.39 us: 1.01x faster                                                                  |
| json_loads           | 25.6 us                                                                      | 25.5 us: 1.00x faster                                                                  |
| xml_etree_generate   | 84.3 ms                                                                      | 84.8 ms: 1.01x slower                                                                  |
| tomli_loads          | 2.22 sec                                                                     | 2.23 sec: 1.01x slower                                                                 |
| unpickle_list        | 4.52 us                                                                      | 4.55 us: 1.01x slower                                                                  |
| xml_etree_parse      | 146 ms                                                                       | 147 ms: 1.01x slower                                                                   |
| xml_etree_iterparse  | 103 ms                                                                       | 105 ms: 1.01x slower                                                                   |
| unpickle             | 14.6 us                                                                      | 14.9 us: 1.02x slower                                                                  |
| unpickle_pure_python | 212 us                                                                       | 227 us: 1.07x slower                                                                   |
| Geometric mean       | (ref)                                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 12.8 ms                                                                      | 12.8 ms: 1.00x faster                                                                  |
| python_startup_no_site | 11.1 ms                                                                      | 11.1 ms: 1.00x faster                                                                  |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml     | 53.7 ms                                                                      | 54.8 ms: 1.02x slower                                                                  |
| genshi_text    | 25.1 ms                                                                      | 25.6 ms: 1.02x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240406-pythonperf2-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| scimark_sor              | 143 ms                                                                       | 130 ms: 1.10x faster                                                                   |
| nbody                    | 93.5 ms                                                                      | 85.5 ms: 1.09x faster                                                                  |
| pickle_dict              | 32.9 us                                                                      | 30.7 us: 1.07x faster                                                                  |
| coverage                 | 85.8 ms                                                                      | 82.1 ms: 1.04x faster                                                                  |
| pickle                   | 10.7 us                                                                      | 10.3 us: 1.04x faster                                                                  |
| nqueens                  | 88.9 ms                                                                      | 86.7 ms: 1.03x faster                                                                  |
| comprehensions           | 17.0 us                                                                      | 16.6 us: 1.02x faster                                                                  |
| regex_v8                 | 26.0 ms                                                                      | 25.4 ms: 1.02x faster                                                                  |
| telco                    | 8.09 ms                                                                      | 7.92 ms: 1.02x faster                                                                  |
| hexiom                   | 6.59 ms                                                                      | 6.45 ms: 1.02x faster                                                                  |
| fannkuch                 | 388 ms                                                                       | 380 ms: 1.02x faster                                                                   |
| deepcopy                 | 384 us                                                                       | 377 us: 1.02x faster                                                                   |
| mdp                      | 2.54 sec                                                                     | 2.50 sec: 1.02x faster                                                                 |
| scimark_lu               | 97.1 ms                                                                      | 95.6 ms: 1.02x faster                                                                  |
| spectral_norm            | 95.5 ms                                                                      | 94.0 ms: 1.02x faster                                                                  |
| dulwich_log              | 68.8 ms                                                                      | 67.8 ms: 1.02x faster                                                                  |
| sqlglot_normalize        | 119 ms                                                                       | 117 ms: 1.02x faster                                                                   |
| crypto_pyaes             | 72.3 ms                                                                      | 71.3 ms: 1.01x faster                                                                  |
| pyflate                  | 508 ms                                                                       | 502 ms: 1.01x faster                                                                   |
| float                    | 76.3 ms                                                                      | 75.4 ms: 1.01x faster                                                                  |
| pprint_safe_repr         | 795 ms                                                                       | 787 ms: 1.01x faster                                                                   |
| aiohttp                  | 1.07 ms                                                                      | 1.06 ms: 1.01x faster                                                                  |
| sqlglot_optimize         | 59.0 ms                                                                      | 58.4 ms: 1.01x faster                                                                  |
| pickle_list              | 4.44 us                                                                      | 4.39 us: 1.01x faster                                                                  |
| gunicorn                 | 1.05 ms                                                                      | 1.04 ms: 1.01x faster                                                                  |
| deepcopy_memo            | 37.2 us                                                                      | 36.9 us: 1.01x faster                                                                  |
| raytrace                 | 253 ms                                                                       | 251 ms: 1.01x faster                                                                   |
| docutils                 | 3.01 sec                                                                     | 2.98 sec: 1.01x faster                                                                 |
| deepcopy_reduce          | 3.45 us                                                                      | 3.42 us: 1.01x faster                                                                  |
| asyncio_websockets       | 392 ms                                                                       | 389 ms: 1.01x faster                                                                   |
| asyncio_tcp              | 371 ms                                                                       | 368 ms: 1.01x faster                                                                   |
| chaos                    | 58.5 ms                                                                      | 58.2 ms: 1.01x faster                                                                  |
| typing_runtime_protocols | 119 us                                                                       | 118 us: 1.01x faster                                                                   |
| pprint_pformat           | 1.62 sec                                                                     | 1.61 sec: 1.01x faster                                                                 |
| regex_dna                | 244 ms                                                                       | 243 ms: 1.01x faster                                                                   |
| pylint                   | 317 ms                                                                       | 315 ms: 1.00x faster                                                                   |
| json_loads               | 25.6 us                                                                      | 25.5 us: 1.00x faster                                                                  |
| python_startup           | 12.8 ms                                                                      | 12.8 ms: 1.00x faster                                                                  |
| 2to3                     | 290 ms                                                                       | 290 ms: 1.00x faster                                                                   |
| python_startup_no_site   | 11.1 ms                                                                      | 11.1 ms: 1.00x faster                                                                  |
| thrift                   | 877 us                                                                       | 880 us: 1.00x slower                                                                   |
| pathlib                  | 19.2 ms                                                                      | 19.2 ms: 1.00x slower                                                                  |
| async_generators         | 352 ms                                                                       | 353 ms: 1.00x slower                                                                   |
| richards                 | 51.8 ms                                                                      | 52.0 ms: 1.01x slower                                                                  |
| xml_etree_generate       | 84.3 ms                                                                      | 84.8 ms: 1.01x slower                                                                  |
| gc_traversal             | 4.62 ms                                                                      | 4.65 ms: 1.01x slower                                                                  |
| tomli_loads              | 2.22 sec                                                                     | 2.23 sec: 1.01x slower                                                                 |
| unpickle_list            | 4.52 us                                                                      | 4.55 us: 1.01x slower                                                                  |
| xml_etree_parse          | 146 ms                                                                       | 147 ms: 1.01x slower                                                                   |
| pycparser                | 1.26 sec                                                                     | 1.27 sec: 1.01x slower                                                                 |
| sqlite_synth             | 2.70 us                                                                      | 2.73 us: 1.01x slower                                                                  |
| deltablue                | 3.40 ms                                                                      | 3.43 ms: 1.01x slower                                                                  |
| xml_etree_iterparse      | 103 ms                                                                       | 105 ms: 1.01x slower                                                                   |
| logging_simple           | 6.43 us                                                                      | 6.52 us: 1.01x slower                                                                  |
| go                       | 169 ms                                                                       | 172 ms: 1.01x slower                                                                   |
| logging_silent           | 95.1 ns                                                                      | 96.7 ns: 1.02x slower                                                                  |
| logging_format           | 7.15 us                                                                      | 7.27 us: 1.02x slower                                                                  |
| unpickle                 | 14.6 us                                                                      | 14.9 us: 1.02x slower                                                                  |
| genshi_xml               | 53.7 ms                                                                      | 54.8 ms: 1.02x slower                                                                  |
| genshi_text              | 25.1 ms                                                                      | 25.6 ms: 1.02x slower                                                                  |
| scimark_fft              | 301 ms                                                                       | 309 ms: 1.03x slower                                                                   |
| bench_mp_pool            | 4.57 ms                                                                      | 4.73 ms: 1.04x slower                                                                  |
| regex_effbot             | 3.43 ms                                                                      | 3.57 ms: 1.04x slower                                                                  |
| scimark_sparse_mat_mult  | 4.21 ms                                                                      | 4.38 ms: 1.04x slower                                                                  |
| unpickle_pure_python     | 212 us                                                                       | 227 us: 1.07x slower                                                                   |
| Geometric mean           | (ref)                                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (34): create_gc_cycles, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, html5lib, sqlglot_parse, async_tree_none_tg, xml_etree_process, async_tree_cpu_io_mixed_tg, scimark_monte_carlo, generators, chameleon, async_tree_memoization, pickle_pure_python, sqlglot_transpile, sympy_sum, sympy_integrate, mypy2, pidigits, asyncio_tcp_ssl, regex_compile, async_tree_none, meteor_contest, sympy_str, sympy_expand, async_tree_io, json_dumps, dask, json, mako, richards_super, coroutines, tornado_http, bench_thread_pool

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x