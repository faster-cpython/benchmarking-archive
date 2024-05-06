# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.58 ms: 1.25x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.08 sec: 1.11x faster                                                       |
| html5lib       | 94.6 ms                                                      | 74.4 ms: 1.27x faster                                                        |
| tornado_http   | 157 ms                                                       | 124 ms: 1.26x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 358 ms: 1.93x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 440 ms: 1.86x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 882 ms: 1.81x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 592 ms: 1.58x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.79x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 78.5 ms: 1.42x faster                                                        |
| nbody          | 134 ms                                                       | 94.9 ms: 1.41x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.70 ms: 1.20x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 311 us: 1.46x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.17 sec: 1.34x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 235 us: 1.33x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 58.3 ms: 1.30x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.1 ms: 1.10x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| pickle_list          | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 33.1 us: 1.12x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.2 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.6 ms: 1.18x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| django_template | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 27.4 ms: 1.15x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 59.4 ms: 1.07x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.22x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 128 us: 4.21x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 371 ms: 2.10x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.75 ms: 2.00x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| async_tree_none          | 692 ms                                                       | 358 ms: 1.93x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 440 ms: 1.86x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 882 ms: 1.81x faster                                                         |
| generators               | 57.3 ms                                                      | 33.6 ms: 1.70x faster                                                        |
| logging_silent           | 167 ns                                                       | 98.3 ns: 1.70x faster                                                        |
| pylint                   | 566 ms                                                       | 339 ms: 1.67x faster                                                         |
| raytrace                 | 489 ms                                                       | 304 ms: 1.61x faster                                                         |
| chaos                    | 109 ms                                                       | 67.9 ms: 1.60x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 592 ms: 1.58x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.57x faster                                                        |
| richards_super           | 90.6 ms                                                      | 58.4 ms: 1.55x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 77.1 ms: 1.55x faster                                                        |
| spectral_norm            | 139 ms                                                       | 93.2 ms: 1.49x faster                                                        |
| go                       | 262 ms                                                       | 175 ms: 1.49x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 72.9 ms: 1.47x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| richards                 | 75.1 ms                                                      | 51.3 ms: 1.46x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 311 us: 1.46x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.83 ms: 1.46x faster                                                        |
| pyflate                  | 733 ms                                                       | 514 ms: 1.43x faster                                                         |
| float                    | 111 ms                                                       | 78.5 ms: 1.42x faster                                                        |
| nbody                    | 134 ms                                                       | 94.9 ms: 1.41x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.61 us: 1.34x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.17 sec: 1.34x faster                                                       |
| thrift                   | 1.18 ms                                                      | 878 us: 1.34x faster                                                         |
| coroutines               | 30.3 ms                                                      | 22.7 ms: 1.34x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.24 us: 1.33x faster                                                        |
| comprehensions           | 26.7 us                                                      | 20.1 us: 1.33x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 235 us: 1.33x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.32x faster                                                       |
| scimark_lu               | 167 ms                                                       | 127 ms: 1.31x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 58.3 ms: 1.30x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.97 ms: 1.28x faster                                                        |
| regex_compile            | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| fannkuch                 | 483 ms                                                       | 379 ms: 1.27x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 74.4 ms: 1.27x faster                                                        |
| tornado_http             | 157 ms                                                       | 124 ms: 1.26x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.71 sec: 1.26x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 836 ms: 1.26x faster                                                         |
| django_template          | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 39.9 us: 1.25x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.58 ms: 1.25x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 7.59 ms: 1.24x faster                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.11 ms: 1.23x faster                                                        |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                        |
| sympy_sum                | 193 ms                                                       | 161 ms: 1.19x faster                                                         |
| sympy_str                | 360 ms                                                       | 304 ms: 1.18x faster                                                         |
| dask                     | 472 ms                                                       | 402 ms: 1.17x faster                                                         |
| deepcopy                 | 468 us                                                       | 398 us: 1.17x faster                                                         |
| scimark_sor              | 180 ms                                                       | 154 ms: 1.17x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 69.2 ms: 1.17x faster                                                        |
| sympy_expand             | 600 ms                                                       | 513 ms: 1.17x faster                                                         |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.48 us: 1.15x faster                                                        |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.62 sec: 1.15x faster                                                       |
| genshi_text              | 31.4 ms                                                      | 27.4 ms: 1.15x faster                                                        |
| scimark_fft              | 361 ms                                                       | 318 ms: 1.14x faster                                                         |
| mypy2                    | 933 ms                                                       | 830 ms: 1.12x faster                                                         |
| nqueens                  | 115 ms                                                       | 103 ms: 1.12x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.11x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 63.1 ms: 1.11x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.08 sec: 1.11x faster                                                       |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 84.1 ms: 1.10x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.8 ms: 1.08x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| json                     | 5.86 ms                                                      | 5.44 ms: 1.08x faster                                                        |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| async_generators         | 421 ms                                                       | 395 ms: 1.07x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 59.4 ms: 1.07x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                         |
| unpack_sequence          | 59.9 ns                                                      | 58.9 ns: 1.02x faster                                                        |
| asyncio_websockets       | 390 ms                                                       | 387 ms: 1.01x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.80 ms: 1.02x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.00 ms: 1.11x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 33.1 us: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.2 us: 1.13x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.6 ms: 1.18x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.70 ms: 1.20x slower                                                        |
| coverage                 | 63.3 ms                                                      | 82.4 ms: 1.30x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.57 ms: 1.34x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.24x faster                                                                 |

Benchmark hidden because not significant (1): bench_thread_pool
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x