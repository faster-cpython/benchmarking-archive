# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 99be8f6
- commit date: 2024-04-08
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.87 ms: 1.41x faster                                                            |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| html5lib       | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 607 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.4 ms: 1.72x faster                                                            |
| float          | 117 ms                                                 | 77.5 ms: 1.51x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                            |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.85 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 300 us: 1.62x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 225 us: 1.47x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                            |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.27 us: 1.01x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.14 us: 1.01x slower                                                            |
| unpickle             | 14.4 us                                                | 14.9 us: 1.03x slower                                                            |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                            |
| genshi_text    | 31.8 ms                                                | 24.2 ms: 1.31x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 52.3 ms: 1.26x faster                                                            |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.64x faster                                                             |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.22 ms: 2.46x faster                                                            |
| async_tree_none          | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| pylint                   | 551 ms                                                 | 279 ms: 1.98x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 918 ms: 1.93x faster                                                             |
| raytrace                 | 507 ms                                                 | 263 ms: 1.93x faster                                                             |
| chaos                    | 115 ms                                                 | 60.1 ms: 1.92x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.89x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 503 ms: 1.83x faster                                                             |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.0 ms: 1.79x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 68.5 ms: 1.72x faster                                                            |
| nbody                    | 154 ms                                                 | 89.4 ms: 1.72x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 74.9 ms: 1.71x faster                                                            |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.69x faster                                                            |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 607 ms: 1.67x faster                                                             |
| go                       | 240 ms                                                 | 146 ms: 1.64x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.36 ms: 1.63x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 300 us: 1.62x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 36.9 us: 1.58x faster                                                            |
| scimark_lu               | 176 ms                                                 | 116 ms: 1.52x faster                                                             |
| float                    | 117 ms                                                 | 77.5 ms: 1.51x faster                                                            |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                            |
| pyflate                  | 716 ms                                                 | 480 ms: 1.49x faster                                                             |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.47x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 225 us: 1.47x faster                                                             |
| coroutines               | 35.1 ms                                                | 24.1 ms: 1.46x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.73 us: 1.45x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| logging_format           | 9.09 us                                                | 6.29 us: 1.45x faster                                                            |
| tornado_http             | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.87 ms: 1.41x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                           |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                                           |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 751 ms: 1.35x faster                                                             |
| fannkuch                 | 532 ms                                                 | 394 ms: 1.35x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                            |
| genshi_text              | 31.8 ms                                                | 24.2 ms: 1.31x faster                                                            |
| html5lib                 | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.20 us: 1.31x faster                                                            |
| thrift                   | 1.07 ms                                                | 823 us: 1.30x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                            |
| nqueens                  | 106 ms                                                 | 82.2 ms: 1.29x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                             |
| 2to3                     | 348 ms                                                 | 271 ms: 1.28x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 52.3 ms: 1.26x faster                                                            |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 55.3 ms: 1.25x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 67.8 ms: 1.24x faster                                                            |
| scimark_fft              | 466 ms                                                 | 375 ms: 1.24x faster                                                             |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.36 ms: 1.21x faster                                                            |
| sympy_expand             | 566 ms                                                 | 471 ms: 1.20x faster                                                             |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 836 us: 1.18x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.6 ms: 1.10x faster                                                            |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| meteor_contest           | 120 ms                                                 | 113 ms: 1.06x faster                                                             |
| json                     | 5.69 ms                                                | 5.38 ms: 1.06x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.73 sec: 1.04x faster                                                           |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                            |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.27 us: 1.01x slower                                                            |
| pickle_list              | 5.08 us                                                | 5.14 us: 1.01x slower                                                            |
| unpickle                 | 14.4 us                                                | 14.9 us: 1.03x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.85 ms: 1.06x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.74 ms: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 4.00 ms: 1.10x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.18x slower                                                            |
| telco                    | 7.27 ms                                                | 8.61 ms: 1.19x slower                                                            |
| coverage                 | 79.4 ms                                                | 99.5 ms: 1.25x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-99be8f6/bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x