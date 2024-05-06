# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-x86
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 230 ms: 1.15x faster                                                                      |
| chameleon      | 6.42 ms                                                         | 5.67 ms: 1.13x faster                                                                     |
| docutils       | 1.95 sec                                                        | 1.77 sec: 1.10x faster                                                                    |
| html5lib       | 52.1 ms                                                         | 42.4 ms: 1.23x faster                                                                     |
| tornado_http   | 118 ms                                                          | 91.6 ms: 1.28x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 457 ms: 2.02x faster                                                                      |
| async_tree_io           | 940 ms                                                          | 510 ms: 1.84x faster                                                                      |
| async_tree_none         | 394 ms                                                          | 216 ms: 1.82x faster                                                                      |
| async_tree_memoization  | 467 ms                                                          | 262 ms: 1.78x faster                                                                      |
| Geometric mean          | (ref)                                                           | 1.86x faster                                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 196 ms: 2.57x faster                                                                      |
| float          | 69.6 ms                                                         | 52.7 ms: 1.32x faster                                                                     |
| nbody          | 79.1 ms                                                         | 75.1 ms: 1.05x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.53x faster                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 96.3 ms: 1.21x faster                                                                     |
| regex_dna      | 131 ms                                                          | 117 ms: 1.12x faster                                                                      |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                                     |
| regex_effbot   | 1.66 ms                                                         | 1.88 ms: 1.13x slower                                                                     |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.55 ms: 1.50x faster                                                                     |
| pickle_pure_python   | 280 us                                                          | 206 us: 1.36x faster                                                                      |
| unpickle_pure_python | 189 us                                                          | 145 us: 1.31x faster                                                                      |
| tomli_loads          | 1.91 sec                                                        | 1.59 sec: 1.20x faster                                                                    |
| xml_etree_parse      | 120 ms                                                          | 106 ms: 1.13x faster                                                                      |
| xml_etree_process    | 48.1 ms                                                         | 42.9 ms: 1.12x faster                                                                     |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                                     |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.1 ms: 1.09x faster                                                                     |
| xml_etree_generate   | 61.6 ms                                                         | 60.1 ms: 1.03x faster                                                                     |
| pickle               | 7.83 us                                                         | 7.88 us: 1.01x slower                                                                     |
| pickle_dict          | 18.2 us                                                         | 20.1 us: 1.10x slower                                                                     |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                              |

