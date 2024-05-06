# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 292 ms: 1.20x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.19 ms: 1.31x faster                                                        |
| docutils       | 3.41 sec                                                     | 2.95 sec: 1.16x faster                                                       |
| html5lib       | 94.6 ms                                                      | 74.0 ms: 1.28x faster                                                        |
| tornado_http   | 157 ms                                                       | 121 ms: 1.29x faster                                                         |
| Geometric mean | (ref)                                                        | 1.25x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 376 ms: 1.84x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 451 ms: 1.82x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 893 ms: 1.79x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 594 ms: 1.58x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.75x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 87.5 ms: 1.53x faster                                                        |
| float          | 111 ms                                                       | 76.5 ms: 1.45x faster                                                        |
| pidigits       | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.32x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 142 ms: 1.34x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.7 ms: 1.06x faster                                                        |
| regex_dna      | 261 ms                                                       | 249 ms: 1.05x faster                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.55 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 306 us: 1.49x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 213 us: 1.46x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.39x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 58.4 ms: 1.30x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.30 sec: 1.27x faster                                                       |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.2 ms: 1.10x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.61 us: 1.01x faster                                                        |
| pickle               | 9.89 us                                                      | 10.5 us: 1.07x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.47 us: 1.09x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.7 us: 1.09x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 33.7 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.8 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.2 ms: 1.45x faster                                                        |
| django_template | 50.2 ms                                                      | 38.5 ms: 1.31x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 53.8 ms: 1.18x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.30x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 115 us: 4.66x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 371 ms: 2.10x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.57 ms: 2.10x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.57 sec: 1.97x faster                                                       |
| raytrace                 | 489 ms                                                       | 261 ms: 1.87x faster                                                         |
| async_tree_none          | 692 ms                                                       | 376 ms: 1.84x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 451 ms: 1.82x faster                                                         |
| chaos                    | 109 ms                                                       | 60.0 ms: 1.81x faster                                                        |
| async_tree_io            | 1.60 sec                                                     | 893 ms: 1.79x faster                                                         |
| pylint                   | 566 ms                                                       | 320 ms: 1.77x faster                                                         |
| scimark_lu               | 167 ms                                                       | 95.6 ms: 1.75x faster                                                        |
| logging_silent           | 167 ns                                                       | 96.2 ns: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.71x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 71.7 ms: 1.66x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 64.9 ms: 1.66x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.37 ms: 1.63x faster                                                        |
| comprehensions           | 26.7 us                                                      | 16.9 us: 1.58x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 594 ms: 1.58x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.75 ms: 1.54x faster                                                        |
| nbody                    | 134 ms                                                       | 87.5 ms: 1.53x faster                                                        |
| richards_super           | 90.6 ms                                                      | 59.3 ms: 1.53x faster                                                        |
| go                       | 262 ms                                                       | 172 ms: 1.52x faster                                                         |
| spectral_norm            | 139 ms                                                       | 92.7 ms: 1.50x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 306 us: 1.49x faster                                                         |
| hexiom                   | 9.42 ms                                                      | 6.41 ms: 1.47x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 213 us: 1.46x faster                                                         |
| float                    | 111 ms                                                       | 76.5 ms: 1.45x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.2 ms: 1.45x faster                                                        |
| richards                 | 75.1 ms                                                      | 53.6 ms: 1.40x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.59 ms: 1.39x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.39x faster                                                        |
| pyflate                  | 733 ms                                                       | 535 ms: 1.37x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.53 us: 1.36x faster                                                        |
| thrift                   | 1.18 ms                                                      | 865 us: 1.36x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 36.7 us: 1.35x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.12 us: 1.35x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.4 ms: 1.35x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.60 sec: 1.34x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 785 ms: 1.34x faster                                                         |
| regex_compile            | 190 ms                                                       | 142 ms: 1.34x faster                                                         |
| chameleon                | 9.44 ms                                                      | 7.19 ms: 1.31x faster                                                        |
| nqueens                  | 115 ms                                                       | 87.7 ms: 1.31x faster                                                        |
| django_template          | 50.2 ms                                                      | 38.5 ms: 1.31x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.4 ms: 1.30x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.29 sec: 1.30x faster                                                       |
| tornado_http             | 157 ms                                                       | 121 ms: 1.29x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 74.0 ms: 1.28x faster                                                        |
| sympy_sum                | 193 ms                                                       | 151 ms: 1.27x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.30 sec: 1.27x faster                                                       |
| fannkuch                 | 483 ms                                                       | 382 ms: 1.26x faster                                                         |
| bench_thread_pool        | 1.14 ms                                                      | 904 us: 1.26x faster                                                         |
| scimark_sor              | 180 ms                                                       | 144 ms: 1.25x faster                                                         |
| sympy_str                | 360 ms                                                       | 290 ms: 1.24x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 117 ms: 1.23x faster                                                         |
| deepcopy                 | 468 us                                                       | 381 us: 1.23x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.14 ms: 1.23x faster                                                        |
| scimark_fft              | 361 ms                                                       | 296 ms: 1.22x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 23.2 ms: 1.22x faster                                                        |
| mypy2                    | 933 ms                                                       | 768 ms: 1.22x faster                                                         |
| sympy_expand             | 600 ms                                                       | 495 ms: 1.21x faster                                                         |
| dask                     | 472 ms                                                       | 393 ms: 1.20x faster                                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 58.4 ms: 1.20x faster                                                        |
| 2to3                     | 350 ms                                                       | 292 ms: 1.20x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.52 sec: 1.19x faster                                                       |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                                        |
| deepcopy_reduce          | 4.01 us                                                      | 3.37 us: 1.19x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 68.7 ms: 1.18x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 53.8 ms: 1.18x faster                                                        |
| async_generators         | 421 ms                                                       | 360 ms: 1.17x faster                                                         |
| docutils                 | 3.41 sec                                                     | 2.95 sec: 1.16x faster                                                       |
| aiohttp                  | 1.19 ms                                                      | 1.05 ms: 1.13x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.05 ms: 1.11x faster                                                        |
| json                     | 5.86 ms                                                      | 5.33 ms: 1.10x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 84.2 ms: 1.10x faster                                                        |
| meteor_contest           | 138 ms                                                       | 126 ms: 1.09x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| unpack_sequence          | 59.9 ns                                                      | 56.3 ns: 1.06x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.7 ms: 1.06x faster                                                        |
| regex_dna                | 261 ms                                                       | 249 ms: 1.05x faster                                                         |
| pidigits                 | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.61 us: 1.01x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.81 ms: 1.02x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.5 us: 1.07x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.47 us: 1.09x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.7 us: 1.09x slower                                                        |
| telco                    | 7.23 ms                                                      | 7.91 ms: 1.09x slower                                                        |
| python_startup           | 11.5 ms                                                      | 12.8 ms: 1.12x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 33.7 us: 1.14x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.55 ms: 1.15x slower                                                        |
| coverage                 | 63.3 ms                                                      | 85.0 ms: 1.34x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.67 ms: 1.37x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.29x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.10x