# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 250 ms: 1.06x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.70 ms: 1.13x faster                                                           |
| html5lib       | 52.1 ms                                                         | 46.3 ms: 1.12x faster                                                           |
| tornado_http   | 118 ms                                                          | 107 ms: 1.10x faster                                                            |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 483 ms: 1.91x faster                                                            |
| async_tree_io           | 940 ms                                                          | 534 ms: 1.76x faster                                                            |
| async_tree_none         | 394 ms                                                          | 229 ms: 1.72x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 277 ms: 1.68x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.77x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| float          | 69.6 ms                                                         | 57.4 ms: 1.21x faster                                                           |
| Geometric mean | (ref)                                                           | 1.46x faster                                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 120 ms: 1.08x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                           |
| regex_compile  | 117 ms                                                          | 121 ms: 1.03x slower                                                            |
| regex_effbot   | 1.66 ms                                                         | 1.93 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.89 ms: 1.43x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 224 us: 1.25x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.60 sec: 1.19x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 104 ms: 1.16x faster                                                            |
| xml_etree_process    | 48.1 ms                                                         | 43.2 ms: 1.11x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.5 us: 1.09x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 174 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 67.0 ms: 1.06x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| pickle               | 7.83 us                                                         | 7.76 us: 1.01x faster                                                           |
| unpickle             | 9.82 us                                                         | 9.90 us: 1.01x slower                                                           |
| unpickle_list        | 2.98 us                                                         | 3.02 us: 1.01x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.32 us: 1.03x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.5 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.5 ms: 1.02x faster                                                           |
| python_startup_no_site | 18.1 ms                                                         | 18.8 ms: 1.04x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.76 ms: 1.17x faster                                                           |
| django_template | 36.0 ms                                                         | 32.0 ms: 1.12x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 20.5 ms: 1.03x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 47.3 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                           | 1.07x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 147 us: 2.69x faster                                                            |
| pidigits                 | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 483 ms: 1.91x faster                                                            |
| async_tree_io            | 940 ms                                                          | 534 ms: 1.76x faster                                                            |
| async_tree_none          | 394 ms                                                          | 229 ms: 1.72x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 277 ms: 1.68x faster                                                            |
| pylint                   | 384 ms                                                          | 236 ms: 1.63x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 61.0 ns: 1.61x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.68 ms: 1.50x faster                                                           |
| richards_super           | 49.9 ms                                                         | 34.9 ms: 1.43x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.89 ms: 1.43x faster                                                           |
| raytrace                 | 303 ms                                                          | 214 ms: 1.41x faster                                                            |
| crypto_pyaes             | 81.3 ms                                                         | 57.6 ms: 1.41x faster                                                           |
| chaos                    | 74.4 ms                                                         | 53.8 ms: 1.38x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 972 us: 1.37x faster                                                            |
| generators               | 31.6 ms                                                         | 23.8 ms: 1.33x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.21 ms: 1.31x faster                                                           |
| richards                 | 40.3 ms                                                         | 31.2 ms: 1.29x faster                                                           |
| comprehensions           | 17.7 us                                                         | 14.1 us: 1.26x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 224 us: 1.25x faster                                                            |
| pycparser                | 1.04 sec                                                        | 843 ms: 1.24x faster                                                            |
| scimark_sor              | 115 ms                                                          | 93.2 ms: 1.23x faster                                                           |
| go                       | 146 ms                                                          | 118 ms: 1.23x faster                                                            |
| pyflate                  | 422 ms                                                          | 344 ms: 1.23x faster                                                            |
| float                    | 69.6 ms                                                         | 57.4 ms: 1.21x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.60 sec: 1.19x faster                                                          |
| scimark_monte_carlo      | 61.9 ms                                                         | 52.4 ms: 1.18x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.76 ms: 1.17x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 104 ms: 1.16x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 25.8 us: 1.15x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 2.01 us: 1.14x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.8 ms: 1.14x faster                                                           |
| chameleon                | 6.42 ms                                                         | 5.70 ms: 1.13x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 46.3 ms: 1.12x faster                                                           |
| django_template          | 36.0 ms                                                         | 32.0 ms: 1.12x faster                                                           |
| json                     | 4.76 ms                                                         | 4.27 ms: 1.11x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 43.2 ms: 1.11x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 78.4 ms: 1.11x faster                                                           |
| fannkuch                 | 317 ms                                                          | 286 ms: 1.11x faster                                                            |
| pprint_pformat           | 1.37 sec                                                        | 1.24 sec: 1.11x faster                                                          |
| tornado_http             | 118 ms                                                          | 107 ms: 1.10x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 1.02 ms: 1.09x faster                                                           |
| mdp                      | 1.83 sec                                                        | 1.67 sec: 1.09x faster                                                          |
| scimark_lu               | 89.8 ms                                                         | 82.1 ms: 1.09x faster                                                           |
| json_loads               | 22.4 us                                                         | 20.5 us: 1.09x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 174 us: 1.09x faster                                                            |
| pprint_safe_repr         | 658 ms                                                          | 605 ms: 1.09x faster                                                            |
| regex_dna                | 131 ms                                                          | 120 ms: 1.08x faster                                                            |
| sympy_sum                | 122 ms                                                          | 113 ms: 1.08x faster                                                            |
| hexiom                   | 6.13 ms                                                         | 5.68 ms: 1.08x faster                                                           |
| deepcopy                 | 310 us                                                          | 291 us: 1.07x faster                                                            |
| 2to3                     | 265 ms                                                          | 250 ms: 1.06x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 67.0 ms: 1.06x faster                                                           |
| sqlglot_normalize        | 230 ms                                                          | 220 ms: 1.05x faster                                                            |
| sympy_integrate          | 16.6 ms                                                         | 16.0 ms: 1.04x faster                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 43.0 ms: 1.04x faster                                                           |
| sympy_str                | 229 ms                                                          | 223 ms: 1.03x faster                                                            |
| deepcopy_reduce          | 2.68 us                                                         | 2.61 us: 1.03x faster                                                           |
| genshi_text              | 21.0 ms                                                         | 20.5 ms: 1.03x faster                                                           |
| python_startup           | 22.9 ms                                                         | 22.5 ms: 1.02x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 78.9 ms: 1.01x faster                                                           |
| pickle                   | 7.83 us                                                         | 7.76 us: 1.01x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 79.5 ms: 1.01x faster                                                           |
| scimark_fft              | 216 ms                                                          | 214 ms: 1.01x faster                                                            |
| sympy_expand             | 391 ms                                                          | 393 ms: 1.01x slower                                                            |
| unpickle                 | 9.82 us                                                         | 9.90 us: 1.01x slower                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.26 ms: 1.01x slower                                                           |
| unpickle_list            | 2.98 us                                                         | 3.02 us: 1.01x slower                                                           |
| genshi_xml               | 46.6 ms                                                         | 47.3 ms: 1.02x slower                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 17.3 sec: 1.02x slower                                                          |
| pickle_list              | 3.22 us                                                         | 3.32 us: 1.03x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                           |
| regex_compile            | 117 ms                                                          | 121 ms: 1.03x slower                                                            |
| python_startup_no_site   | 18.1 ms                                                         | 18.8 ms: 1.04x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.47 us: 1.07x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 750 us: 1.08x slower                                                            |
| bench_mp_pool            | 66.4 ms                                                         | 71.7 ms: 1.08x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.90 us: 1.08x slower                                                           |
| asyncio_tcp              | 744 ms                                                          | 807 ms: 1.08x slower                                                            |
| pathlib                  | 81.2 ms                                                         | 89.7 ms: 1.10x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.5 us: 1.12x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.45 ms: 1.13x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.93 ms: 1.16x slower                                                           |
| telco                    | 4.83 ms                                                         | 5.67 ms: 1.17x slower                                                           |
| async_generators         | 241 ms                                                          | 297 ms: 1.23x slower                                                            |
| coverage                 | 46.6 ms                                                         | 418 ms: 8.97x slower                                                            |
| thrift                   | 902 us                                                          | 11.6 ms: 12.82x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.08x faster                                                                    |

Benchmark hidden because not significant (2): nbody, docutils
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown