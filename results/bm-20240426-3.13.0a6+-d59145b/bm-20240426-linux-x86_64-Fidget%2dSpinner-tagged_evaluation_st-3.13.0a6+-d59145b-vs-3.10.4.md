# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: d59145b
- commit date: 2024-04-26
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                            |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 65.8 ms: 1.35x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.8 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 351 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 916 ms: 1.93x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 467 ms: 1.86x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.4 ms: 1.70x faster                                                            |
| float          | 117 ms                                                 | 77.8 ms: 1.50x faster                                                            |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.7 ms: 1.08x faster                                                            |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 300 us: 1.61x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 213 us: 1.55x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 86.3 ms: 1.15x faster                                                            |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.03 us: 1.01x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| pickle               | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.1 ms: 1.48x faster                                                            |
| django_template | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 159 us: 3.42x faster                                                             |
| generators               | 80.1 ms                                                | 29.3 ms: 2.74x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.16 ms: 2.50x faster                                                            |
| async_tree_none          | 728 ms                                                 | 351 ms: 2.07x faster                                                             |
| raytrace                 | 507 ms                                                 | 257 ms: 1.97x faster                                                             |
| chaos                    | 115 ms                                                 | 59.4 ms: 1.94x faster                                                            |
| logging_silent           | 190 ns                                                 | 98.0 ns: 1.94x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 916 ms: 1.93x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 467 ms: 1.86x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.81x faster                                                             |
| scimark_sor              | 220 ms                                                 | 121 ms: 1.81x faster                                                             |
| richards_super           | 94.7 ms                                                | 52.5 ms: 1.80x faster                                                            |
| pylint                   | 551 ms                                                 | 315 ms: 1.75x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 73.7 ms: 1.73x faster                                                            |
| go                       | 240 ms                                                 | 139 ms: 1.73x faster                                                             |
| richards                 | 79.3 ms                                                | 46.0 ms: 1.72x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 69.4 ms: 1.70x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.27 ms: 1.70x faster                                                            |
| nbody                    | 154 ms                                                 | 90.4 ms: 1.70x faster                                                            |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.70x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.25 ms: 1.66x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.58 ms: 1.63x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 300 us: 1.61x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 213 us: 1.55x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 37.9 us: 1.54x faster                                                            |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.52x faster                                                             |
| pyflate                  | 716 ms                                                 | 474 ms: 1.51x faster                                                             |
| float                    | 117 ms                                                 | 77.8 ms: 1.50x faster                                                            |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.50x faster                                                             |
| mako                     | 16.3 ms                                                | 11.1 ms: 1.48x faster                                                            |
| tornado_http             | 136 ms                                                 | 93.8 ms: 1.45x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.78 us: 1.44x faster                                                            |
| logging_format           | 9.09 us                                                | 6.36 us: 1.43x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                           |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                            |
| django_template          | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.38x faster                                                           |
| chameleon                | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 748 ms: 1.36x faster                                                             |
| fannkuch                 | 532 ms                                                 | 394 ms: 1.35x faster                                                             |
| html5lib                 | 88.9 ms                                                | 65.8 ms: 1.35x faster                                                            |
| deepcopy                 | 479 us                                                 | 356 us: 1.35x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.13 us: 1.33x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.89 ms: 1.32x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.32x faster                                                           |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.32x faster                                                             |
| thrift                   | 1.07 ms                                                | 815 us: 1.32x faster                                                             |
| nqueens                  | 106 ms                                                 | 80.7 ms: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 267 ms: 1.30x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                                            |
| sympy_sum                | 196 ms                                                 | 153 ms: 1.28x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 65.9 ms: 1.28x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 54.5 ms: 1.27x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                            |
| sympy_str                | 346 ms                                                 | 274 ms: 1.26x faster                                                             |
| scimark_fft              | 466 ms                                                 | 371 ms: 1.25x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                                            |
| mypy2                    | 894 ms                                                 | 729 ms: 1.23x faster                                                             |
| sympy_expand             | 566 ms                                                 | 463 ms: 1.22x faster                                                             |
| djangocms                | 38.4 us                                                | 31.5 us: 1.22x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.22x faster                                                            |
| dask                     | 441 ms                                                 | 365 ms: 1.21x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 827 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 86.3 ms: 1.15x faster                                                            |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                            |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| json                     | 5.69 ms                                                | 5.15 ms: 1.11x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.7 ms: 1.08x faster                                                            |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.76 sec: 1.03x faster                                                           |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.03 us: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                             |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                             |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| unpickle_list            | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.78 ms: 1.04x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                            |
| pickle                   | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| telco                    | 7.27 ms                                                | 8.50 ms: 1.17x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| coverage                 | 79.4 ms                                                | 96.5 ms: 1.22x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |

Benchmark hidden because not significant (2): bench_mp_pool, async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-d59145b/bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x