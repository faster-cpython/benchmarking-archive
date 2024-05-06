# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 286 ms: 1.22x faster                                                          |
| chameleon      | 9.44 ms                                                      | 7.18 ms: 1.32x faster                                                         |
| docutils       | 3.41 sec                                                     | 3.00 sec: 1.14x faster                                                        |
| html5lib       | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                         |
| tornado_http   | 157 ms                                                       | 119 ms: 1.32x faster                                                          |
| Geometric mean | (ref)                                                        | 1.26x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 363 ms: 1.90x faster                                                          |
| async_tree_io           | 1.60 sec                                                     | 867 ms: 1.84x faster                                                          |
| async_tree_memoization  | 819 ms                                                       | 458 ms: 1.79x faster                                                          |
| async_tree_cpu_io_mixed | 936 ms                                                       | 606 ms: 1.55x faster                                                          |
| Geometric mean          | (ref)                                                        | 1.76x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 86.5 ms: 1.55x faster                                                         |
| float          | 111 ms                                                       | 77.4 ms: 1.44x faster                                                         |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                        | 1.32x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 142 ms: 1.34x faster                                                          |
| regex_dna      | 261 ms                                                       | 239 ms: 1.09x faster                                                          |
| regex_v8       | 27.2 ms                                                      | 26.5 ms: 1.03x faster                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.70 ms: 1.20x slower                                                         |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 308 us: 1.48x faster                                                          |
| unpickle_pure_python | 312 us                                                       | 212 us: 1.47x faster                                                          |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.23 sec: 1.30x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                         |
| json_loads           | 30.3 us                                                      | 24.6 us: 1.23x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                         |
| xml_etree_parse      | 160 ms                                                       | 150 ms: 1.07x faster                                                          |
| xml_etree_iterparse  | 110 ms                                                       | 106 ms: 1.04x faster                                                          |
| unpickle_list        | 4.65 us                                                      | 4.58 us: 1.02x faster                                                         |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                         |
| pickle_dict          | 29.5 us                                                      | 32.2 us: 1.09x slower                                                         |
| pickle_list          | 4.12 us                                                      | 4.52 us: 1.10x slower                                                         |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.13x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                         |
| python_startup_no_site | 7.33 ms                                                      | 8.81 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.2 ms: 1.45x faster                                                         |
| django_template | 50.2 ms                                                      | 38.7 ms: 1.30x faster                                                         |
| genshi_text     | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                         |
| genshi_xml      | 63.3 ms                                                      | 54.0 ms: 1.17x faster                                                         |
| Geometric mean  | (ref)                                                        | 1.29x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 173 us: 3.10x faster                                                          |
| deltablue                | 7.50 ms                                                      | 3.22 ms: 2.33x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 367 ms: 2.12x faster                                                          |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.57 sec: 1.97x faster                                                        |
| raytrace                 | 489 ms                                                       | 257 ms: 1.90x faster                                                          |
| async_tree_none          | 692 ms                                                       | 363 ms: 1.90x faster                                                          |
| chaos                    | 109 ms                                                       | 58.8 ms: 1.85x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 867 ms: 1.84x faster                                                          |
| async_tree_memoization   | 819 ms                                                       | 458 ms: 1.79x faster                                                          |
| logging_silent           | 167 ns                                                       | 93.9 ns: 1.78x faster                                                         |
| scimark_lu               | 167 ms                                                       | 95.4 ms: 1.75x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 61.8 ms: 1.74x faster                                                         |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.72x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 71.3 ms: 1.67x faster                                                         |
| pylint                   | 566 ms                                                       | 345 ms: 1.64x faster                                                          |
| go                       | 262 ms                                                       | 160 ms: 1.64x faster                                                          |
| sqlglot_parse            | 2.24 ms                                                      | 1.38 ms: 1.62x faster                                                         |
| pyflate                  | 733 ms                                                       | 454 ms: 1.61x faster                                                          |
| hexiom                   | 9.42 ms                                                      | 5.99 ms: 1.57x faster                                                         |
| comprehensions           | 26.7 us                                                      | 17.1 us: 1.56x faster                                                         |
| richards_super           | 90.6 ms                                                      | 58.4 ms: 1.55x faster                                                         |
| nbody                    | 134 ms                                                       | 86.5 ms: 1.55x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 606 ms: 1.55x faster                                                          |
| sqlglot_transpile        | 2.68 ms                                                      | 1.77 ms: 1.52x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 308 us: 1.48x faster                                                          |
| unpickle_pure_python     | 312 us                                                       | 212 us: 1.47x faster                                                          |
| coroutines               | 30.3 ms                                                      | 20.6 ms: 1.47x faster                                                         |
| bench_mp_pool            | 6.37 ms                                                      | 4.35 ms: 1.47x faster                                                         |
| scimark_sor              | 180 ms                                                       | 123 ms: 1.46x faster                                                          |
| mako                     | 14.7 ms                                                      | 10.2 ms: 1.45x faster                                                         |
| richards                 | 75.1 ms                                                      | 52.0 ms: 1.44x faster                                                         |
| float                    | 111 ms                                                       | 77.4 ms: 1.44x faster                                                         |
| spectral_norm            | 139 ms                                                       | 97.8 ms: 1.42x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.41 us: 1.38x faster                                                         |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.03 us: 1.37x faster                                                         |
| fannkuch                 | 483 ms                                                       | 356 ms: 1.36x faster                                                          |
| thrift                   | 1.18 ms                                                      | 878 us: 1.34x faster                                                          |
| regex_compile            | 190 ms                                                       | 142 ms: 1.34x faster                                                          |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.33x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.63 sec: 1.32x faster                                                        |
| tornado_http             | 157 ms                                                       | 119 ms: 1.32x faster                                                          |
| chameleon                | 9.44 ms                                                      | 7.18 ms: 1.32x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 798 ms: 1.32x faster                                                          |
| nqueens                  | 115 ms                                                       | 87.6 ms: 1.31x faster                                                         |
| tomli_loads              | 2.92 sec                                                     | 2.23 sec: 1.30x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                         |
| django_template          | 50.2 ms                                                      | 38.7 ms: 1.30x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                         |
| bench_thread_pool        | 1.14 ms                                                      | 890 us: 1.28x faster                                                          |
| deepcopy_memo            | 49.8 us                                                      | 38.9 us: 1.28x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 24.8 ms: 1.27x faster                                                         |
| sympy_sum                | 193 ms                                                       | 153 ms: 1.26x faster                                                          |
| pathlib                  | 21.4 ms                                                      | 17.2 ms: 1.24x faster                                                         |
| json_loads               | 30.3 us                                                      | 24.6 us: 1.23x faster                                                         |
| sympy_str                | 360 ms                                                       | 294 ms: 1.22x faster                                                          |
| 2to3                     | 350 ms                                                       | 286 ms: 1.22x faster                                                          |
| dulwich_log              | 81.1 ms                                                      | 66.4 ms: 1.22x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 118 ms: 1.22x faster                                                          |
| deepcopy                 | 468 us                                                       | 386 us: 1.21x faster                                                          |
| sympy_integrate          | 28.2 ms                                                      | 23.3 ms: 1.21x faster                                                         |
| mypy2                    | 933 ms                                                       | 771 ms: 1.21x faster                                                          |
| dask                     | 472 ms                                                       | 391 ms: 1.21x faster                                                          |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                        |
| sympy_expand             | 600 ms                                                       | 499 ms: 1.20x faster                                                          |
| scimark_fft              | 361 ms                                                       | 301 ms: 1.20x faster                                                          |
| sqlglot_optimize         | 70.1 ms                                                      | 58.9 ms: 1.19x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 54.0 ms: 1.17x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.36 ms: 1.17x faster                                                         |
| async_generators         | 421 ms                                                       | 365 ms: 1.15x faster                                                          |
| docutils                 | 3.41 sec                                                     | 3.00 sec: 1.14x faster                                                        |
| deepcopy_reduce          | 4.01 us                                                      | 3.56 us: 1.13x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.07 ms: 1.11x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.06 ms: 1.10x faster                                                         |
| regex_dna                | 261 ms                                                       | 239 ms: 1.09x faster                                                          |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                                         |
| json                     | 5.86 ms                                                      | 5.38 ms: 1.09x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                         |
| meteor_contest           | 138 ms                                                       | 128 ms: 1.08x faster                                                          |
| xml_etree_parse          | 160 ms                                                       | 150 ms: 1.07x faster                                                          |
| xml_etree_iterparse      | 110 ms                                                       | 106 ms: 1.04x faster                                                          |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                          |
| regex_v8                 | 27.2 ms                                                      | 26.5 ms: 1.03x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.58 us: 1.02x faster                                                         |
| pickle                   | 9.89 us                                                      | 10.4 us: 1.05x slower                                                         |
| pickle_dict              | 29.5 us                                                      | 32.2 us: 1.09x slower                                                         |
| pickle_list              | 4.12 us                                                      | 4.52 us: 1.10x slower                                                         |
| telco                    | 7.23 ms                                                      | 7.97 ms: 1.10x slower                                                         |
| create_gc_cycles         | 1.76 ms                                                      | 1.95 ms: 1.11x slower                                                         |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                         |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.13x slower                                                         |
| regex_effbot             | 3.09 ms                                                      | 3.70 ms: 1.20x slower                                                         |
| python_startup_no_site   | 7.33 ms                                                      | 8.81 ms: 1.20x slower                                                         |
| gc_traversal             | 3.42 ms                                                      | 4.42 ms: 1.30x slower                                                         |
| coverage                 | 63.3 ms                                                      | 85.3 ms: 1.35x slower                                                         |
| Geometric mean           | (ref)                                                        | 1.30x faster                                                                  |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.11x