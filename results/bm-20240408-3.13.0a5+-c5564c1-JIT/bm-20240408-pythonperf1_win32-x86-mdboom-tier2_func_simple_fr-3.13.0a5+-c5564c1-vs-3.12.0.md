# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 258 ms: 1.08x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.25 ms: 1.24x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| tornado_http   | 105 ms                                                          | 96.9 ms: 1.08x faster                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 268 ms: 1.31x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 290 ms: 1.25x faster                                                            |
| async_tree_io              | 693 ms                                                          | 556 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 549 ms: 1.23x faster                                                            |
| async_tree_none            | 298 ms                                                          | 241 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 460 ms: 1.19x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 490 ms: 1.15x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.1 ms: 1.44x faster                                                           |
| nbody          | 127 ms                                                          | 94.8 ms: 1.34x faster                                                           |
| pidigits       | 199 ms                                                          | 198 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 112 ms: 1.15x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| regex_dna      | 127 ms                                                          | 121 ms: 1.05x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 222 us: 1.29x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.80 sec: 1.22x faster                                                          |
| unpickle_pure_python | 210 us                                                          | 172 us: 1.22x faster                                                            |
| xml_etree_process    | 53.2 ms                                                         | 44.2 ms: 1.20x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.0 ms: 1.20x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 61.6 ms: 1.17x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.87 ms: 1.08x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 106 ms: 1.07x faster                                                            |
| unpickle_list        | 2.95 us                                                         | 2.82 us: 1.04x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.0 us: 1.02x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.33 us: 1.01x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 20.0 us: 1.01x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| pickle               | 7.79 us                                                         | 8.13 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                           |
| python_startup_no_site | 19.1 ms                                                         | 22.0 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 6.99 ms: 1.42x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.0 ms: 1.75x faster                                                           |
| logging_silent             | 101 ns                                                          | 61.0 ns: 1.66x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 24.8 us: 1.55x faster                                                           |
| float                      | 76.7 ms                                                         | 53.1 ms: 1.44x faster                                                           |
| mako                       | 9.96 ms                                                         | 6.99 ms: 1.42x faster                                                           |
| spectral_norm              | 104 ms                                                          | 73.6 ms: 1.41x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.1 ms: 1.38x faster                                                           |
| nbody                      | 127 ms                                                          | 94.8 ms: 1.34x faster                                                           |
| raytrace                   | 308 ms                                                          | 231 ms: 1.34x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 268 ms: 1.31x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.74 ms: 1.31x faster                                                           |
| scimark_sor                | 130 ms                                                          | 101 ms: 1.29x faster                                                            |
| pickle_pure_python         | 286 us                                                          | 222 us: 1.29x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 101 us: 1.26x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 290 ms: 1.25x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 997 us: 1.25x faster                                                            |
| async_tree_io              | 693 ms                                                          | 556 ms: 1.25x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 6.25 ms: 1.24x faster                                                           |
| deepcopy                   | 360 us                                                          | 291 us: 1.24x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.61 us: 1.23x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 549 ms: 1.23x faster                                                            |
| async_tree_none            | 298 ms                                                          | 241 ms: 1.23x faster                                                            |
| comprehensions             | 19.2 us                                                         | 15.6 us: 1.23x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.25 ms: 1.23x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.80 sec: 1.22x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 172 us: 1.22x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 44.2 ms: 1.20x faster                                                           |
| logging_simple             | 9.75 us                                                         | 8.11 us: 1.20x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.22 ms: 1.20x faster                                                           |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.0 ms: 1.20x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.76 us: 1.19x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 460 ms: 1.19x faster                                                            |
| richards                   | 41.3 ms                                                         | 35.2 ms: 1.18x faster                                                           |
| richards_super             | 46.5 ms                                                         | 39.5 ms: 1.18x faster                                                           |
| pyflate                    | 424 ms                                                          | 362 ms: 1.17x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 61.6 ms: 1.17x faster                                                           |
| regex_compile              | 129 ms                                                          | 112 ms: 1.15x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 490 ms: 1.15x faster                                                            |
| pycparser                  | 978 ms                                                          | 850 ms: 1.15x faster                                                            |
| chaos                      | 69.4 ms                                                         | 61.2 ms: 1.13x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 6.10 ms: 1.12x faster                                                           |
| crypto_pyaes               | 69.2 ms                                                         | 62.4 ms: 1.11x faster                                                           |
| go                         | 137 ms                                                          | 124 ms: 1.11x faster                                                            |
| scimark_fft                | 271 ms                                                          | 245 ms: 1.10x faster                                                            |
| fannkuch                   | 354 ms                                                          | 321 ms: 1.10x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 1.00 ms: 1.10x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 112 ms: 1.10x faster                                                            |
| async_generators           | 313 ms                                                          | 288 ms: 1.09x faster                                                            |
| 2to3                       | 280 ms                                                          | 258 ms: 1.08x faster                                                            |
| tornado_http               | 105 ms                                                          | 96.9 ms: 1.08x faster                                                           |
| sympy_str                  | 240 ms                                                          | 221 ms: 1.08x faster                                                            |
| scimark_lu                 | 93.2 ms                                                         | 86.2 ms: 1.08x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.87 ms: 1.08x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 106 ms: 1.07x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.80 sec: 1.06x faster                                                          |
| sympy_integrate            | 17.5 ms                                                         | 16.6 ms: 1.06x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 82.6 ms: 1.05x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 63.3 ms: 1.05x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 46.2 ms: 1.05x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 87.1 ms: 1.05x faster                                                           |
| regex_dna                  | 127 ms                                                          | 121 ms: 1.05x faster                                                            |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.04x faster                                                          |
| sqlite_synth               | 2.07 us                                                         | 1.98 us: 1.04x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.82 us: 1.04x faster                                                           |
| sympy_expand               | 398 ms                                                          | 382 ms: 1.04x faster                                                            |
| bench_mp_pool              | 75.4 ms                                                         | 73.8 ms: 1.02x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| json_loads                 | 20.4 us                                                         | 20.0 us: 1.02x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.33 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 198 ms: 1.00x faster                                                            |
| pickle_dict                | 19.9 us                                                         | 20.0 us: 1.01x slower                                                           |
| nqueens                    | 93.7 ms                                                         | 94.2 ms: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| pickle                     | 7.79 us                                                         | 8.13 us: 1.04x slower                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.58 sec: 1.05x slower                                                          |
| pprint_safe_repr           | 721 ms                                                          | 769 ms: 1.07x slower                                                            |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| python_startup             | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 745 us: 1.14x slower                                                            |
| python_startup_no_site     | 19.1 ms                                                         | 22.0 ms: 1.15x slower                                                           |
| telco                      | 5.51 ms                                                         | 6.43 ms: 1.17x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 233 ms: 2.33x slower                                                            |
| coverage                   | 48.4 ms                                                         | 531 ms: 10.96x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (3): asyncio_tcp, json, gc_traversal
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown