# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-x86
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.00x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| chameleon      | 5.80 ms                                                                         | 5.67 ms: 1.02x faster                                                                     |
| docutils       | 1.78 sec                                                                        | 1.77 sec: 1.00x faster                                                                    |
| html5lib       | 42.5 ms                                                                         | 42.4 ms: 1.00x faster                                                                     |
| tornado_http   | 93.1 ms                                                                         | 91.6 ms: 1.02x faster                                                                     |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                              |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 450 ms                                                                          | 439 ms: 1.03x faster                                                                      |
| Geometric mean             | (ref)                                                                           | 1.01x faster                                                                              |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_io_tg, async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| nbody          | 77.9 ms                                                                         | 75.1 ms: 1.04x faster                                                                     |
| float          | 53.3 ms                                                                         | 52.7 ms: 1.01x faster                                                                     |
| pidigits       | 197 ms                                                                          | 196 ms: 1.00x faster                                                                      |
| Geometric mean | (ref)                                                                           | 1.02x faster                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| regex_dna      | 122 ms                                                                          | 117 ms: 1.04x faster                                                                      |
| regex_effbot   | 1.91 ms                                                                         | 1.88 ms: 1.01x faster                                                                     |
| regex_compile  | 97.5 ms                                                                         | 96.3 ms: 1.01x faster                                                                     |
| Geometric mean | (ref)                                                                           | 1.02x faster                                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|---------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| pickle_list         | 3.63 us                                                                         | 3.21 us: 1.13x faster                                                                     |
| pickle_dict         | 21.3 us                                                                         | 20.1 us: 1.06x faster                                                                     |
| pickle              | 8.05 us                                                                         | 7.88 us: 1.02x faster                                                                     |
| unpickle            | 10.0 us                                                                         | 9.87 us: 1.02x faster                                                                     |
| xml_etree_parse     | 107 ms                                                                          | 106 ms: 1.01x faster                                                                      |
| tomli_loads         | 1.60 sec                                                                        | 1.59 sec: 1.01x faster                                                                    |
| xml_etree_iterparse | 65.4 ms                                                                         | 65.1 ms: 1.00x faster                                                                     |
| pickle_pure_python  | 204 us                                                                          | 206 us: 1.01x slower                                                                      |
| json_loads          | 19.9 us                                                                         | 20.1 us: 1.01x slower                                                                     |
| xml_etree_process   | 40.6 ms                                                                         | 42.9 ms: 1.06x slower                                                                     |
| unpickle_list       | 2.70 us                                                                         | 3.00 us: 1.11x slower                                                                     |
| Geometric mean      | (ref)                                                                           | 1.00x faster                                                                              |

