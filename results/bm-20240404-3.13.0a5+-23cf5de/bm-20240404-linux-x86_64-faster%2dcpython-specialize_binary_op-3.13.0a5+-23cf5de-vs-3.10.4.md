# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 23cf5de
- commit date: 2024-04-04
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                            |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.8 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 608 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 81.7 ms: 1.43x faster                                                            |
| nbody          | 154 ms                                                 | 118 ms: 1.30x faster                                                             |
| pidigits       | 191 ms                                                 | 199 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.21x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.39x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                            |
| regex_dna      | 227 ms                                                 | 220 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.30 sec: 1.37x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 87.5 ms: 1.14x faster                                                            |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.04 us: 1.01x faster                                                            |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.3 us: 1.16x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.99 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 51.5 ms: 1.28x faster                                                            |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.78x faster                                                             |
| generators               | 80.1 ms                                                | 29.6 ms: 2.71x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.27 ms: 2.42x faster                                                            |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| logging_silent           | 190 ns                                                 | 100 ns: 1.90x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                             |
| raytrace                 | 507 ms                                                 | 279 ms: 1.82x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.78x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.74x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 73.5 ms: 1.74x faster                                                            |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                            |
| chaos                    | 115 ms                                                 | 68.6 ms: 1.68x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 608 ms: 1.67x faster                                                             |
| go                       | 240 ms                                                 | 146 ms: 1.65x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.39 ms: 1.63x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| scimark_sor              | 220 ms                                                 | 137 ms: 1.61x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 74.0 ms: 1.60x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 38.3 us: 1.53x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                             |
| pyflate                  | 716 ms                                                 | 480 ms: 1.49x faster                                                             |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| coroutines               | 35.1 ms                                                | 23.9 ms: 1.47x faster                                                            |
| scimark_lu               | 176 ms                                                 | 121 ms: 1.46x faster                                                             |
| tornado_http             | 136 ms                                                 | 94.8 ms: 1.44x faster                                                            |
| float                    | 117 ms                                                 | 81.7 ms: 1.43x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.83 us: 1.43x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.40x faster                                                           |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                           |
| regex_compile            | 188 ms                                                 | 135 ms: 1.39x faster                                                             |
| logging_format           | 9.09 us                                                | 6.54 us: 1.39x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 734 ms: 1.39x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.30 sec: 1.37x faster                                                           |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                           |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| thrift                   | 1.07 ms                                                | 808 us: 1.33x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                            |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                             |
| nbody                    | 154 ms                                                 | 118 ms: 1.30x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.29x faster                                                             |
| fannkuch                 | 532 ms                                                 | 413 ms: 1.29x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 51.5 ms: 1.28x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 54.9 ms: 1.26x faster                                                            |
| nqueens                  | 106 ms                                                 | 84.2 ms: 1.26x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 67.8 ms: 1.24x faster                                                            |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| spectral_norm            | 170 ms                                                 | 138 ms: 1.23x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                            |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| sympy_expand             | 566 ms                                                 | 470 ms: 1.20x faster                                                             |
| dask                     | 441 ms                                                 | 369 ms: 1.19x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 829 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 87.5 ms: 1.14x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                            |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                             |
| scimark_fft              | 466 ms                                                 | 428 ms: 1.09x faster                                                             |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.14 ms: 1.05x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| json                     | 5.69 ms                                                | 5.51 ms: 1.03x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                            |
| regex_dna                | 227 ms                                                 | 220 ms: 1.03x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.80 sec: 1.02x faster                                                           |
| pickle_list              | 5.08 us                                                | 5.04 us: 1.01x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| async_generators         | 444 ms                                                 | 442 ms: 1.00x faster                                                             |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.73 ms: 1.03x slower                                                            |
| pidigits                 | 191 ms                                                 | 199 ms: 1.04x slower                                                             |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.3 us: 1.16x slower                                                            |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.3 ms: 1.24x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.99 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                     |

Benchmark hidden because not significant (2): regex_effbot, unpickle_list
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-23cf5de/bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.09x