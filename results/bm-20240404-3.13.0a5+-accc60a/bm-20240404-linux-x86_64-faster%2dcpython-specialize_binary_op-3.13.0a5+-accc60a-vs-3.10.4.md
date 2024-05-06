# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: accc60a
- commit date: 2024-04-04
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                            |
| docutils       | 3.30 sec                                               | 2.78 sec: 1.18x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.3 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.90x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 608 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 81.7 ms: 1.43x faster                                                            |
| nbody          | 154 ms                                                 | 127 ms: 1.21x faster                                                             |
| pidigits       | 191 ms                                                 | 195 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                  | 1.19x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.10x faster                                                            |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                     |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 297 us: 1.63x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.6 ms: 1.12x faster                                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.09 us: 1.02x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.26 us: 1.04x slower                                                            |
| unpickle             | 14.4 us                                                | 15.6 us: 1.08x slower                                                            |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.01 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.5 ms: 1.36x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                            |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.81x faster                                                             |
| generators               | 80.1 ms                                                | 29.6 ms: 2.71x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.17 ms: 2.50x faster                                                            |
| async_tree_none          | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| logging_silent           | 190 ns                                                 | 99.2 ns: 1.91x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.90x faster                                                             |
| richards_super           | 94.7 ms                                                | 52.0 ms: 1.82x faster                                                            |
| raytrace                 | 507 ms                                                 | 280 ms: 1.81x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.3 us: 1.76x faster                                                            |
| richards                 | 79.3 ms                                                | 46.2 ms: 1.71x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 75.0 ms: 1.70x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 608 ms: 1.67x faster                                                             |
| chaos                    | 115 ms                                                 | 69.9 ms: 1.65x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.30 ms: 1.65x faster                                                            |
| go                       | 240 ms                                                 | 146 ms: 1.64x faster                                                             |
| scimark_sor              | 220 ms                                                 | 135 ms: 1.63x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 297 us: 1.63x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 73.0 ms: 1.62x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.61x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 36.5 us: 1.60x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                             |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| pyflate                  | 716 ms                                                 | 486 ms: 1.47x faster                                                             |
| coroutines               | 35.1 ms                                                | 24.1 ms: 1.45x faster                                                            |
| scimark_lu               | 176 ms                                                 | 121 ms: 1.45x faster                                                             |
| tornado_http             | 136 ms                                                 | 94.3 ms: 1.45x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.75 us: 1.44x faster                                                            |
| float                    | 117 ms                                                 | 81.7 ms: 1.43x faster                                                            |
| logging_format           | 9.09 us                                                | 6.43 us: 1.41x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.50 sec: 1.40x faster                                                           |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| chameleon                | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 733 ms: 1.39x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                           |
| deepcopy                 | 479 us                                                 | 347 us: 1.38x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.5 ms: 1.36x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.12 us: 1.34x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.19 sec: 1.32x faster                                                           |
| thrift                   | 1.07 ms                                                | 811 us: 1.32x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.31x faster                                                             |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 51.2 ms: 1.29x faster                                                            |
| fannkuch                 | 532 ms                                                 | 414 ms: 1.28x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 54.7 ms: 1.27x faster                                                            |
| nqueens                  | 106 ms                                                 | 83.8 ms: 1.26x faster                                                            |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.6 ms: 1.25x faster                                                            |
| sympy_str                | 346 ms                                                 | 278 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                                            |
| mypy2                    | 894 ms                                                 | 736 ms: 1.21x faster                                                             |
| sympy_expand             | 566 ms                                                 | 466 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                            |
| nbody                    | 154 ms                                                 | 127 ms: 1.21x faster                                                             |
| spectral_norm            | 170 ms                                                 | 141 ms: 1.20x faster                                                             |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 828 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.78 sec: 1.18x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.6 ms: 1.12x faster                                                            |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.10x faster                                                            |
| json_loads               | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| scimark_fft              | 466 ms                                                 | 427 ms: 1.09x faster                                                             |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.08x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.65 sec: 1.08x faster                                                           |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.13 ms: 1.06x faster                                                            |
| json                     | 5.69 ms                                                | 5.43 ms: 1.05x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.05x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.96 us: 1.02x faster                                                            |
| unpickle_list            | 5.20 us                                                | 5.09 us: 1.02x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                             |
| pidigits                 | 191 ms                                                 | 195 ms: 1.02x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.26 us: 1.04x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.08x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 4.02 ms: 1.11x slower                                                            |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                            |
| telco                    | 7.27 ms                                                | 8.60 ms: 1.18x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| coverage                 | 79.4 ms                                                | 101 ms: 1.27x slower                                                             |
| python_startup_no_site   | 5.93 ms                                                | 9.01 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                     |

Benchmark hidden because not significant (3): async_generators, regex_dna, regex_effbot
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-accc60a/bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x