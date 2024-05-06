# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 198ceb6
- commit date: 2024-04-03
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 266 ms: 1.31x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.86 ms: 1.41x faster                                                            |
| docutils       | 3.30 sec                                               | 2.78 sec: 1.19x faster                                                           |
| html5lib       | 88.9 ms                                                | 66.1 ms: 1.34x faster                                                            |
| tornado_http   | 136 ms                                                 | 95.6 ms: 1.43x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 378 ms: 1.93x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 463 ms: 1.88x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 594 ms: 1.71x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 80.8 ms: 1.45x faster                                                            |
| nbody          | 154 ms                                                 | 120 ms: 1.28x faster                                                             |
| pidigits       | 191 ms                                                 | 191 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                  | 1.23x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                            |
| regex_dna      | 227 ms                                                 | 223 ms: 1.02x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 301 us: 1.61x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 215 us: 1.54x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 59.6 ms: 1.33x faster                                                            |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 85.9 ms: 1.16x faster                                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.10x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.33 us: 1.03x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| unpickle             | 14.4 us                                                | 16.1 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.0 us: 1.15x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.89 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.49x faster                                                            |
| django_template | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.89x faster                                                             |
| generators               | 80.1 ms                                                | 30.4 ms: 2.64x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                            |
| async_tree_none          | 728 ms                                                 | 378 ms: 1.93x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| logging_silent           | 190 ns                                                 | 99.9 ns: 1.90x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 463 ms: 1.88x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 500 ms: 1.84x faster                                                             |
| richards_super           | 94.7 ms                                                | 51.7 ms: 1.83x faster                                                            |
| raytrace                 | 507 ms                                                 | 288 ms: 1.76x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.75x faster                                                            |
| richards                 | 79.3 ms                                                | 45.7 ms: 1.73x faster                                                            |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 594 ms: 1.71x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.13 ms: 1.70x faster                                                            |
| go                       | 240 ms                                                 | 142 ms: 1.69x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 75.9 ms: 1.68x faster                                                            |
| chaos                    | 115 ms                                                 | 68.7 ms: 1.68x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                            |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.63x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 72.8 ms: 1.62x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 301 us: 1.61x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 37.9 us: 1.54x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 215 us: 1.54x faster                                                             |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.49x faster                                                            |
| pyflate                  | 716 ms                                                 | 482 ms: 1.49x faster                                                             |
| scimark_lu               | 176 ms                                                 | 119 ms: 1.48x faster                                                             |
| coroutines               | 35.1 ms                                                | 24.1 ms: 1.46x faster                                                            |
| float                    | 117 ms                                                 | 80.8 ms: 1.45x faster                                                            |
| tornado_http             | 136 ms                                                 | 95.6 ms: 1.43x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.86 ms: 1.41x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.83 sec: 1.41x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.91 us: 1.40x faster                                                            |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                           |
| tomli_loads              | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 734 ms: 1.39x faster                                                             |
| logging_format           | 9.09 us                                                | 6.56 us: 1.39x faster                                                            |
| django_template          | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                           |
| deepcopy                 | 479 us                                                 | 355 us: 1.35x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                            |
| html5lib                 | 88.9 ms                                                | 66.1 ms: 1.34x faster                                                            |
| thrift                   | 1.07 ms                                                | 806 us: 1.33x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 59.6 ms: 1.33x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| fannkuch                 | 532 ms                                                 | 404 ms: 1.32x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.17 us: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 266 ms: 1.31x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                             |
| sympy_sum                | 196 ms                                                 | 152 ms: 1.29x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                            |
| nbody                    | 154 ms                                                 | 120 ms: 1.28x faster                                                             |
| nqueens                  | 106 ms                                                 | 83.0 ms: 1.27x faster                                                            |
| sympy_str                | 346 ms                                                 | 273 ms: 1.26x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 68.2 ms: 1.24x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| sympy_expand             | 566 ms                                                 | 464 ms: 1.22x faster                                                             |
| spectral_norm            | 170 ms                                                 | 140 ms: 1.21x faster                                                             |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                            |
| dask                     | 441 ms                                                 | 369 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 827 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.78 sec: 1.19x faster                                                           |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.45 ms: 1.19x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 85.9 ms: 1.16x faster                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.44 ms: 1.13x faster                                                            |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.11x faster                                                             |
| scimark_fft              | 466 ms                                                 | 422 ms: 1.10x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                            |
| json_loads               | 31.2 us                                                | 28.5 us: 1.10x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                                           |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| pickle_list              | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                                            |
| regex_dna                | 227 ms                                                 | 223 ms: 1.02x faster                                                             |
| async_generators         | 444 ms                                                 | 441 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 191 ms: 1.00x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.33 us: 1.03x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.73 ms: 1.03x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| unpickle                 | 14.4 us                                                | 16.1 us: 1.12x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.0 us: 1.15x slower                                                            |
| telco                    | 7.27 ms                                                | 8.41 ms: 1.16x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.23x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.89 ms: 1.50x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                     |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-198ceb6/bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.08x