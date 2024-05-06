# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 290 ms: 1.21x faster                                                                   |
| chameleon      | 9.44 ms                                                      | 7.24 ms: 1.30x faster                                                                  |
| docutils       | 3.41 sec                                                     | 2.98 sec: 1.15x faster                                                                 |
| html5lib       | 94.6 ms                                                      | 74.4 ms: 1.27x faster                                                                  |
| tornado_http   | 157 ms                                                       | 120 ms: 1.31x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.25x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 368 ms: 1.88x faster                                                                   |
| async_tree_memoization  | 819 ms                                                       | 462 ms: 1.77x faster                                                                   |
| async_tree_io           | 1.60 sec                                                     | 902 ms: 1.77x faster                                                                   |
| async_tree_cpu_io_mixed | 936 ms                                                       | 610 ms: 1.53x faster                                                                   |
| Geometric mean          | (ref)                                                        | 1.74x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 85.5 ms: 1.57x faster                                                                  |
| float          | 111 ms                                                       | 75.4 ms: 1.47x faster                                                                  |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.34x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                                   |
| regex_dna      | 261 ms                                                       | 243 ms: 1.07x faster                                                                   |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                                  |
| regex_effbot   | 3.09 ms                                                      | 3.57 ms: 1.16x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 307 us: 1.48x faster                                                                   |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                                  |
| unpickle_pure_python | 312 us                                                       | 227 us: 1.37x faster                                                                   |
| tomli_loads          | 2.92 sec                                                     | 2.23 sec: 1.30x faster                                                                 |
| xml_etree_process    | 75.9 ms                                                      | 58.6 ms: 1.29x faster                                                                  |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                                                  |
| xml_etree_generate   | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                                  |
| xml_etree_parse      | 160 ms                                                       | 147 ms: 1.09x faster                                                                   |
| xml_etree_iterparse  | 110 ms                                                       | 105 ms: 1.05x faster                                                                   |
| unpickle_list        | 4.65 us                                                      | 4.55 us: 1.02x faster                                                                  |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                                  |
| pickle_dict          | 29.5 us                                                      | 30.7 us: 1.04x slower                                                                  |
| pickle_list          | 4.12 us                                                      | 4.39 us: 1.07x slower                                                                  |
| unpickle             | 13.5 us                                                      | 14.9 us: 1.11x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| python_startup_no_site | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                                  |
| genshi_text    | 31.4 ms                                                      | 25.6 ms: 1.23x faster                                                                  |
| genshi_xml     | 63.3 ms                                                      | 54.8 ms: 1.16x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.27x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 118 us: 4.53x faster                                                                   |
| deltablue                | 7.50 ms                                                      | 3.43 ms: 2.18x faster                                                                  |
| asyncio_tcp              | 779 ms                                                       | 368 ms: 2.12x faster                                                                   |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                                 |
| raytrace                 | 489 ms                                                       | 251 ms: 1.95x faster                                                                   |
| async_tree_none          | 692 ms                                                       | 368 ms: 1.88x faster                                                                   |
| chaos                    | 109 ms                                                       | 58.2 ms: 1.87x faster                                                                  |
| pylint                   | 566 ms                                                       | 315 ms: 1.79x faster                                                                   |
| async_tree_memoization   | 819 ms                                                       | 462 ms: 1.77x faster                                                                   |
| async_tree_io            | 1.60 sec                                                     | 902 ms: 1.77x faster                                                                   |
| scimark_lu               | 167 ms                                                       | 95.6 ms: 1.74x faster                                                                  |
| logging_silent           | 167 ns                                                       | 96.7 ns: 1.73x faster                                                                  |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.72x faster                                                                  |
| crypto_pyaes             | 119 ms                                                       | 71.3 ms: 1.67x faster                                                                  |
| scimark_monte_carlo      | 107 ms                                                       | 64.7 ms: 1.66x faster                                                                  |
| comprehensions           | 26.7 us                                                      | 16.6 us: 1.60x faster                                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                                                  |
| nbody                    | 134 ms                                                       | 85.5 ms: 1.57x faster                                                                  |
| richards_super           | 90.6 ms                                                      | 58.6 ms: 1.55x faster                                                                  |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 610 ms: 1.53x faster                                                                   |
| go                       | 262 ms                                                       | 172 ms: 1.52x faster                                                                   |
| sqlglot_transpile        | 2.68 ms                                                      | 1.78 ms: 1.50x faster                                                                  |
| pickle_pure_python       | 455 us                                                       | 307 us: 1.48x faster                                                                   |
| spectral_norm            | 139 ms                                                       | 94.0 ms: 1.48x faster                                                                  |
| float                    | 111 ms                                                       | 75.4 ms: 1.47x faster                                                                  |
| pyflate                  | 733 ms                                                       | 502 ms: 1.46x faster                                                                   |
| hexiom                   | 9.42 ms                                                      | 6.45 ms: 1.46x faster                                                                  |
| richards                 | 75.1 ms                                                      | 52.0 ms: 1.44x faster                                                                  |
| mako                     | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                                  |
| scimark_sor              | 180 ms                                                       | 130 ms: 1.38x faster                                                                   |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                                  |
| unpickle_pure_python     | 312 us                                                       | 227 us: 1.37x faster                                                                   |
| logging_simple           | 8.88 us                                                      | 6.52 us: 1.36x faster                                                                  |
| deepcopy_memo            | 49.8 us                                                      | 36.9 us: 1.35x faster                                                                  |
| bench_mp_pool            | 6.37 ms                                                      | 4.73 ms: 1.35x faster                                                                  |
| coroutines               | 30.3 ms                                                      | 22.6 ms: 1.34x faster                                                                  |
| pprint_pformat           | 2.15 sec                                                     | 1.61 sec: 1.34x faster                                                                 |
| thrift                   | 1.18 ms                                                      | 880 us: 1.34x faster                                                                   |
| pprint_safe_repr         | 1.05 sec                                                     | 787 ms: 1.33x faster                                                                   |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                                   |
| logging_format           | 9.64 us                                                      | 7.27 us: 1.33x faster                                                                  |
| nqueens                  | 115 ms                                                       | 86.7 ms: 1.33x faster                                                                  |
| pycparser                | 1.67 sec                                                     | 1.27 sec: 1.32x faster                                                                 |
| tornado_http             | 157 ms                                                       | 120 ms: 1.31x faster                                                                   |
| chameleon                | 9.44 ms                                                      | 7.24 ms: 1.30x faster                                                                  |
| tomli_loads              | 2.92 sec                                                     | 2.23 sec: 1.30x faster                                                                 |
| xml_etree_process        | 75.9 ms                                                      | 58.6 ms: 1.29x faster                                                                  |
| html5lib                 | 94.6 ms                                                      | 74.4 ms: 1.27x faster                                                                  |
| fannkuch                 | 483 ms                                                       | 380 ms: 1.27x faster                                                                   |
| bench_thread_pool        | 1.14 ms                                                      | 900 us: 1.27x faster                                                                   |
| sympy_sum                | 193 ms                                                       | 155 ms: 1.24x faster                                                                   |
| deepcopy                 | 468 us                                                       | 377 us: 1.24x faster                                                                   |
| sqlglot_normalize        | 144 ms                                                       | 117 ms: 1.23x faster                                                                   |
| genshi_text              | 31.4 ms                                                      | 25.6 ms: 1.23x faster                                                                  |
| sympy_str                | 360 ms                                                       | 296 ms: 1.22x faster                                                                   |
| 2to3                     | 350 ms                                                       | 290 ms: 1.21x faster                                                                   |
| mypy2                    | 933 ms                                                       | 774 ms: 1.21x faster                                                                   |
| sqlglot_optimize         | 70.1 ms                                                      | 58.4 ms: 1.20x faster                                                                  |
| sympy_expand             | 600 ms                                                       | 500 ms: 1.20x faster                                                                   |
| dask                     | 472 ms                                                       | 393 ms: 1.20x faster                                                                   |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                                 |
| sympy_integrate          | 28.2 ms                                                      | 23.5 ms: 1.20x faster                                                                  |
| dulwich_log              | 81.1 ms                                                      | 67.8 ms: 1.20x faster                                                                  |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                                                  |
| async_generators         | 421 ms                                                       | 353 ms: 1.19x faster                                                                   |
| deepcopy_reduce          | 4.01 us                                                      | 3.42 us: 1.17x faster                                                                  |
| scimark_fft              | 361 ms                                                       | 309 ms: 1.17x faster                                                                   |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.38 ms: 1.16x faster                                                                  |
| genshi_xml               | 63.3 ms                                                      | 54.8 ms: 1.16x faster                                                                  |
| docutils                 | 3.41 sec                                                     | 2.98 sec: 1.15x faster                                                                 |
| aiohttp                  | 1.19 ms                                                      | 1.06 ms: 1.12x faster                                                                  |
| gunicorn                 | 1.16 ms                                                      | 1.04 ms: 1.12x faster                                                                  |
| pathlib                  | 21.4 ms                                                      | 19.2 ms: 1.11x faster                                                                  |
| sqlite_synth             | 2.99 us                                                      | 2.73 us: 1.10x faster                                                                  |
| xml_etree_generate       | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                                  |
| meteor_contest           | 138 ms                                                       | 127 ms: 1.09x faster                                                                   |
| xml_etree_parse          | 160 ms                                                       | 147 ms: 1.09x faster                                                                   |
| regex_dna                | 261 ms                                                       | 243 ms: 1.07x faster                                                                   |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                                  |
| json                     | 5.86 ms                                                      | 5.50 ms: 1.07x faster                                                                  |
| xml_etree_iterparse      | 110 ms                                                       | 105 ms: 1.05x faster                                                                   |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                                   |
| unpickle_list            | 4.65 us                                                      | 4.55 us: 1.02x faster                                                                  |
| pickle                   | 9.89 us                                                      | 10.3 us: 1.04x slower                                                                  |
| pickle_dict              | 29.5 us                                                      | 30.7 us: 1.04x slower                                                                  |
| pickle_list              | 4.12 us                                                      | 4.39 us: 1.07x slower                                                                  |
| create_gc_cycles         | 1.76 ms                                                      | 1.89 ms: 1.07x slower                                                                  |
| telco                    | 7.23 ms                                                      | 7.92 ms: 1.10x slower                                                                  |
| unpickle                 | 13.5 us                                                      | 14.9 us: 1.11x slower                                                                  |
| python_startup           | 11.5 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| regex_effbot             | 3.09 ms                                                      | 3.57 ms: 1.16x slower                                                                  |
| coverage                 | 63.3 ms                                                      | 82.1 ms: 1.30x slower                                                                  |
| gc_traversal             | 3.42 ms                                                      | 4.65 ms: 1.36x slower                                                                  |
| python_startup_no_site   | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                                  |
| Geometric mean           | (ref)                                                        | 1.30x faster                                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.10x