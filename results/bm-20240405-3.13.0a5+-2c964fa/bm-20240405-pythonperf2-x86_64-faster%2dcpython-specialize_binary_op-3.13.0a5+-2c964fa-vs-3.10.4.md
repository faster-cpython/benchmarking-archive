# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 288 ms: 1.21x faster                                                                   |
| chameleon      | 9.44 ms                                                      | 7.47 ms: 1.26x faster                                                                  |
| docutils       | 3.41 sec                                                     | 2.98 sec: 1.15x faster                                                                 |
| html5lib       | 94.6 ms                                                      | 73.9 ms: 1.28x faster                                                                  |
| tornado_http   | 157 ms                                                       | 119 ms: 1.31x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.24x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 366 ms: 1.89x faster                                                                   |
| async_tree_memoization  | 819 ms                                                       | 460 ms: 1.78x faster                                                                   |
| async_tree_io           | 1.60 sec                                                     | 907 ms: 1.76x faster                                                                   |
| async_tree_cpu_io_mixed | 936 ms                                                       | 607 ms: 1.54x faster                                                                   |
| Geometric mean          | (ref)                                                        | 1.74x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 91.4 ms: 1.47x faster                                                                  |
| float          | 111 ms                                                       | 76.4 ms: 1.46x faster                                                                  |
| pidigits       | 271 ms                                                       | 262 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.30x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 141 ms: 1.35x faster                                                                   |
| regex_dna      | 261 ms                                                       | 240 ms: 1.09x faster                                                                   |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                                  |
| regex_effbot   | 3.09 ms                                                      | 3.48 ms: 1.13x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 307 us: 1.48x faster                                                                   |
| unpickle_pure_python | 312 us                                                       | 221 us: 1.41x faster                                                                   |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                                  |
| tomli_loads          | 2.92 sec                                                     | 2.20 sec: 1.32x faster                                                                 |
| xml_etree_process    | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                                  |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                                                  |
| xml_etree_generate   | 92.3 ms                                                      | 82.6 ms: 1.12x faster                                                                  |
| xml_etree_parse      | 160 ms                                                       | 148 ms: 1.08x faster                                                                   |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.06x faster                                                                   |
| unpickle_list        | 4.65 us                                                      | 4.57 us: 1.02x faster                                                                  |
| pickle_dict          | 29.5 us                                                      | 30.4 us: 1.03x slower                                                                  |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                                                  |
| pickle_list          | 4.12 us                                                      | 4.29 us: 1.04x slower                                                                  |
| unpickle             | 13.5 us                                                      | 15.2 us: 1.12x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.14x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| python_startup_no_site | 7.33 ms                                                      | 11.0 ms: 1.51x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.29x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.3 ms: 1.43x faster                                                                  |
| genshi_text    | 31.4 ms                                                      | 24.7 ms: 1.27x faster                                                                  |
| genshi_xml     | 63.3 ms                                                      | 53.5 ms: 1.18x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.29x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 116 us: 4.65x faster                                                                   |
| deltablue                | 7.50 ms                                                      | 3.42 ms: 2.19x faster                                                                  |
| asyncio_tcp              | 779 ms                                                       | 369 ms: 2.11x faster                                                                   |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                                 |
| raytrace                 | 489 ms                                                       | 258 ms: 1.89x faster                                                                   |
| async_tree_none          | 692 ms                                                       | 366 ms: 1.89x faster                                                                   |
| chaos                    | 109 ms                                                       | 60.7 ms: 1.79x faster                                                                  |
| async_tree_memoization   | 819 ms                                                       | 460 ms: 1.78x faster                                                                   |
| pylint                   | 566 ms                                                       | 318 ms: 1.78x faster                                                                   |
| logging_silent           | 167 ns                                                       | 94.0 ns: 1.78x faster                                                                  |
| async_tree_io            | 1.60 sec                                                     | 907 ms: 1.76x faster                                                                   |
| generators               | 57.3 ms                                                      | 32.9 ms: 1.74x faster                                                                  |
| scimark_lu               | 167 ms                                                       | 98.7 ms: 1.69x faster                                                                  |
| crypto_pyaes             | 119 ms                                                       | 72.4 ms: 1.65x faster                                                                  |
| comprehensions           | 26.7 us                                                      | 16.5 us: 1.61x faster                                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.59x faster                                                                  |
| scimark_monte_carlo      | 107 ms                                                       | 68.2 ms: 1.57x faster                                                                  |
| spectral_norm            | 139 ms                                                       | 88.4 ms: 1.57x faster                                                                  |
| richards_super           | 90.6 ms                                                      | 58.3 ms: 1.56x faster                                                                  |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 607 ms: 1.54x faster                                                                   |
| sqlglot_transpile        | 2.68 ms                                                      | 1.77 ms: 1.51x faster                                                                  |
| go                       | 262 ms                                                       | 173 ms: 1.51x faster                                                                   |
| pickle_pure_python       | 455 us                                                       | 307 us: 1.48x faster                                                                   |
| nbody                    | 134 ms                                                       | 91.4 ms: 1.47x faster                                                                  |
| float                    | 111 ms                                                       | 76.4 ms: 1.46x faster                                                                  |
| richards                 | 75.1 ms                                                      | 51.7 ms: 1.45x faster                                                                  |
| hexiom                   | 9.42 ms                                                      | 6.50 ms: 1.45x faster                                                                  |
| pyflate                  | 733 ms                                                       | 507 ms: 1.45x faster                                                                   |
| mako                     | 14.7 ms                                                      | 10.3 ms: 1.43x faster                                                                  |
| unpickle_pure_python     | 312 us                                                       | 221 us: 1.41x faster                                                                   |
| bench_mp_pool            | 6.37 ms                                                      | 4.55 ms: 1.40x faster                                                                  |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                                  |
| logging_simple           | 8.88 us                                                      | 6.49 us: 1.37x faster                                                                  |
| thrift                   | 1.18 ms                                                      | 867 us: 1.36x faster                                                                   |
| pprint_pformat           | 2.15 sec                                                     | 1.60 sec: 1.35x faster                                                                 |
| regex_compile            | 190 ms                                                       | 141 ms: 1.35x faster                                                                   |
| pprint_safe_repr         | 1.05 sec                                                     | 785 ms: 1.34x faster                                                                   |
| deepcopy_memo            | 49.8 us                                                      | 37.2 us: 1.34x faster                                                                  |
| coroutines               | 30.3 ms                                                      | 22.7 ms: 1.33x faster                                                                  |
| logging_format           | 9.64 us                                                      | 7.24 us: 1.33x faster                                                                  |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.32x faster                                                                 |
| tomli_loads              | 2.92 sec                                                     | 2.20 sec: 1.32x faster                                                                 |
| xml_etree_process        | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                                  |
| tornado_http             | 157 ms                                                       | 119 ms: 1.31x faster                                                                   |
| scimark_sor              | 180 ms                                                       | 139 ms: 1.29x faster                                                                   |
| bench_thread_pool        | 1.14 ms                                                      | 886 us: 1.29x faster                                                                   |
| nqueens                  | 115 ms                                                       | 89.5 ms: 1.28x faster                                                                  |
| html5lib                 | 94.6 ms                                                      | 73.9 ms: 1.28x faster                                                                  |
| genshi_text              | 31.4 ms                                                      | 24.7 ms: 1.27x faster                                                                  |
| fannkuch                 | 483 ms                                                       | 381 ms: 1.27x faster                                                                   |
| chameleon                | 9.44 ms                                                      | 7.47 ms: 1.26x faster                                                                  |
| sympy_sum                | 193 ms                                                       | 153 ms: 1.26x faster                                                                   |
| sqlglot_normalize        | 144 ms                                                       | 116 ms: 1.24x faster                                                                   |
| deepcopy                 | 468 us                                                       | 379 us: 1.24x faster                                                                   |
| sympy_str                | 360 ms                                                       | 294 ms: 1.22x faster                                                                   |
| mypy2                    | 933 ms                                                       | 766 ms: 1.22x faster                                                                   |
| dask                     | 472 ms                                                       | 389 ms: 1.21x faster                                                                   |
| 2to3                     | 350 ms                                                       | 288 ms: 1.21x faster                                                                   |
| sympy_expand             | 600 ms                                                       | 495 ms: 1.21x faster                                                                   |
| sympy_integrate          | 28.2 ms                                                      | 23.3 ms: 1.21x faster                                                                  |
| sqlglot_optimize         | 70.1 ms                                                      | 58.1 ms: 1.21x faster                                                                  |
| mdp                      | 3.01 sec                                                     | 2.51 sec: 1.20x faster                                                                 |
| dulwich_log              | 81.1 ms                                                      | 68.1 ms: 1.19x faster                                                                  |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                                                  |
| genshi_xml               | 63.3 ms                                                      | 53.5 ms: 1.18x faster                                                                  |
| async_generators         | 421 ms                                                       | 359 ms: 1.17x faster                                                                   |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.35 ms: 1.17x faster                                                                  |
| deepcopy_reduce          | 4.01 us                                                      | 3.43 us: 1.17x faster                                                                  |
| docutils                 | 3.41 sec                                                     | 2.98 sec: 1.15x faster                                                                 |
| scimark_fft              | 361 ms                                                       | 320 ms: 1.13x faster                                                                   |
| pathlib                  | 21.4 ms                                                      | 19.1 ms: 1.12x faster                                                                  |
| xml_etree_generate       | 92.3 ms                                                      | 82.6 ms: 1.12x faster                                                                  |
| gunicorn                 | 1.16 ms                                                      | 1.04 ms: 1.11x faster                                                                  |
| aiohttp                  | 1.19 ms                                                      | 1.08 ms: 1.10x faster                                                                  |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                                                  |
| regex_dna                | 261 ms                                                       | 240 ms: 1.09x faster                                                                   |
| meteor_contest           | 138 ms                                                       | 127 ms: 1.09x faster                                                                   |
| xml_etree_parse          | 160 ms                                                       | 148 ms: 1.08x faster                                                                   |
| json                     | 5.86 ms                                                      | 5.48 ms: 1.07x faster                                                                  |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                                  |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.06x faster                                                                   |
| pidigits                 | 271 ms                                                       | 262 ms: 1.04x faster                                                                   |
| unpickle_list            | 4.65 us                                                      | 4.57 us: 1.02x faster                                                                  |
| pickle_dict              | 29.5 us                                                      | 30.4 us: 1.03x slower                                                                  |
| pickle                   | 9.89 us                                                      | 10.2 us: 1.03x slower                                                                  |
| pickle_list              | 4.12 us                                                      | 4.29 us: 1.04x slower                                                                  |
| create_gc_cycles         | 1.76 ms                                                      | 1.92 ms: 1.09x slower                                                                  |
| telco                    | 7.23 ms                                                      | 7.91 ms: 1.09x slower                                                                  |
| python_startup           | 11.5 ms                                                      | 12.8 ms: 1.11x slower                                                                  |
| unpickle                 | 13.5 us                                                      | 15.2 us: 1.12x slower                                                                  |
| regex_effbot             | 3.09 ms                                                      | 3.48 ms: 1.13x slower                                                                  |
| gc_traversal             | 3.42 ms                                                      | 4.60 ms: 1.35x slower                                                                  |
| coverage                 | 63.3 ms                                                      | 89.1 ms: 1.41x slower                                                                  |
| python_startup_no_site   | 7.33 ms                                                      | 11.0 ms: 1.51x slower                                                                  |
| Geometric mean           | (ref)                                                        | 1.30x faster                                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-2c964fa/bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.10x