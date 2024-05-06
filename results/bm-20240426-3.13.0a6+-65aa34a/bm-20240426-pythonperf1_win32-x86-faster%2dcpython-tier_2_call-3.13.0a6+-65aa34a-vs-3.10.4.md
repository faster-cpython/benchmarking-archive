# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-x86
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 235 ms: 1.13x faster                                                             |
| chameleon      | 6.42 ms                                                         | 5.69 ms: 1.13x faster                                                            |
| docutils       | 1.95 sec                                                        | 1.80 sec: 1.08x faster                                                           |
| html5lib       | 52.1 ms                                                         | 43.1 ms: 1.21x faster                                                            |
| tornado_http   | 118 ms                                                          | 102 ms: 1.15x faster                                                             |
| Geometric mean | (ref)                                                           | 1.14x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 480 ms: 1.92x faster                                                             |
| async_tree_io           | 940 ms                                                          | 529 ms: 1.78x faster                                                             |
| async_tree_none         | 394 ms                                                          | 228 ms: 1.73x faster                                                             |
| async_tree_memoization  | 467 ms                                                          | 275 ms: 1.70x faster                                                             |
| Geometric mean          | (ref)                                                           | 1.78x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 200 ms: 2.51x faster                                                             |
| float          | 69.6 ms                                                         | 53.0 ms: 1.31x faster                                                            |
| nbody          | 79.1 ms                                                         | 80.3 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                           | 1.48x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 96.3 ms: 1.21x faster                                                            |
| regex_dna      | 131 ms                                                          | 121 ms: 1.08x faster                                                             |
| regex_effbot   | 1.66 ms                                                         | 1.87 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 140 us: 1.36x faster                                                             |
| pickle_pure_python   | 280 us                                                          | 209 us: 1.34x faster                                                             |
| tomli_loads          | 1.91 sec                                                        | 1.58 sec: 1.21x faster                                                           |
| xml_etree_process    | 48.1 ms                                                         | 41.8 ms: 1.15x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 106 ms: 1.13x faster                                                             |
| json_loads           | 22.4 us                                                         | 19.9 us: 1.12x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.2 ms: 1.09x faster                                                            |
| xml_etree_generate   | 61.6 ms                                                         | 58.8 ms: 1.05x faster                                                            |
| unpickle_list        | 2.98 us                                                         | 2.90 us: 1.03x faster                                                            |
| pickle               | 7.83 us                                                         | 7.90 us: 1.01x slower                                                            |
| pickle_list          | 3.22 us                                                         | 3.26 us: 1.01x slower                                                            |
| unpickle             | 9.82 us                                                         | 9.97 us: 1.02x slower                                                            |
| pickle_dict          | 18.2 us                                                         | 20.3 us: 1.11x slower                                                            |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.6 ms: 1.01x faster                                                            |
| python_startup_no_site | 18.1 ms                                                         | 18.4 ms: 1.02x slower                                                            |
| Geometric mean         | (ref)                                                           | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.94 ms: 1.31x faster                                                            |
| django_template | 36.0 ms                                                         | 29.8 ms: 1.21x faster                                                            |
| genshi_text     | 21.0 ms                                                         | 18.9 ms: 1.11x faster                                                            |
| genshi_xml      | 46.6 ms                                                         | 43.1 ms: 1.08x faster                                                            |
| Geometric mean  | (ref)                                                           | 1.17x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 131 us: 3.03x faster                                                             |
| pidigits                 | 502 ms                                                          | 200 ms: 2.51x faster                                                             |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 480 ms: 1.92x faster                                                             |
| deltablue                | 4.04 ms                                                         | 2.16 ms: 1.87x faster                                                            |
| async_tree_io            | 940 ms                                                          | 529 ms: 1.78x faster                                                             |
| pylint                   | 384 ms                                                          | 218 ms: 1.76x faster                                                             |
| logging_silent           | 97.9 ns                                                         | 56.1 ns: 1.74x faster                                                            |
| async_tree_none          | 394 ms                                                          | 228 ms: 1.73x faster                                                             |
| async_tree_memoization   | 467 ms                                                          | 275 ms: 1.70x faster                                                             |
| raytrace                 | 303 ms                                                          | 182 ms: 1.67x faster                                                             |
| chaos                    | 74.4 ms                                                         | 47.5 ms: 1.57x faster                                                            |
| comprehensions           | 17.7 us                                                         | 11.7 us: 1.52x faster                                                            |
| richards_super           | 49.9 ms                                                         | 33.0 ms: 1.51x faster                                                            |
| crypto_pyaes             | 81.3 ms                                                         | 54.9 ms: 1.48x faster                                                            |
| scimark_lu               | 89.8 ms                                                         | 60.7 ms: 1.48x faster                                                            |
| sqlglot_parse            | 1.33 ms                                                         | 907 us: 1.47x faster                                                             |
| go                       | 146 ms                                                          | 99.6 ms: 1.46x faster                                                            |
| scimark_sor              | 115 ms                                                          | 79.1 ms: 1.46x faster                                                            |
| json_dumps               | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                            |
| hexiom                   | 6.13 ms                                                         | 4.24 ms: 1.45x faster                                                            |
| sqlglot_transpile        | 1.58 ms                                                         | 1.13 ms: 1.40x faster                                                            |
| generators               | 31.6 ms                                                         | 22.6 ms: 1.40x faster                                                            |
| richards                 | 40.3 ms                                                         | 29.5 ms: 1.37x faster                                                            |
| pycparser                | 1.04 sec                                                        | 766 ms: 1.36x faster                                                             |
| unpickle_pure_python     | 189 us                                                          | 140 us: 1.36x faster                                                             |
| pyflate                  | 422 ms                                                          | 313 ms: 1.35x faster                                                             |
| pickle_pure_python       | 280 us                                                          | 209 us: 1.34x faster                                                             |
| scimark_monte_carlo      | 61.9 ms                                                         | 46.8 ms: 1.32x faster                                                            |
| float                    | 69.6 ms                                                         | 53.0 ms: 1.31x faster                                                            |
| mako                     | 9.10 ms                                                         | 6.94 ms: 1.31x faster                                                            |
| nqueens                  | 87.1 ms                                                         | 68.2 ms: 1.28x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 23.3 us: 1.27x faster                                                            |
| regex_compile            | 117 ms                                                          | 96.3 ms: 1.21x faster                                                            |
| html5lib                 | 52.1 ms                                                         | 43.1 ms: 1.21x faster                                                            |
| django_template          | 36.0 ms                                                         | 29.8 ms: 1.21x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.58 sec: 1.21x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.93 us: 1.18x faster                                                            |
| sympy_sum                | 122 ms                                                          | 104 ms: 1.18x faster                                                             |
| spectral_norm            | 80.2 ms                                                         | 67.9 ms: 1.18x faster                                                            |
| sympy_integrate          | 16.6 ms                                                         | 14.2 ms: 1.17x faster                                                            |
| pprint_pformat           | 1.37 sec                                                        | 1.17 sec: 1.17x faster                                                           |
| fannkuch                 | 317 ms                                                          | 273 ms: 1.16x faster                                                             |
| sqlglot_optimize         | 44.7 ms                                                         | 38.7 ms: 1.15x faster                                                            |
| sqlglot_normalize        | 230 ms                                                          | 200 ms: 1.15x faster                                                             |
| xml_etree_process        | 48.1 ms                                                         | 41.8 ms: 1.15x faster                                                            |
| sympy_str                | 229 ms                                                          | 199 ms: 1.15x faster                                                             |
| tornado_http             | 118 ms                                                          | 102 ms: 1.15x faster                                                             |
| json                     | 4.76 ms                                                         | 4.17 ms: 1.14x faster                                                            |
| pprint_safe_repr         | 658 ms                                                          | 576 ms: 1.14x faster                                                             |
| coroutines               | 17.9 ms                                                         | 15.7 ms: 1.14x faster                                                            |
| deepcopy                 | 310 us                                                          | 272 us: 1.14x faster                                                             |
| mdp                      | 1.83 sec                                                        | 1.61 sec: 1.13x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 106 ms: 1.13x faster                                                             |
| chameleon                | 6.42 ms                                                         | 5.69 ms: 1.13x faster                                                            |
| 2to3                     | 265 ms                                                          | 235 ms: 1.13x faster                                                             |
| bench_thread_pool        | 1.12 ms                                                         | 992 us: 1.13x faster                                                             |
| sympy_expand             | 391 ms                                                          | 347 ms: 1.13x faster                                                             |
| json_loads               | 22.4 us                                                         | 19.9 us: 1.12x faster                                                            |
| genshi_text              | 21.0 ms                                                         | 18.9 ms: 1.11x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.2 ms: 1.09x faster                                                            |
| regex_dna                | 131 ms                                                          | 121 ms: 1.08x faster                                                             |
| genshi_xml               | 46.6 ms                                                         | 43.1 ms: 1.08x faster                                                            |
| docutils                 | 1.95 sec                                                        | 1.80 sec: 1.08x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.06 ms: 1.06x faster                                                            |
| xml_etree_generate       | 61.6 ms                                                         | 58.8 ms: 1.05x faster                                                            |
| deepcopy_reduce          | 2.68 us                                                         | 2.58 us: 1.04x faster                                                            |
| meteor_contest           | 80.0 ms                                                         | 76.9 ms: 1.04x faster                                                            |
| scimark_fft              | 216 ms                                                          | 208 ms: 1.04x faster                                                             |
| unpickle_list            | 2.98 us                                                         | 2.90 us: 1.03x faster                                                            |
| logging_simple           | 7.29 us                                                         | 7.12 us: 1.02x faster                                                            |
| python_startup           | 22.9 ms                                                         | 22.6 ms: 1.01x faster                                                            |
| logging_format           | 7.91 us                                                         | 7.80 us: 1.01x faster                                                            |
| pickle                   | 7.83 us                                                         | 7.90 us: 1.01x slower                                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 17.2 sec: 1.01x slower                                                           |
| pickle_list              | 3.22 us                                                         | 3.26 us: 1.01x slower                                                            |
| nbody                    | 79.1 ms                                                         | 80.3 ms: 1.01x slower                                                            |
| unpickle                 | 9.82 us                                                         | 9.97 us: 1.02x slower                                                            |
| python_startup_no_site   | 18.1 ms                                                         | 18.4 ms: 1.02x slower                                                            |
| bench_mp_pool            | 66.4 ms                                                         | 69.8 ms: 1.05x slower                                                            |
| create_gc_cycles         | 694 us                                                          | 740 us: 1.07x slower                                                             |
| pathlib                  | 81.2 ms                                                         | 90.2 ms: 1.11x slower                                                            |
| pickle_dict              | 18.2 us                                                         | 20.3 us: 1.11x slower                                                            |
| regex_effbot             | 1.66 ms                                                         | 1.87 ms: 1.13x slower                                                            |
| gc_traversal             | 1.28 ms                                                         | 1.45 ms: 1.13x slower                                                            |
| asyncio_tcp              | 744 ms                                                          | 878 ms: 1.18x slower                                                             |
| async_generators         | 241 ms                                                          | 289 ms: 1.20x slower                                                             |
| telco                    | 4.83 ms                                                         | 5.87 ms: 1.22x slower                                                            |
| coverage                 | 46.6 ms                                                         | 498 ms: 10.70x slower                                                            |
| thrift                   | 902 us                                                          | 9.90 ms: 10.98x slower                                                           |
| Geometric mean           | (ref)                                                           | 1.15x faster                                                                     |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: unknown