Benchmark hidden because not significant (3): xml_etree_generate, unpickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| mako           | 7.06 ms                                                                         | 6.76 ms: 1.04x faster                                                                     |
| genshi_text    | 19.5 ms                                                                         | 19.7 ms: 1.01x slower                                                                     |
| genshi_xml     | 43.2 ms                                                                         | 43.9 ms: 1.02x slower                                                                     |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240406-pythonperf1_win32-x86-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| pickle_list                | 3.63 us                                                                         | 3.21 us: 1.13x faster                                                                     |
| chaos                      | 49.9 ms                                                                         | 46.8 ms: 1.07x faster                                                                     |
| pickle_dict                | 21.3 us                                                                         | 20.1 us: 1.06x faster                                                                     |
| mako                       | 7.06 ms                                                                         | 6.76 ms: 1.04x faster                                                                     |
| crypto_pyaes               | 56.3 ms                                                                         | 53.9 ms: 1.04x faster                                                                     |
| regex_dna                  | 122 ms                                                                          | 117 ms: 1.04x faster                                                                      |
| nbody                      | 77.9 ms                                                                         | 75.1 ms: 1.04x faster                                                                     |
| coroutines                 | 14.7 ms                                                                         | 14.2 ms: 1.04x faster                                                                     |
| pyflate                    | 315 ms                                                                          | 304 ms: 1.04x faster                                                                      |
| hexiom                     | 4.36 ms                                                                         | 4.22 ms: 1.03x faster                                                                     |
| scimark_fft                | 210 ms                                                                          | 204 ms: 1.03x faster                                                                      |
| scimark_sparse_mat_mult    | 3.11 ms                                                                         | 3.03 ms: 1.03x faster                                                                     |
| async_tree_cpu_io_mixed_tg | 450 ms                                                                          | 439 ms: 1.03x faster                                                                      |
| chameleon                  | 5.80 ms                                                                         | 5.67 ms: 1.02x faster                                                                     |
| pickle                     | 8.05 us                                                                         | 7.88 us: 1.02x faster                                                                     |
| unpickle                   | 10.0 us                                                                         | 9.87 us: 1.02x faster                                                                     |
| scimark_sor                | 80.3 ms                                                                         | 79.0 ms: 1.02x faster                                                                     |
| sympy_integrate            | 14.4 ms                                                                         | 14.2 ms: 1.02x faster                                                                     |
| pprint_pformat             | 1.16 sec                                                                        | 1.14 sec: 1.02x faster                                                                    |
| tornado_http               | 93.1 ms                                                                         | 91.6 ms: 1.02x faster                                                                     |
| go                         | 98.1 ms                                                                         | 96.6 ms: 1.02x faster                                                                     |
| regex_effbot               | 1.91 ms                                                                         | 1.88 ms: 1.01x faster                                                                     |
| regex_compile              | 97.5 ms                                                                         | 96.3 ms: 1.01x faster                                                                     |
| float                      | 53.3 ms                                                                         | 52.7 ms: 1.01x faster                                                                     |
| sqlite_synth               | 1.92 us                                                                         | 1.90 us: 1.01x faster                                                                     |
| pprint_safe_repr           | 564 ms                                                                          | 558 ms: 1.01x faster                                                                      |
| richards                   | 30.0 ms                                                                         | 29.7 ms: 1.01x faster                                                                     |
| scimark_lu                 | 60.4 ms                                                                         | 59.7 ms: 1.01x faster                                                                     |
| scimark_monte_carlo        | 45.9 ms                                                                         | 45.5 ms: 1.01x faster                                                                     |
| pathlib                    | 86.3 ms                                                                         | 85.6 ms: 1.01x faster                                                                     |
| meteor_contest             | 76.1 ms                                                                         | 75.5 ms: 1.01x faster                                                                     |
| xml_etree_parse            | 107 ms                                                                          | 106 ms: 1.01x faster                                                                      |
| generators                 | 22.7 ms                                                                         | 22.5 ms: 1.01x faster                                                                     |
| tomli_loads                | 1.60 sec                                                                        | 1.59 sec: 1.01x faster                                                                    |
| docutils                   | 1.78 sec                                                                        | 1.77 sec: 1.00x faster                                                                    |
| xml_etree_iterparse        | 65.4 ms                                                                         | 65.1 ms: 1.00x faster                                                                     |
| bench_mp_pool              | 68.2 ms                                                                         | 68.0 ms: 1.00x faster                                                                     |
| pidigits                   | 197 ms                                                                          | 196 ms: 1.00x faster                                                                      |
| html5lib                   | 42.5 ms                                                                         | 42.4 ms: 1.00x faster                                                                     |
| sympy_expand               | 347 ms                                                                          | 349 ms: 1.00x slower                                                                      |
| raytrace                   | 187 ms                                                                          | 188 ms: 1.01x slower                                                                      |
| async_generators           | 276 ms                                                                          | 278 ms: 1.01x slower                                                                      |
| sqlglot_transpile          | 1.10 ms                                                                         | 1.10 ms: 1.01x slower                                                                     |
| coverage                   | 504 ms                                                                          | 507 ms: 1.01x slower                                                                      |
| nqueens                    | 70.2 ms                                                                         | 70.9 ms: 1.01x slower                                                                     |
| pickle_pure_python         | 204 us                                                                          | 206 us: 1.01x slower                                                                      |
| deltablue                  | 2.12 ms                                                                         | 2.14 ms: 1.01x slower                                                                     |
| sqlglot_parse              | 868 us                                                                          | 878 us: 1.01x slower                                                                      |
| bench_thread_pool          | 968 us                                                                          | 979 us: 1.01x slower                                                                      |
| spectral_norm              | 67.9 ms                                                                         | 68.7 ms: 1.01x slower                                                                     |
| json_loads                 | 19.9 us                                                                         | 20.1 us: 1.01x slower                                                                     |
| sqlglot_normalize          | 204 ms                                                                          | 206 ms: 1.01x slower                                                                      |
| genshi_text                | 19.5 ms                                                                         | 19.7 ms: 1.01x slower                                                                     |
| pycparser                  | 755 ms                                                                          | 767 ms: 1.02x slower                                                                      |
| deepcopy_reduce            | 2.39 us                                                                         | 2.43 us: 1.02x slower                                                                     |
| telco                      | 5.91 ms                                                                         | 6.00 ms: 1.02x slower                                                                     |
| genshi_xml                 | 43.2 ms                                                                         | 43.9 ms: 1.02x slower                                                                     |
| comprehensions             | 11.6 us                                                                         | 11.8 us: 1.02x slower                                                                     |
| sqlglot_optimize           | 38.8 ms                                                                         | 39.6 ms: 1.02x slower                                                                     |
| deepcopy                   | 262 us                                                                          | 272 us: 1.04x slower                                                                      |
| logging_simple             | 7.26 us                                                                         | 7.54 us: 1.04x slower                                                                     |
| logging_format             | 7.82 us                                                                         | 8.12 us: 1.04x slower                                                                     |
| xml_etree_process          | 40.6 ms                                                                         | 42.9 ms: 1.06x slower                                                                     |
| typing_runtime_protocols   | 87.6 us                                                                         | 92.8 us: 1.06x slower                                                                     |
| unpickle_list              | 2.70 us                                                                         | 3.00 us: 1.11x slower                                                                     |
| Geometric mean             | (ref)                                                                           | 1.00x faster                                                                              |

Benchmark hidden because not significant (28): async_tree_none_tg, async_tree_memoization_tg, json, async_tree_none, xml_etree_generate, async_tree_io_tg, async_tree_io, async_tree_memoization, mdp, async_tree_cpu_io_mixed, gc_traversal, logging_silent, asyncio_tcp_ssl, asyncio_tcp, 2to3, deepcopy_memo, sympy_str, richards_super, pylint, sympy_sum, thrift, create_gc_cycles, fannkuch, regex_v8, python_startup, python_startup_no_site, unpickle_pure_python, json_dumps

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown