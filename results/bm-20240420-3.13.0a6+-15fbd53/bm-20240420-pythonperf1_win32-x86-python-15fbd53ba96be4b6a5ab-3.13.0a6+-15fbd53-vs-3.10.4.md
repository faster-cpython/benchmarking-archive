# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 229 ms: 1.16x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.69 ms: 1.13x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.79 sec: 1.09x faster                                                          |
| html5lib       | 52.1 ms                                                         | 42.2 ms: 1.23x faster                                                           |
| tornado_http   | 118 ms                                                          | 92.8 ms: 1.27x faster                                                           |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 488 ms: 1.89x faster                                                            |
| async_tree_io           | 940 ms                                                          | 523 ms: 1.80x faster                                                            |
| async_tree_none         | 394 ms                                                          | 225 ms: 1.75x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 270 ms: 1.73x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.79x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 196 ms: 2.56x faster                                                            |
| float          | 69.6 ms                                                         | 54.0 ms: 1.29x faster                                                           |
| nbody          | 79.1 ms                                                         | 80.7 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                           | 1.48x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 94.7 ms: 1.23x faster                                                           |
| regex_dna      | 131 ms                                                          | 124 ms: 1.06x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 15.8 ms: 1.01x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.92 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.76 ms: 1.45x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 199 us: 1.41x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 137 us: 1.38x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.61 sec: 1.19x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 42.2 ms: 1.14x faster                                                           |
| json_loads           | 22.4 us                                                         | 19.9 us: 1.12x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.93 us: 1.02x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 60.6 ms: 1.02x faster                                                           |
| unpickle             | 9.82 us                                                         | 9.77 us: 1.01x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.20 us: 1.00x faster                                                           |
| pickle_dict          | 18.2 us                                                         | 20.0 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.9 ms                                                         | 21.8 ms: 1.05x faster                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.73 ms: 1.35x faster                                                           |
| django_template | 36.0 ms                                                         | 28.8 ms: 1.25x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 18.6 ms: 1.13x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 41.4 ms: 1.12x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.21x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 89.8 us: 4.40x faster                                                           |
| pidigits                 | 502 ms                                                          | 196 ms: 2.56x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.13 ms: 1.89x faster                                                           |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 488 ms: 1.89x faster                                                            |
| async_tree_io            | 940 ms                                                          | 523 ms: 1.80x faster                                                            |
| pylint                   | 384 ms                                                          | 217 ms: 1.77x faster                                                            |
| async_tree_none          | 394 ms                                                          | 225 ms: 1.75x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 270 ms: 1.73x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 58.0 ns: 1.69x faster                                                           |
| raytrace                 | 303 ms                                                          | 182 ms: 1.66x faster                                                            |
| chaos                    | 74.4 ms                                                         | 45.0 ms: 1.65x faster                                                           |
| comprehensions           | 17.7 us                                                         | 11.6 us: 1.54x faster                                                           |
| richards_super           | 49.9 ms                                                         | 32.7 ms: 1.53x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 873 us: 1.52x faster                                                            |
| go                       | 146 ms                                                          | 97.2 ms: 1.50x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 60.2 ms: 1.49x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 55.5 ms: 1.46x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.76 ms: 1.45x faster                                                           |
| scimark_sor              | 115 ms                                                          | 79.5 ms: 1.45x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.10 ms: 1.43x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 4.29 ms: 1.43x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 199 us: 1.41x faster                                                            |
| generators               | 31.6 ms                                                         | 22.4 ms: 1.41x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 137 us: 1.38x faster                                                            |
| pycparser                | 1.04 sec                                                        | 758 ms: 1.37x faster                                                            |
| richards                 | 40.3 ms                                                         | 29.4 ms: 1.37x faster                                                           |
| pyflate                  | 422 ms                                                          | 308 ms: 1.37x faster                                                            |
| mako                     | 9.10 ms                                                         | 6.73 ms: 1.35x faster                                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 46.0 ms: 1.35x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 22.8 us: 1.30x faster                                                           |
| float                    | 69.6 ms                                                         | 54.0 ms: 1.29x faster                                                           |
| tornado_http             | 118 ms                                                          | 92.8 ms: 1.27x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 69.4 ms: 1.25x faster                                                           |
| django_template          | 36.0 ms                                                         | 28.8 ms: 1.25x faster                                                           |
| coroutines               | 17.9 ms                                                         | 14.5 ms: 1.24x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 42.2 ms: 1.23x faster                                                           |
| regex_compile            | 117 ms                                                          | 94.7 ms: 1.23x faster                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.13 sec: 1.21x faster                                                          |
| sympy_sum                | 122 ms                                                          | 101 ms: 1.21x faster                                                            |
| spectral_norm            | 80.2 ms                                                         | 66.8 ms: 1.20x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.92 us: 1.19x faster                                                           |
| pprint_safe_repr         | 658 ms                                                          | 553 ms: 1.19x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.61 sec: 1.19x faster                                                          |
| deepcopy                 | 310 us                                                          | 263 us: 1.18x faster                                                            |
| sympy_integrate          | 16.6 ms                                                         | 14.2 ms: 1.17x faster                                                           |
| json                     | 4.76 ms                                                         | 4.07 ms: 1.17x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.30 us: 1.17x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 639 ms: 1.16x faster                                                            |
| fannkuch                 | 317 ms                                                          | 273 ms: 1.16x faster                                                            |
| 2to3                     | 265 ms                                                          | 229 ms: 1.16x faster                                                            |
| sqlglot_optimize         | 44.7 ms                                                         | 38.7 ms: 1.15x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 971 us: 1.15x faster                                                            |
| sqlglot_normalize        | 230 ms                                                          | 201 ms: 1.15x faster                                                            |
| sympy_str                | 229 ms                                                          | 200 ms: 1.15x faster                                                            |
| xml_etree_process        | 48.1 ms                                                         | 42.2 ms: 1.14x faster                                                           |
| genshi_text              | 21.0 ms                                                         | 18.6 ms: 1.13x faster                                                           |
| chameleon                | 6.42 ms                                                         | 5.69 ms: 1.13x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 41.4 ms: 1.12x faster                                                           |
| json_loads               | 22.4 us                                                         | 19.9 us: 1.12x faster                                                           |
| sympy_expand             | 391 ms                                                          | 348 ms: 1.12x faster                                                            |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.67 sec: 1.09x faster                                                          |
| docutils                 | 1.95 sec                                                        | 1.79 sec: 1.09x faster                                                          |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 75.5 ms: 1.06x faster                                                           |
| regex_dna                | 131 ms                                                          | 124 ms: 1.06x faster                                                            |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.07 ms: 1.05x faster                                                           |
| python_startup           | 22.9 ms                                                         | 21.8 ms: 1.05x faster                                                           |
| scimark_fft              | 216 ms                                                          | 206 ms: 1.05x faster                                                            |
| unpickle_list            | 2.98 us                                                         | 2.93 us: 1.02x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 60.6 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| unpickle                 | 9.82 us                                                         | 9.77 us: 1.01x faster                                                           |
| pickle_list              | 3.22 us                                                         | 3.20 us: 1.00x faster                                                           |
| regex_v8                 | 15.8 ms                                                         | 15.8 ms: 1.01x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.04 us: 1.02x slower                                                           |
| nbody                    | 79.1 ms                                                         | 80.7 ms: 1.02x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 68.1 ms: 1.03x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.48 us: 1.03x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 84.2 ms: 1.04x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 728 us: 1.05x slower                                                            |
| pickle_dict              | 18.2 us                                                         | 20.0 us: 1.10x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.92 ms: 1.16x slower                                                           |
| async_generators         | 241 ms                                                          | 298 ms: 1.23x slower                                                            |
| telco                    | 4.83 ms                                                         | 6.25 ms: 1.29x slower                                                           |
| coverage                 | 46.6 ms                                                         | 489 ms: 10.50x slower                                                           |
| thrift                   | 902 us                                                          | 9.59 ms: 10.63x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.17x faster                                                                    |

Benchmark hidden because not significant (2): python_startup_no_site, pickle
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: unknown