# Results vs. 3.10.4

- fork: faster-cpython
- ref: call_complex_paramet
- machine: linux-x86_64
- commit hash: 8623ee7
- commit date: 2024-04-10
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 292 ms: 1.20x faster                                                                   |
| chameleon      | 9.44 ms                                                      | 7.12 ms: 1.33x faster                                                                  |
| docutils       | 3.41 sec                                                     | 2.99 sec: 1.14x faster                                                                 |
| html5lib       | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                                  |
| tornado_http   | 157 ms                                                       | 120 ms: 1.31x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.25x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 369 ms: 1.88x faster                                                                   |
| async_tree_memoization  | 819 ms                                                       | 462 ms: 1.77x faster                                                                   |
| async_tree_io           | 1.60 sec                                                     | 905 ms: 1.77x faster                                                                   |
| async_tree_cpu_io_mixed | 936 ms                                                       | 609 ms: 1.54x faster                                                                   |
| Geometric mean          | (ref)                                                        | 1.73x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 90.0 ms: 1.49x faster                                                                  |
| float          | 111 ms                                                       | 77.2 ms: 1.44x faster                                                                  |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.30x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 142 ms: 1.34x faster                                                                   |
| regex_v8       | 27.2 ms                                                      | 26.0 ms: 1.04x faster                                                                  |
| regex_dna      | 261 ms                                                       | 252 ms: 1.04x faster                                                                   |
| regex_effbot   | 3.09 ms                                                      | 3.56 ms: 1.15x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 315 us: 1.45x faster                                                                   |
| unpickle_pure_python | 312 us                                                       | 225 us: 1.38x faster                                                                   |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                                  |
| tomli_loads          | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                                 |
| xml_etree_process    | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                                  |
| json_loads           | 30.3 us                                                      | 25.9 us: 1.17x faster                                                                  |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.10x faster                                                                   |
| xml_etree_generate   | 92.3 ms                                                      | 84.5 ms: 1.09x faster                                                                  |
| xml_etree_iterparse  | 110 ms                                                       | 105 ms: 1.05x faster                                                                   |
| unpickle_list        | 4.65 us                                                      | 4.60 us: 1.01x faster                                                                  |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                                  |
| pickle_list          | 4.12 us                                                      | 4.42 us: 1.07x slower                                                                  |
| unpickle             | 13.5 us                                                      | 14.9 us: 1.11x slower                                                                  |
| pickle_dict          | 29.5 us                                                      | 33.6 us: 1.14x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                                  |
| python_startup_no_site | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                                  |
| genshi_text    | 31.4 ms                                                      | 25.1 ms: 1.25x faster                                                                  |
| genshi_xml     | 63.3 ms                                                      | 54.3 ms: 1.17x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 114 us: 4.72x faster                                                                   |
| deltablue                | 7.50 ms                                                      | 3.45 ms: 2.17x faster                                                                  |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.09x faster                                                                   |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                                 |
| raytrace                 | 489 ms                                                       | 258 ms: 1.89x faster                                                                   |
| async_tree_none          | 692 ms                                                       | 369 ms: 1.88x faster                                                                   |
| chaos                    | 109 ms                                                       | 59.9 ms: 1.81x faster                                                                  |
| pylint                   | 566 ms                                                       | 317 ms: 1.79x faster                                                                   |
| async_tree_memoization   | 819 ms                                                       | 462 ms: 1.77x faster                                                                   |
| async_tree_io            | 1.60 sec                                                     | 905 ms: 1.77x faster                                                                   |
| logging_silent           | 167 ns                                                       | 95.3 ns: 1.76x faster                                                                  |
| scimark_lu               | 167 ms                                                       | 95.2 ms: 1.75x faster                                                                  |
| generators               | 57.3 ms                                                      | 33.6 ms: 1.71x faster                                                                  |
| crypto_pyaes             | 119 ms                                                       | 71.8 ms: 1.66x faster                                                                  |
| comprehensions           | 26.7 us                                                      | 16.6 us: 1.61x faster                                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                                                  |
| richards_super           | 90.6 ms                                                      | 58.2 ms: 1.56x faster                                                                  |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 609 ms: 1.54x faster                                                                   |
| go                       | 262 ms                                                       | 170 ms: 1.54x faster                                                                   |
| scimark_monte_carlo      | 107 ms                                                       | 70.1 ms: 1.53x faster                                                                  |
| sqlglot_transpile        | 2.68 ms                                                      | 1.78 ms: 1.51x faster                                                                  |
| nbody                    | 134 ms                                                       | 90.0 ms: 1.49x faster                                                                  |
| spectral_norm            | 139 ms                                                       | 95.0 ms: 1.46x faster                                                                  |
| hexiom                   | 9.42 ms                                                      | 6.45 ms: 1.46x faster                                                                  |
| pickle_pure_python       | 455 us                                                       | 315 us: 1.45x faster                                                                   |
| float                    | 111 ms                                                       | 77.2 ms: 1.44x faster                                                                  |
| richards                 | 75.1 ms                                                      | 52.2 ms: 1.44x faster                                                                  |
| mako                     | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                                  |
| pyflate                  | 733 ms                                                       | 523 ms: 1.40x faster                                                                   |
| unpickle_pure_python     | 312 us                                                       | 225 us: 1.38x faster                                                                   |
| bench_mp_pool            | 6.37 ms                                                      | 4.61 ms: 1.38x faster                                                                  |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                                  |
| coroutines               | 30.3 ms                                                      | 22.4 ms: 1.35x faster                                                                  |
| logging_simple           | 8.88 us                                                      | 6.59 us: 1.35x faster                                                                  |
| regex_compile            | 190 ms                                                       | 142 ms: 1.34x faster                                                                   |
| thrift                   | 1.18 ms                                                      | 880 us: 1.34x faster                                                                   |
| tomli_loads              | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                                 |
| pprint_pformat           | 2.15 sec                                                     | 1.62 sec: 1.33x faster                                                                 |
| logging_format           | 9.64 us                                                      | 7.27 us: 1.33x faster                                                                  |
| pprint_safe_repr         | 1.05 sec                                                     | 792 ms: 1.33x faster                                                                   |
| chameleon                | 9.44 ms                                                      | 7.12 ms: 1.33x faster                                                                  |
| deepcopy_memo            | 49.8 us                                                      | 37.8 us: 1.32x faster                                                                  |
| pycparser                | 1.67 sec                                                     | 1.27 sec: 1.32x faster                                                                 |
| tornado_http             | 157 ms                                                       | 120 ms: 1.31x faster                                                                   |
| xml_etree_process        | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                                  |
| bench_thread_pool        | 1.14 ms                                                      | 888 us: 1.29x faster                                                                   |
| scimark_sor              | 180 ms                                                       | 141 ms: 1.28x faster                                                                   |
| nqueens                  | 115 ms                                                       | 90.1 ms: 1.28x faster                                                                  |
| html5lib                 | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                                  |
| genshi_text              | 31.4 ms                                                      | 25.1 ms: 1.25x faster                                                                  |
| sympy_sum                | 193 ms                                                       | 155 ms: 1.24x faster                                                                   |
| fannkuch                 | 483 ms                                                       | 392 ms: 1.23x faster                                                                   |
| sqlglot_normalize        | 144 ms                                                       | 118 ms: 1.22x faster                                                                   |
| sympy_str                | 360 ms                                                       | 296 ms: 1.22x faster                                                                   |
| scimark_fft              | 361 ms                                                       | 297 ms: 1.22x faster                                                                   |
| deepcopy                 | 468 us                                                       | 387 us: 1.21x faster                                                                   |
| mypy2                    | 933 ms                                                       | 772 ms: 1.21x faster                                                                   |
| sympy_integrate          | 28.2 ms                                                      | 23.4 ms: 1.20x faster                                                                  |
| sympy_expand             | 600 ms                                                       | 499 ms: 1.20x faster                                                                   |
| 2to3                     | 350 ms                                                       | 292 ms: 1.20x faster                                                                   |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.24 ms: 1.20x faster                                                                  |
| dask                     | 472 ms                                                       | 395 ms: 1.20x faster                                                                   |
| sqlglot_optimize         | 70.1 ms                                                      | 58.6 ms: 1.20x faster                                                                  |
| dulwich_log              | 81.1 ms                                                      | 68.0 ms: 1.19x faster                                                                  |
| mdp                      | 3.01 sec                                                     | 2.54 sec: 1.18x faster                                                                 |
| json_loads               | 30.3 us                                                      | 25.9 us: 1.17x faster                                                                  |
| genshi_xml               | 63.3 ms                                                      | 54.3 ms: 1.17x faster                                                                  |
| async_generators         | 421 ms                                                       | 364 ms: 1.16x faster                                                                   |
| deepcopy_reduce          | 4.01 us                                                      | 3.48 us: 1.15x faster                                                                  |
| docutils                 | 3.41 sec                                                     | 2.99 sec: 1.14x faster                                                                 |
| gunicorn                 | 1.16 ms                                                      | 1.04 ms: 1.11x faster                                                                  |
| aiohttp                  | 1.19 ms                                                      | 1.07 ms: 1.11x faster                                                                  |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                                  |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.10x faster                                                                   |
| xml_etree_generate       | 92.3 ms                                                      | 84.5 ms: 1.09x faster                                                                  |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                                                  |
| meteor_contest           | 138 ms                                                       | 129 ms: 1.07x faster                                                                   |
| json                     | 5.86 ms                                                      | 5.53 ms: 1.06x faster                                                                  |
| xml_etree_iterparse      | 110 ms                                                       | 105 ms: 1.05x faster                                                                   |
| regex_v8                 | 27.2 ms                                                      | 26.0 ms: 1.04x faster                                                                  |
| regex_dna                | 261 ms                                                       | 252 ms: 1.04x faster                                                                   |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                                   |
| unpickle_list            | 4.65 us                                                      | 4.60 us: 1.01x faster                                                                  |
| asyncio_websockets       | 390 ms                                                       | 395 ms: 1.01x slower                                                                   |
| create_gc_cycles         | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                                  |
| pickle                   | 9.89 us                                                      | 10.6 us: 1.07x slower                                                                  |
| pickle_list              | 4.12 us                                                      | 4.42 us: 1.07x slower                                                                  |
| unpickle                 | 13.5 us                                                      | 14.9 us: 1.11x slower                                                                  |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                                  |
| telco                    | 7.23 ms                                                      | 8.11 ms: 1.12x slower                                                                  |
| pickle_dict              | 29.5 us                                                      | 33.6 us: 1.14x slower                                                                  |
| regex_effbot             | 3.09 ms                                                      | 3.56 ms: 1.15x slower                                                                  |
| coverage                 | 63.3 ms                                                      | 85.3 ms: 1.35x slower                                                                  |
| gc_traversal             | 3.42 ms                                                      | 4.68 ms: 1.37x slower                                                                  |
| python_startup_no_site   | 7.33 ms                                                      | 11.1 ms: 1.51x slower                                                                  |
| Geometric mean           | (ref)                                                        | 1.29x faster                                                                           |
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-8623ee7/bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.10x