Benchmark hidden because not significant (3): pickle_list, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.2 ms: 1.03x faster                                                                     |
| python_startup_no_site | 18.1 ms                                                         | 19.8 ms: 1.10x slower                                                                     |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 6.76 ms: 1.35x faster                                                                     |
| genshi_text    | 21.0 ms                                                         | 19.7 ms: 1.06x faster                                                                     |
| genshi_xml     | 46.6 ms                                                         | 43.9 ms: 1.06x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.15x faster                                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 92.8 us: 4.26x faster                                                                     |
| pidigits                 | 502 ms                                                          | 196 ms: 2.57x faster                                                                      |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 457 ms: 2.02x faster                                                                      |
| pylint                   | 384 ms                                                          | 204 ms: 1.88x faster                                                                      |
| deltablue                | 4.04 ms                                                         | 2.14 ms: 1.88x faster                                                                     |
| async_tree_io            | 940 ms                                                          | 510 ms: 1.84x faster                                                                      |
| async_tree_none          | 394 ms                                                          | 216 ms: 1.82x faster                                                                      |
| async_tree_memoization   | 467 ms                                                          | 262 ms: 1.78x faster                                                                      |
| logging_silent           | 97.9 ns                                                         | 57.5 ns: 1.70x faster                                                                     |
| raytrace                 | 303 ms                                                          | 188 ms: 1.61x faster                                                                      |
| chaos                    | 74.4 ms                                                         | 46.8 ms: 1.59x faster                                                                     |
| sqlglot_parse            | 1.33 ms                                                         | 878 us: 1.51x faster                                                                      |
| go                       | 146 ms                                                          | 96.6 ms: 1.51x faster                                                                     |
| crypto_pyaes             | 81.3 ms                                                         | 53.9 ms: 1.51x faster                                                                     |
| scimark_lu               | 89.8 ms                                                         | 59.7 ms: 1.50x faster                                                                     |
| comprehensions           | 17.7 us                                                         | 11.8 us: 1.50x faster                                                                     |
| json_dumps               | 9.82 ms                                                         | 6.55 ms: 1.50x faster                                                                     |
| richards_super           | 49.9 ms                                                         | 33.6 ms: 1.49x faster                                                                     |
| scimark_sor              | 115 ms                                                          | 79.0 ms: 1.46x faster                                                                     |
| hexiom                   | 6.13 ms                                                         | 4.22 ms: 1.45x faster                                                                     |
| sqlglot_transpile        | 1.58 ms                                                         | 1.10 ms: 1.44x faster                                                                     |
| generators               | 31.6 ms                                                         | 22.5 ms: 1.40x faster                                                                     |
| pyflate                  | 422 ms                                                          | 304 ms: 1.39x faster                                                                      |
| scimark_monte_carlo      | 61.9 ms                                                         | 45.5 ms: 1.36x faster                                                                     |
| pickle_pure_python       | 280 us                                                          | 206 us: 1.36x faster                                                                      |
| pycparser                | 1.04 sec                                                        | 767 ms: 1.36x faster                                                                      |
| richards                 | 40.3 ms                                                         | 29.7 ms: 1.36x faster                                                                     |
| mako                     | 9.10 ms                                                         | 6.76 ms: 1.35x faster                                                                     |
| float                    | 69.6 ms                                                         | 52.7 ms: 1.32x faster                                                                     |
| unpickle_pure_python     | 189 us                                                          | 145 us: 1.31x faster                                                                      |
| deepcopy_memo            | 29.6 us                                                         | 22.8 us: 1.30x faster                                                                     |
| tornado_http             | 118 ms                                                          | 91.6 ms: 1.28x faster                                                                     |
| coroutines               | 17.9 ms                                                         | 14.2 ms: 1.26x faster                                                                     |
| html5lib                 | 52.1 ms                                                         | 42.4 ms: 1.23x faster                                                                     |
| nqueens                  | 87.1 ms                                                         | 70.9 ms: 1.23x faster                                                                     |
| sympy_sum                | 122 ms                                                          | 101 ms: 1.22x faster                                                                      |
| regex_compile            | 117 ms                                                          | 96.3 ms: 1.21x faster                                                                     |
| sqlite_synth             | 2.29 us                                                         | 1.90 us: 1.21x faster                                                                     |
| tomli_loads              | 1.91 sec                                                        | 1.59 sec: 1.20x faster                                                                    |
| pprint_pformat           | 1.37 sec                                                        | 1.14 sec: 1.20x faster                                                                    |
| pprint_safe_repr         | 658 ms                                                          | 558 ms: 1.18x faster                                                                      |
| json                     | 4.76 ms                                                         | 4.04 ms: 1.18x faster                                                                     |
| sympy_integrate          | 16.6 ms                                                         | 14.2 ms: 1.18x faster                                                                     |
| spectral_norm            | 80.2 ms                                                         | 68.7 ms: 1.17x faster                                                                     |
| fannkuch                 | 317 ms                                                          | 275 ms: 1.16x faster                                                                      |
| 2to3                     | 265 ms                                                          | 230 ms: 1.15x faster                                                                      |
| asyncio_tcp              | 744 ms                                                          | 649 ms: 1.15x faster                                                                      |
| sympy_str                | 229 ms                                                          | 200 ms: 1.15x faster                                                                      |
| bench_thread_pool        | 1.12 ms                                                         | 979 us: 1.14x faster                                                                      |
| deepcopy                 | 310 us                                                          | 272 us: 1.14x faster                                                                      |
| chameleon                | 6.42 ms                                                         | 5.67 ms: 1.13x faster                                                                     |
| sqlglot_optimize         | 44.7 ms                                                         | 39.6 ms: 1.13x faster                                                                     |
| xml_etree_parse          | 120 ms                                                          | 106 ms: 1.13x faster                                                                      |
| mdp                      | 1.83 sec                                                        | 1.62 sec: 1.13x faster                                                                    |
| xml_etree_process        | 48.1 ms                                                         | 42.9 ms: 1.12x faster                                                                     |
| sympy_expand             | 391 ms                                                          | 349 ms: 1.12x faster                                                                      |
| sqlglot_normalize        | 230 ms                                                          | 206 ms: 1.12x faster                                                                      |
| regex_dna                | 131 ms                                                          | 117 ms: 1.12x faster                                                                      |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                                     |
| deepcopy_reduce          | 2.68 us                                                         | 2.43 us: 1.10x faster                                                                     |
| docutils                 | 1.95 sec                                                        | 1.77 sec: 1.10x faster                                                                    |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.1 ms: 1.09x faster                                                                     |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.03 ms: 1.07x faster                                                                     |
| genshi_text              | 21.0 ms                                                         | 19.7 ms: 1.06x faster                                                                     |
| genshi_xml               | 46.6 ms                                                         | 43.9 ms: 1.06x faster                                                                     |
| scimark_fft              | 216 ms                                                          | 204 ms: 1.06x faster                                                                      |
| meteor_contest           | 80.0 ms                                                         | 75.5 ms: 1.06x faster                                                                     |
| nbody                    | 79.1 ms                                                         | 75.1 ms: 1.05x faster                                                                     |
| python_startup           | 22.9 ms                                                         | 22.2 ms: 1.03x faster                                                                     |
| xml_etree_generate       | 61.6 ms                                                         | 60.1 ms: 1.03x faster                                                                     |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                                    |
| pickle                   | 7.83 us                                                         | 7.88 us: 1.01x slower                                                                     |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                                     |
| bench_mp_pool            | 66.4 ms                                                         | 68.0 ms: 1.02x slower                                                                     |
| logging_format           | 7.91 us                                                         | 8.12 us: 1.03x slower                                                                     |
| logging_simple           | 7.29 us                                                         | 7.54 us: 1.03x slower                                                                     |
| pathlib                  | 81.2 ms                                                         | 85.6 ms: 1.05x slower                                                                     |
| create_gc_cycles         | 694 us                                                          | 733 us: 1.06x slower                                                                      |
| python_startup_no_site   | 18.1 ms                                                         | 19.8 ms: 1.10x slower                                                                     |
| pickle_dict              | 18.2 us                                                         | 20.1 us: 1.10x slower                                                                     |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                                     |
| regex_effbot             | 1.66 ms                                                         | 1.88 ms: 1.13x slower                                                                     |
| async_generators         | 241 ms                                                          | 278 ms: 1.15x slower                                                                      |
| telco                    | 4.83 ms                                                         | 6.00 ms: 1.24x slower                                                                     |
| thrift                   | 902 us                                                          | 9.74 ms: 10.80x slower                                                                    |
| coverage                 | 46.6 ms                                                         | 507 ms: 10.89x slower                                                                     |
| Geometric mean           | (ref)                                                           | 1.17x faster                                                                              |

Benchmark hidden because not significant (3): pickle_list, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: unknown