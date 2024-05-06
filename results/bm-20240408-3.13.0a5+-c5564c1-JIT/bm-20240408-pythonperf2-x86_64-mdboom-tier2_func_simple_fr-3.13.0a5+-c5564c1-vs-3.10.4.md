# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 298 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.70 ms: 1.23x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.09 sec: 1.10x faster                                                       |
| html5lib       | 94.6 ms                                                      | 73.7 ms: 1.28x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 847 ms: 1.89x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 441 ms: 1.86x faster                                                         |
| async_tree_none         | 692 ms                                                       | 375 ms: 1.84x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 606 ms: 1.54x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.78x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.3 ms: 1.46x faster                                                        |
| nbody          | 134 ms                                                       | 96.2 ms: 1.39x faster                                                        |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.29x faster                                                         |
| regex_dna      | 261 ms                                                       | 238 ms: 1.10x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.3 ms: 1.07x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.58 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 310 us: 1.47x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| unpickle_pure_python | 312 us                                                       | 233 us: 1.34x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.18 sec: 1.34x faster                                                       |
| xml_etree_process    | 75.9 ms                                                      | 59.2 ms: 1.28x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 85.9 ms: 1.07x faster                                                        |
| pickle_list          | 4.12 us                                                      | 4.44 us: 1.08x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.6 us: 1.08x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 34.6 us: 1.17x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| genshi_text    | 31.4 ms                                                      | 27.4 ms: 1.15x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 60.9 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                        | 1.20x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 123 us: 4.35x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.76 ms: 2.00x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 847 ms: 1.89x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 441 ms: 1.86x faster                                                         |
| async_tree_none          | 692 ms                                                       | 375 ms: 1.84x faster                                                         |
| raytrace                 | 489 ms                                                       | 271 ms: 1.80x faster                                                         |
| richards_super           | 90.6 ms                                                      | 52.1 ms: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.2 ms: 1.72x faster                                                        |
| logging_silent           | 167 ns                                                       | 98.1 ns: 1.71x faster                                                        |
| pylint                   | 566 ms                                                       | 334 ms: 1.69x faster                                                         |
| chaos                    | 109 ms                                                       | 64.2 ms: 1.69x faster                                                        |
| richards                 | 75.1 ms                                                      | 45.8 ms: 1.64x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.58x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 606 ms: 1.54x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 77.8 ms: 1.53x faster                                                        |
| pyflate                  | 733 ms                                                       | 481 ms: 1.52x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 70.8 ms: 1.52x faster                                                        |
| spectral_norm            | 139 ms                                                       | 93.3 ms: 1.49x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.48x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 310 us: 1.47x faster                                                         |
| mako                     | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| float                    | 111 ms                                                       | 76.3 ms: 1.46x faster                                                        |
| go                       | 262 ms                                                       | 180 ms: 1.45x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.30 us: 1.41x faster                                                        |
| nbody                    | 134 ms                                                       | 96.2 ms: 1.39x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.2 us: 1.39x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.2 ms: 1.37x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.08 us: 1.36x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.71 ms: 1.35x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 233 us: 1.34x faster                                                         |
| tomli_loads              | 2.92 sec                                                     | 2.18 sec: 1.34x faster                                                       |
| thrift                   | 1.18 ms                                                      | 884 us: 1.33x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.27 sec: 1.32x faster                                                       |
| hexiom                   | 9.42 ms                                                      | 7.17 ms: 1.31x faster                                                        |
| scimark_lu               | 167 ms                                                       | 128 ms: 1.30x faster                                                         |
| regex_compile            | 190 ms                                                       | 148 ms: 1.29x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 73.7 ms: 1.28x faster                                                        |
| tornado_http             | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 59.2 ms: 1.28x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.9 us: 1.28x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.70 sec: 1.27x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 831 ms: 1.26x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.13 ms: 1.23x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.70 ms: 1.23x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 931 us: 1.23x faster                                                         |
| fannkuch                 | 483 ms                                                       | 398 ms: 1.21x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 67.7 ms: 1.20x faster                                                        |
| json_loads               | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| sqlglot_normalize        | 144 ms                                                       | 121 ms: 1.18x faster                                                         |
| deepcopy                 | 468 us                                                       | 398 us: 1.18x faster                                                         |
| 2to3                     | 350 ms                                                       | 298 ms: 1.17x faster                                                         |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                         |
| sympy_sum                | 193 ms                                                       | 164 ms: 1.17x faster                                                         |
| sympy_str                | 360 ms                                                       | 308 ms: 1.17x faster                                                         |
| sympy_expand             | 600 ms                                                       | 515 ms: 1.16x faster                                                         |
| scimark_sor              | 180 ms                                                       | 156 ms: 1.15x faster                                                         |
| nqueens                  | 115 ms                                                       | 99.7 ms: 1.15x faster                                                        |
| mdp                      | 3.01 sec                                                     | 2.61 sec: 1.15x faster                                                       |
| genshi_text              | 31.4 ms                                                      | 27.4 ms: 1.15x faster                                                        |
| deepcopy_reduce          | 4.01 us                                                      | 3.50 us: 1.14x faster                                                        |
| mypy2                    | 933 ms                                                       | 818 ms: 1.14x faster                                                         |
| scimark_fft              | 361 ms                                                       | 320 ms: 1.13x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 62.7 ms: 1.12x faster                                                        |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.12x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.09 sec: 1.10x faster                                                       |
| async_generators         | 421 ms                                                       | 382 ms: 1.10x faster                                                         |
| regex_dna                | 261 ms                                                       | 238 ms: 1.10x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.73 us: 1.09x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.5 ms: 1.09x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| json                     | 5.86 ms                                                      | 5.45 ms: 1.08x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 85.9 ms: 1.07x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.3 ms: 1.07x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.07x faster                                                        |
| meteor_contest           | 138 ms                                                       | 132 ms: 1.05x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 60.9 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                         |
| create_gc_cycles         | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.44 us: 1.08x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.6 us: 1.08x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.05 ms: 1.11x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.58 ms: 1.16x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 34.6 us: 1.17x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.38 ms: 1.28x slower                                                        |
| coverage                 | 63.3 ms                                                      | 83.9 ms: 1.33x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                 |

Benchmark hidden because not significant (2): unpickle_list, asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x