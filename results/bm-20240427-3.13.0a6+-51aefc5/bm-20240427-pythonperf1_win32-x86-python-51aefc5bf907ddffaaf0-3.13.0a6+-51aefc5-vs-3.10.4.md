# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 231 ms: 1.15x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.56 ms: 1.16x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.81 sec: 1.08x faster                                                          |
| html5lib       | 52.1 ms                                                         | 43.3 ms: 1.20x faster                                                           |
| tornado_http   | 118 ms                                                          | 104 ms: 1.14x faster                                                            |
| Geometric mean | (ref)                                                           | 1.14x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 468 ms: 1.97x faster                                                            |
| async_tree_io           | 940 ms                                                          | 517 ms: 1.82x faster                                                            |
| async_tree_none         | 394 ms                                                          | 221 ms: 1.78x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 267 ms: 1.75x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.83x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 200 ms: 2.51x faster                                                            |
| float          | 69.6 ms                                                         | 52.7 ms: 1.32x faster                                                           |
| nbody          | 79.1 ms                                                         | 80.9 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                           | 1.48x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 95.0 ms: 1.23x faster                                                           |
| regex_dna      | 131 ms                                                          | 121 ms: 1.08x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.4 ms: 1.04x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.94 ms: 1.17x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.75 ms: 1.46x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 202 us: 1.39x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 138 us: 1.37x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 103 ms: 1.17x faster                                                            |
| xml_etree_process    | 48.1 ms                                                         | 42.0 ms: 1.15x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.2 us: 1.11x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.5 ms: 1.08x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 59.8 ms: 1.03x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.92 us: 1.02x faster                                                           |
| pickle               | 7.83 us                                                         | 7.92 us: 1.01x slower                                                           |
| unpickle             | 9.82 us                                                         | 9.94 us: 1.01x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.59 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.4 ms: 1.02x faster                                                           |
| python_startup_no_site | 18.1 ms                                                         | 18.7 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.87 ms: 1.33x faster                                                           |
| django_template | 36.0 ms                                                         | 28.1 ms: 1.28x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 18.2 ms: 1.15x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 42.8 ms: 1.09x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.21x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 131 us: 3.02x faster                                                            |
| pidigits                 | 502 ms                                                          | 200 ms: 2.51x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 468 ms: 1.97x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.15 ms: 1.88x faster                                                           |
| async_tree_io            | 940 ms                                                          | 517 ms: 1.82x faster                                                            |
| async_tree_none          | 394 ms                                                          | 221 ms: 1.78x faster                                                            |
| pylint                   | 384 ms                                                          | 218 ms: 1.76x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 267 ms: 1.75x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 58.1 ns: 1.68x faster                                                           |
| chaos                    | 74.4 ms                                                         | 44.8 ms: 1.66x faster                                                           |
| raytrace                 | 303 ms                                                          | 184 ms: 1.65x faster                                                            |
| comprehensions           | 17.7 us                                                         | 11.7 us: 1.52x faster                                                           |
| go                       | 146 ms                                                          | 96.2 ms: 1.51x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 883 us: 1.51x faster                                                            |
| richards_super           | 49.9 ms                                                         | 33.4 ms: 1.49x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 60.2 ms: 1.49x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 55.1 ms: 1.47x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 4.18 ms: 1.47x faster                                                           |
| scimark_sor              | 115 ms                                                          | 78.5 ms: 1.47x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.75 ms: 1.46x faster                                                           |
| generators               | 31.6 ms                                                         | 22.1 ms: 1.43x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.12 ms: 1.42x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 202 us: 1.39x faster                                                            |
| unpickle_pure_python     | 189 us                                                          | 138 us: 1.37x faster                                                            |
| richards                 | 40.3 ms                                                         | 29.8 ms: 1.35x faster                                                           |
| pycparser                | 1.04 sec                                                        | 773 ms: 1.35x faster                                                            |
| pyflate                  | 422 ms                                                          | 314 ms: 1.34x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 46.1 ms: 1.34x faster                                                           |
| mako                     | 9.10 ms                                                         | 6.87 ms: 1.33x faster                                                           |
| float                    | 69.6 ms                                                         | 52.7 ms: 1.32x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 66.0 ms: 1.32x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 22.6 us: 1.31x faster                                                           |
| django_template          | 36.0 ms                                                         | 28.1 ms: 1.28x faster                                                           |
| regex_compile            | 117 ms                                                          | 95.0 ms: 1.23x faster                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.12 sec: 1.22x faster                                                          |
| html5lib                 | 52.1 ms                                                         | 43.3 ms: 1.20x faster                                                           |
| pprint_safe_repr         | 658 ms                                                          | 549 ms: 1.20x faster                                                            |
| sympy_sum                | 122 ms                                                          | 102 ms: 1.20x faster                                                            |
| sqlglot_normalize        | 230 ms                                                          | 193 ms: 1.19x faster                                                            |
| spectral_norm            | 80.2 ms                                                         | 67.9 ms: 1.18x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.94 us: 1.18x faster                                                           |
| fannkuch                 | 317 ms                                                          | 270 ms: 1.17x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| xml_etree_parse          | 120 ms                                                          | 103 ms: 1.17x faster                                                            |
| sqlglot_optimize         | 44.7 ms                                                         | 38.3 ms: 1.17x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 14.4 ms: 1.16x faster                                                           |
| chameleon                | 6.42 ms                                                         | 5.56 ms: 1.16x faster                                                           |
| genshi_text              | 21.0 ms                                                         | 18.2 ms: 1.15x faster                                                           |
| deepcopy                 | 310 us                                                          | 269 us: 1.15x faster                                                            |
| 2to3                     | 265 ms                                                          | 231 ms: 1.15x faster                                                            |
| json                     | 4.76 ms                                                         | 4.14 ms: 1.15x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 42.0 ms: 1.15x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.7 ms: 1.14x faster                                                           |
| tornado_http             | 118 ms                                                          | 104 ms: 1.14x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.61 sec: 1.13x faster                                                          |
| sympy_str                | 229 ms                                                          | 202 ms: 1.13x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 995 us: 1.13x faster                                                            |
| sympy_expand             | 391 ms                                                          | 351 ms: 1.11x faster                                                            |
| json_loads               | 22.4 us                                                         | 20.2 us: 1.11x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 42.8 ms: 1.09x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.47 us: 1.09x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 2.99 ms: 1.08x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.5 ms: 1.08x faster                                                           |
| regex_dna                | 131 ms                                                          | 121 ms: 1.08x faster                                                            |
| docutils                 | 1.95 sec                                                        | 1.81 sec: 1.08x faster                                                          |
| meteor_contest           | 80.0 ms                                                         | 74.4 ms: 1.08x faster                                                           |
| logging_format           | 7.91 us                                                         | 7.66 us: 1.03x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 59.8 ms: 1.03x faster                                                           |
| python_startup           | 22.9 ms                                                         | 22.4 ms: 1.02x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.92 us: 1.02x faster                                                           |
| logging_simple           | 7.29 us                                                         | 7.13 us: 1.02x faster                                                           |
| scimark_fft              | 216 ms                                                          | 212 ms: 1.02x faster                                                            |
| pickle                   | 7.83 us                                                         | 7.92 us: 1.01x slower                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 17.2 sec: 1.01x slower                                                          |
| unpickle                 | 9.82 us                                                         | 9.94 us: 1.01x slower                                                           |
| nbody                    | 79.1 ms                                                         | 80.9 ms: 1.02x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 18.7 ms: 1.03x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.4 ms: 1.04x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 70.0 ms: 1.06x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 743 us: 1.07x slower                                                            |
| asyncio_tcp              | 744 ms                                                          | 812 ms: 1.09x slower                                                            |
| pathlib                  | 81.2 ms                                                         | 88.7 ms: 1.09x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| pickle_list              | 3.22 us                                                         | 3.59 us: 1.12x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.45 ms: 1.13x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.94 ms: 1.17x slower                                                           |
| async_generators         | 241 ms                                                          | 283 ms: 1.17x slower                                                            |
| telco                    | 4.83 ms                                                         | 5.98 ms: 1.24x slower                                                           |
| coverage                 | 46.6 ms                                                         | 399 ms: 8.56x slower                                                            |
| thrift                   | 902 us                                                          | 9.80 ms: 10.86x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.16x faster                                                                    |
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: unknown