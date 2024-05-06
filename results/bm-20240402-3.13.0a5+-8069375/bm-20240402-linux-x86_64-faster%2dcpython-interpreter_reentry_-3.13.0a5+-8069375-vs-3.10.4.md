# Results vs. 3.10.4

- fork: faster-cpython
- ref: interpreter_reentry_
- machine: linux-x86_64
- commit hash: 8069375
- commit date: 2024-04-02
- overall geometric mean: 1.36x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.81 ms: 1.42x faster                                                            |
| docutils       | 3.30 sec                                               | 2.77 sec: 1.19x faster                                                           |
| html5lib       | 88.9 ms                                                | 66.7 ms: 1.33x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.7 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 438 ms: 1.98x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 900 ms: 1.96x faster                                                             |
| async_tree_none         | 728 ms                                                 | 383 ms: 1.90x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 599 ms: 1.70x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.7 ms: 1.75x faster                                                            |
| float          | 117 ms                                                 | 76.6 ms: 1.53x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.39x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 133 ms: 1.42x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                            |
| regex_dna      | 227 ms                                                 | 220 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 301 us: 1.61x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 218 us: 1.52x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.22 sec: 1.41x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 59.5 ms: 1.33x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 86.4 ms: 1.15x faster                                                            |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.94 us: 1.03x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.31 us: 1.02x slower                                                            |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| unpickle             | 14.4 us                                                | 16.2 us: 1.13x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.0 us: 1.15x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.03 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                            |
| django_template | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                            |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 52.5 ms: 1.26x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.75x faster                                                             |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.17 ms: 2.49x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 438 ms: 1.98x faster                                                             |
| pylint                   | 551 ms                                                 | 280 ms: 1.97x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 900 ms: 1.96x faster                                                             |
| raytrace                 | 507 ms                                                 | 261 ms: 1.94x faster                                                             |
| chaos                    | 115 ms                                                 | 59.8 ms: 1.93x faster                                                            |
| async_tree_none          | 728 ms                                                 | 383 ms: 1.90x faster                                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 500 ms: 1.84x faster                                                             |
| richards_super           | 94.7 ms                                                | 51.8 ms: 1.83x faster                                                            |
| scimark_sor              | 220 ms                                                 | 121 ms: 1.81x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 66.8 ms: 1.77x faster                                                            |
| nbody                    | 154 ms                                                 | 87.7 ms: 1.75x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.4 us: 1.75x faster                                                            |
| richards                 | 79.3 ms                                                | 45.6 ms: 1.74x faster                                                            |
| go                       | 240 ms                                                 | 139 ms: 1.72x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 74.4 ms: 1.72x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.09 ms: 1.71x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.27 ms: 1.71x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 599 ms: 1.70x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 301 us: 1.61x faster                                                             |
| spectral_norm            | 170 ms                                                 | 109 ms: 1.57x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                            |
| scimark_lu               | 176 ms                                                 | 113 ms: 1.55x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 37.7 us: 1.55x faster                                                            |
| float                    | 117 ms                                                 | 76.6 ms: 1.53x faster                                                            |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 218 us: 1.52x faster                                                             |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                            |
| tornado_http             | 136 ms                                                 | 94.7 ms: 1.44x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.81 ms: 1.42x faster                                                            |
| regex_compile            | 188 ms                                                 | 133 ms: 1.42x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.22 sec: 1.41x faster                                                           |
| logging_format           | 9.09 us                                                | 6.45 us: 1.41x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.90 us: 1.41x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.61 ms: 1.40x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.83 sec: 1.40x faster                                                           |
| django_template          | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                                           |
| deepcopy                 | 479 us                                                 | 350 us: 1.37x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 747 ms: 1.36x faster                                                             |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.34x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.13 us: 1.33x faster                                                            |
| html5lib                 | 88.9 ms                                                | 66.7 ms: 1.33x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 59.5 ms: 1.33x faster                                                            |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 108 ms: 1.32x faster                                                             |
| nqueens                  | 106 ms                                                 | 80.7 ms: 1.31x faster                                                            |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| scimark_fft              | 466 ms                                                 | 359 ms: 1.30x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                                            |
| unpack_sequence          | 60.0 ns                                                | 46.8 ns: 1.28x faster                                                            |
| sympy_sum                | 196 ms                                                 | 153 ms: 1.28x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 54.5 ms: 1.27x faster                                                            |
| sympy_str                | 346 ms                                                 | 274 ms: 1.26x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 66.8 ms: 1.26x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 52.5 ms: 1.26x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.22x faster                                                            |
| sympy_expand             | 566 ms                                                 | 463 ms: 1.22x faster                                                             |
| mypy2                    | 894 ms                                                 | 734 ms: 1.22x faster                                                             |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                                            |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                            |
| docutils                 | 3.30 sec                                               | 2.77 sec: 1.19x faster                                                           |
| bench_thread_pool        | 986 us                                                 | 828 us: 1.19x faster                                                             |
| xml_etree_generate       | 99.4 ms                                                | 86.4 ms: 1.15x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.56 sec: 1.11x faster                                                           |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.10x faster                                                             |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                             |
| json                     | 5.69 ms                                                | 5.29 ms: 1.08x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| regex_dna                | 227 ms                                                 | 220 ms: 1.03x faster                                                             |
| pickle_list              | 5.08 us                                                | 4.94 us: 1.03x faster                                                            |
| gc_traversal             | 3.62 ms                                                | 3.57 ms: 1.01x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.31 us: 1.02x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.67 ms: 1.03x slower                                                            |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| unpickle                 | 14.4 us                                                | 16.2 us: 1.13x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.0 us: 1.15x slower                                                            |
| telco                    | 7.27 ms                                                | 8.54 ms: 1.18x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.3 ms: 1.22x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 9.03 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.36x faster                                                                     |

Benchmark hidden because not significant (2): async_generators, regex_effbot
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-8069375/bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.09x