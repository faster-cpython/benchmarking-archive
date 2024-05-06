# Results vs. 3.10.4

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: 17ed8bc
- commit date: 2024-04-05
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 269 ms: 1.29x faster                                                          |
| chameleon      | 9.68 ms                                                | 6.99 ms: 1.39x faster                                                         |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                        |
| html5lib       | 88.9 ms                                                | 66.6 ms: 1.33x faster                                                         |
| tornado_http   | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 930 ms: 1.90x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 615 ms: 1.65x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 81.0 ms: 1.45x faster                                                         |
| nbody          | 154 ms                                                 | 116 ms: 1.33x faster                                                          |
| Geometric mean | (ref)                                                  | 1.24x faster                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.39x faster                                                          |
| regex_v8       | 27.8 ms                                                | 26.1 ms: 1.07x faster                                                         |
| regex_dna      | 227 ms                                                 | 232 ms: 1.02x slower                                                          |
| regex_effbot   | 3.63 ms                                                | 3.87 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                          |
| unpickle_pure_python | 331 us                                                 | 217 us: 1.52x faster                                                          |
| tomli_loads          | 3.14 sec                                               | 2.25 sec: 1.39x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                         |
| xml_etree_process    | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 86.4 ms: 1.15x faster                                                         |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                          |
| unpickle_list        | 5.20 us                                                | 5.27 us: 1.01x slower                                                         |
| pickle_list          | 5.08 us                                                | 5.26 us: 1.04x slower                                                         |
| unpickle             | 14.4 us                                                | 15.8 us: 1.10x slower                                                         |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                         |
| pickle_dict          | 29.6 us                                                | 34.5 us: 1.16x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 9.02 ms: 1.52x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                         |
| genshi_text    | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                         |
| genshi_xml     | 66.0 ms                                                | 51.6 ms: 1.28x faster                                                         |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.76x faster                                                          |
| generators               | 80.1 ms                                                | 29.4 ms: 2.72x faster                                                         |
| deltablue                | 7.91 ms                                                | 3.21 ms: 2.46x faster                                                         |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                          |
| pylint                   | 551 ms                                                 | 279 ms: 1.98x faster                                                          |
| async_tree_io            | 1.77 sec                                               | 930 ms: 1.90x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                          |
| logging_silent           | 190 ns                                                 | 101 ns: 1.87x faster                                                          |
| raytrace                 | 507 ms                                                 | 278 ms: 1.82x faster                                                          |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.81x faster                                                          |
| richards_super           | 94.7 ms                                                | 52.9 ms: 1.79x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 73.0 ms: 1.75x faster                                                         |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.73x faster                                                         |
| chaos                    | 115 ms                                                 | 67.8 ms: 1.70x faster                                                         |
| richards                 | 79.3 ms                                                | 46.8 ms: 1.69x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.15 ms: 1.69x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                         |
| go                       | 240 ms                                                 | 145 ms: 1.66x faster                                                          |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 615 ms: 1.65x faster                                                          |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                          |
| scimark_monte_carlo      | 118 ms                                                 | 72.8 ms: 1.62x faster                                                         |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                         |
| deepcopy_memo            | 58.5 us                                                | 38.1 us: 1.54x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 217 us: 1.52x faster                                                          |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.51x faster                                                          |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                         |
| pyflate                  | 716 ms                                                 | 482 ms: 1.49x faster                                                          |
| coroutines               | 35.1 ms                                                | 24.0 ms: 1.46x faster                                                         |
| float                    | 117 ms                                                 | 81.0 ms: 1.45x faster                                                         |
| tornado_http             | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.78 us: 1.44x faster                                                         |
| logging_format           | 9.09 us                                                | 6.44 us: 1.41x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                        |
| tomli_loads              | 3.14 sec                                               | 2.25 sec: 1.39x faster                                                        |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                        |
| regex_compile            | 188 ms                                                 | 136 ms: 1.39x faster                                                          |
| chameleon                | 9.68 ms                                                | 6.99 ms: 1.39x faster                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 737 ms: 1.38x faster                                                          |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                         |
| genshi_text              | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                         |
| deepcopy                 | 479 us                                                 | 355 us: 1.35x faster                                                          |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                         |
| html5lib                 | 88.9 ms                                                | 66.6 ms: 1.33x faster                                                         |
| thrift                   | 1.07 ms                                                | 804 us: 1.33x faster                                                          |
| nbody                    | 154 ms                                                 | 116 ms: 1.33x faster                                                          |
| xml_etree_process        | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                         |
| fannkuch                 | 532 ms                                                 | 404 ms: 1.32x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.31x faster                                                        |
| deepcopy_reduce          | 4.17 us                                                | 3.20 us: 1.31x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                          |
| 2to3                     | 348 ms                                                 | 269 ms: 1.29x faster                                                          |
| genshi_xml               | 66.0 ms                                                | 51.6 ms: 1.28x faster                                                         |
| nqueens                  | 106 ms                                                 | 83.5 ms: 1.27x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                                         |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                          |
| sqlglot_optimize         | 69.2 ms                                                | 54.9 ms: 1.26x faster                                                         |
| spectral_norm            | 170 ms                                                 | 135 ms: 1.26x faster                                                          |
| dulwich_log              | 84.3 ms                                                | 67.6 ms: 1.25x faster                                                         |
| sympy_str                | 346 ms                                                 | 280 ms: 1.24x faster                                                          |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                         |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                         |
| sympy_expand             | 566 ms                                                 | 471 ms: 1.20x faster                                                          |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                          |
| bench_thread_pool        | 986 us                                                 | 828 us: 1.19x faster                                                          |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                        |
| xml_etree_generate       | 99.4 ms                                                | 86.4 ms: 1.15x faster                                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.74 ms: 1.13x faster                                                         |
| scimark_fft              | 466 ms                                                 | 419 ms: 1.11x faster                                                          |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                          |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                                         |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                          |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 26.1 ms: 1.07x faster                                                         |
| json                     | 5.69 ms                                                | 5.39 ms: 1.05x faster                                                         |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                          |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                        |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                          |
| unpickle_list            | 5.20 us                                                | 5.27 us: 1.01x slower                                                         |
| regex_dna                | 227 ms                                                 | 232 ms: 1.02x slower                                                          |
| pickle_list              | 5.08 us                                                | 5.26 us: 1.04x slower                                                         |
| gc_traversal             | 3.62 ms                                                | 3.80 ms: 1.05x slower                                                         |
| regex_effbot             | 3.63 ms                                                | 3.87 ms: 1.07x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.8 us: 1.10x slower                                                         |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                         |
| pickle_dict              | 29.6 us                                                | 34.5 us: 1.16x slower                                                         |
| telco                    | 7.27 ms                                                | 8.63 ms: 1.19x slower                                                         |
| coverage                 | 79.4 ms                                                | 98.6 ms: 1.24x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 9.02 ms: 1.52x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                  |

Benchmark hidden because not significant (2): pidigits, async_generators
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-17ed8bc/bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x