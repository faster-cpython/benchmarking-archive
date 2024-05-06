# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.74 ms: 1.44x faster                                                            |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 66.9 ms: 1.33x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 930 ms: 1.90x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 468 ms: 1.86x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.6 ms: 1.73x faster                                                            |
| float          | 117 ms                                                 | 78.1 ms: 1.50x faster                                                            |
| pidigits       | 191 ms                                                 | 211 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                            |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 300 us: 1.61x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 221 us: 1.49x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                             |
| json_loads           | 31.2 us                                                | 29.0 us: 1.08x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.90 us: 1.04x faster                                                            |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 33.7 us: 1.14x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                            |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.74x faster                                                             |
| generators               | 80.1 ms                                                | 29.3 ms: 2.73x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.13 ms: 2.53x faster                                                            |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                             |
| raytrace                 | 507 ms                                                 | 259 ms: 1.96x faster                                                             |
| chaos                    | 115 ms                                                 | 59.3 ms: 1.95x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 930 ms: 1.90x faster                                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 468 ms: 1.86x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                             |
| scimark_sor              | 220 ms                                                 | 122 ms: 1.80x faster                                                             |
| richards_super           | 94.7 ms                                                | 52.7 ms: 1.80x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.4 us: 1.75x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 73.1 ms: 1.75x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 67.6 ms: 1.75x faster                                                            |
| nbody                    | 154 ms                                                 | 88.6 ms: 1.73x faster                                                            |
| go                       | 240 ms                                                 | 139 ms: 1.73x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.70x faster                                                            |
| richards                 | 79.3 ms                                                | 46.7 ms: 1.70x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.23 ms: 1.67x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.58 ms: 1.63x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 300 us: 1.61x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 36.7 us: 1.59x faster                                                            |
| pyflate                  | 716 ms                                                 | 451 ms: 1.59x faster                                                             |
| scimark_lu               | 176 ms                                                 | 113 ms: 1.56x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.55x faster                                                            |
| spectral_norm            | 170 ms                                                 | 111 ms: 1.53x faster                                                             |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                            |
| float                    | 117 ms                                                 | 78.1 ms: 1.50x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 221 us: 1.49x faster                                                             |
| logging_simple           | 8.30 us                                                | 5.70 us: 1.46x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.74 ms: 1.44x faster                                                            |
| logging_format           | 9.09 us                                                | 6.34 us: 1.43x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                                           |
| fannkuch                 | 532 ms                                                 | 389 ms: 1.37x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 745 ms: 1.37x faster                                                             |
| deepcopy                 | 479 us                                                 | 354 us: 1.35x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                            |
| html5lib                 | 88.9 ms                                                | 66.9 ms: 1.33x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.89 ms: 1.32x faster                                                            |
| nqueens                  | 106 ms                                                 | 80.2 ms: 1.32x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.31x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                             |
| thrift                   | 1.07 ms                                                | 829 us: 1.29x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.2 ms: 1.28x faster                                                            |
| scimark_fft              | 466 ms                                                 | 366 ms: 1.27x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.0 ms: 1.26x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.1 ms: 1.26x faster                                                            |
| sympy_str                | 346 ms                                                 | 278 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                            |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| sympy_expand             | 566 ms                                                 | 469 ms: 1.21x faster                                                             |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 829 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.17x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                            |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.10x faster                                                             |
| pathlib                  | 20.5 ms                                                | 18.7 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                             |
| json_loads               | 31.2 us                                                | 29.0 us: 1.08x faster                                                            |
| json                     | 5.69 ms                                                | 5.32 ms: 1.07x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| pickle_list              | 5.08 us                                                | 4.90 us: 1.04x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.76 sec: 1.03x faster                                                           |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                             |
| async_generators         | 444 ms                                                 | 446 ms: 1.00x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 565 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.78 ms: 1.04x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pidigits                 | 191 ms                                                 | 211 ms: 1.11x slower                                                             |
| pickle_dict              | 29.6 us                                                | 33.7 us: 1.14x slower                                                            |
| telco                    | 7.27 ms                                                | 8.46 ms: 1.17x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.5 ms: 1.24x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.09x