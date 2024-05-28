# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 881df50
- commit date: 2024-05-23
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                                            |
| chameleon      | 9.68 ms                                                | 6.99 ms: 1.38x faster                                                           |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                          |
| html5lib       | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                           |
| tornado_http   | 136 ms                                                 | 94.5 ms: 1.44x faster                                                           |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 382 ms: 1.91x faster                                                            |
| async_tree_memoization  | 870 ms                                                 | 460 ms: 1.89x faster                                                            |
| async_tree_io           | 1.77 sec                                               | 942 ms: 1.88x faster                                                            |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                            |
| Geometric mean          | (ref)                                                  | 1.83x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 94.3 ms: 1.63x faster                                                           |
| float          | 117 ms                                                 | 78.2 ms: 1.50x faster                                                           |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                            |
| regex_v8       | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                           |
| regex_dna      | 227 ms                                                 | 233 ms: 1.03x slower                                                            |
| regex_effbot   | 3.63 ms                                                | 3.94 ms: 1.09x slower                                                           |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 304 us: 1.59x faster                                                            |
| unpickle_pure_python | 331 us                                                 | 218 us: 1.51x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.19 sec: 1.44x faster                                                          |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                           |
| xml_etree_generate   | 99.4 ms                                                | 86.5 ms: 1.15x faster                                                           |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                            |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                           |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                           |
| unpickle_list        | 5.20 us                                                | 5.48 us: 1.05x slower                                                           |
| unpickle             | 14.4 us                                                | 15.6 us: 1.08x slower                                                           |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                           |
| pickle_dict          | 29.6 us                                                | 35.6 us: 1.20x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.4 ms: 1.41x faster                                                           |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.09x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.49x faster                                                           |
| genshi_text     | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                           |
| django_template | 48.2 ms                                                | 35.3 ms: 1.36x faster                                                           |
| genshi_xml      | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 163 us: 3.34x faster                                                            |
| generators               | 80.1 ms                                                | 29.3 ms: 2.73x faster                                                           |
| deltablue                | 7.91 ms                                                | 3.28 ms: 2.41x faster                                                           |
| async_tree_none          | 728 ms                                                 | 382 ms: 1.91x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 460 ms: 1.89x faster                                                            |
| chaos                    | 115 ms                                                 | 61.5 ms: 1.88x faster                                                           |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 942 ms: 1.88x faster                                                            |
| asyncio_tcp              | 922 ms                                                 | 503 ms: 1.83x faster                                                            |
| raytrace                 | 507 ms                                                 | 280 ms: 1.81x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 71.7 ms: 1.78x faster                                                           |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                                            |
| pylint                   | 551 ms                                                 | 318 ms: 1.74x faster                                                            |
| richards_super           | 94.7 ms                                                | 54.9 ms: 1.72x faster                                                           |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.72x faster                                                           |
| scimark_monte_carlo      | 118 ms                                                 | 70.3 ms: 1.68x faster                                                           |
| go                       | 240 ms                                                 | 144 ms: 1.66x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.29 ms: 1.65x faster                                                           |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.65x faster                                                           |
| richards                 | 79.3 ms                                                | 48.4 ms: 1.64x faster                                                           |
| nbody                    | 154 ms                                                 | 94.3 ms: 1.63x faster                                                           |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.59x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.62 ms: 1.59x faster                                                           |
| spectral_norm            | 170 ms                                                 | 107 ms: 1.59x faster                                                            |
| pyflate                  | 716 ms                                                 | 461 ms: 1.55x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 218 us: 1.51x faster                                                            |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.50x faster                                                            |
| float                    | 117 ms                                                 | 78.2 ms: 1.50x faster                                                           |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.49x faster                                                           |
| deepcopy_memo            | 58.5 us                                                | 39.7 us: 1.47x faster                                                           |
| coroutines               | 35.1 ms                                                | 23.9 ms: 1.47x faster                                                           |
| tornado_http             | 136 ms                                                 | 94.5 ms: 1.44x faster                                                           |
| tomli_loads              | 3.14 sec                                               | 2.19 sec: 1.44x faster                                                          |
| logging_simple           | 8.30 us                                                | 5.80 us: 1.43x faster                                                           |
| logging_format           | 9.09 us                                                | 6.41 us: 1.42x faster                                                           |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.4 ms: 1.41x faster                                                           |
| pprint_pformat           | 2.10 sec                                               | 1.49 sec: 1.41x faster                                                          |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                          |
| pprint_safe_repr         | 1.02 sec                                               | 730 ms: 1.39x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.99 ms: 1.38x faster                                                           |
| genshi_text              | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                           |
| django_template          | 48.2 ms                                                | 35.3 ms: 1.36x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                           |
| html5lib                 | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                           |
| fannkuch                 | 532 ms                                                 | 401 ms: 1.32x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                           |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                                            |
| deepcopy                 | 479 us                                                 | 367 us: 1.30x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                          |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                            |
| nqueens                  | 106 ms                                                 | 81.6 ms: 1.30x faster                                                           |
| genshi_xml               | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                           |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 65.6 ms: 1.29x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.25 us: 1.28x faster                                                           |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.27x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                                           |
| sqlglot_optimize         | 69.2 ms                                                | 54.8 ms: 1.26x faster                                                           |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                                            |
| pathlib                  | 20.5 ms                                                | 16.8 ms: 1.22x faster                                                           |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.31 ms: 1.22x faster                                                           |
| sympy_expand             | 566 ms                                                 | 469 ms: 1.21x faster                                                            |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                            |
| scimark_fft              | 466 ms                                                 | 391 ms: 1.19x faster                                                            |
| bench_thread_pool        | 986 us                                                 | 834 us: 1.18x faster                                                            |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                          |
| xml_etree_generate       | 99.4 ms                                                | 86.5 ms: 1.15x faster                                                           |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                            |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                           |
| mdp                      | 2.85 sec                                               | 2.63 sec: 1.08x faster                                                          |
| regex_v8                 | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                           |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                                           |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.98 us: 1.02x faster                                                           |
| async_generators         | 444 ms                                                 | 441 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.15 us: 1.01x slower                                                           |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.72 ms: 1.03x slower                                                           |
| regex_dna                | 227 ms                                                 | 233 ms: 1.03x slower                                                            |
| flaskblogging            | 8.58 ms                                                | 8.96 ms: 1.04x slower                                                           |
| unpickle_list            | 5.20 us                                                | 5.48 us: 1.05x slower                                                           |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.08x slower                                                           |
| regex_effbot             | 3.63 ms                                                | 3.94 ms: 1.09x slower                                                           |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                           |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                           |
| coverage                 | 79.4 ms                                                | 92.1 ms: 1.16x slower                                                           |
| telco                    | 7.27 ms                                                | 8.46 ms: 1.16x slower                                                           |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                           |
| pickle_dict              | 29.6 us                                                | 35.6 us: 1.20x slower                                                           |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                    |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240523-3.14.0a0-881df50/bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.11x