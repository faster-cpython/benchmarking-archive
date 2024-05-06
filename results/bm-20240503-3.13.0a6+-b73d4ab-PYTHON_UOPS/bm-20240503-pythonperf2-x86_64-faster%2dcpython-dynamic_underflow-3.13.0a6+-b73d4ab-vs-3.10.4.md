# Results vs. 3.10.4

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: b73d4ab
- commit date: 2024-05-03
- overall geometric mean: 1.06x faster
- HPT reliability: 92.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 9.44 ms                                                      | 8.91 ms: 1.06x faster                                                               |
| tornado_http   | 157 ms                                                       | 139 ms: 1.13x faster                                                                |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 921 ms: 1.73x faster                                                                |
| async_tree_none         | 692 ms                                                       | 399 ms: 1.73x faster                                                                |
| async_tree_memoization  | 819 ms                                                       | 502 ms: 1.63x faster                                                                |
| async_tree_cpu_io_mixed | 936 ms                                                       | 649 ms: 1.44x faster                                                                |
| Geometric mean          | (ref)                                                        | 1.63x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 98.7 ms: 1.13x faster                                                               |
| pidigits       | 271 ms                                                       | 256 ms: 1.06x faster                                                                |
| nbody          | 134 ms                                                       | 129 ms: 1.04x faster                                                                |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                                |
| regex_v8       | 27.2 ms                                                      | 26.3 ms: 1.03x faster                                                               |
| regex_effbot   | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                                               |
| regex_compile  | 190 ms                                                       | 231 ms: 1.21x slower                                                                |
| Geometric mean | (ref)                                                        | 1.06x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_dumps           | 14.5 ms                                                      | 11.4 ms: 1.27x faster                                                               |
| json_loads           | 30.3 us                                                      | 25.1 us: 1.21x faster                                                               |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.10x faster                                                                |
| xml_etree_process    | 75.9 ms                                                      | 69.2 ms: 1.10x faster                                                               |
| unpickle_list        | 4.65 us                                                      | 4.80 us: 1.03x slower                                                               |
| xml_etree_iterparse  | 110 ms                                                       | 116 ms: 1.05x slower                                                                |
| pickle_pure_python   | 455 us                                                       | 479 us: 1.05x slower                                                                |
| xml_etree_generate   | 92.3 ms                                                      | 97.6 ms: 1.06x slower                                                               |
| pickle_list          | 4.12 us                                                      | 4.37 us: 1.06x slower                                                               |
| unpickle_pure_python | 312 us                                                       | 335 us: 1.07x slower                                                                |
| pickle               | 9.89 us                                                      | 10.7 us: 1.09x slower                                                               |
| pickle_dict          | 29.5 us                                                      | 32.7 us: 1.11x slower                                                               |
| unpickle             | 13.5 us                                                      | 15.2 us: 1.13x slower                                                               |
| tomli_loads          | 2.92 sec                                                     | 3.32 sec: 1.14x slower                                                              |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                               |
| python_startup_no_site | 7.33 ms                                                      | 8.93 ms: 1.22x slower                                                               |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 50.2 ms                                                      | 46.8 ms: 1.07x faster                                                               |
| mako            | 14.7 ms                                                      | 14.2 ms: 1.03x faster                                                               |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 204 us: 2.63x faster                                                                |
| asyncio_tcp              | 779 ms                                                       | 392 ms: 1.99x faster                                                                |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.61 sec: 1.93x faster                                                              |
| async_tree_io            | 1.60 sec                                                     | 921 ms: 1.73x faster                                                                |
| async_tree_none          | 692 ms                                                       | 399 ms: 1.73x faster                                                                |
| generators               | 57.3 ms                                                      | 34.2 ms: 1.68x faster                                                               |
| async_tree_memoization   | 819 ms                                                       | 502 ms: 1.63x faster                                                                |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 649 ms: 1.44x faster                                                                |
| coroutines               | 30.3 ms                                                      | 22.5 ms: 1.35x faster                                                               |
| raytrace                 | 489 ms                                                       | 365 ms: 1.34x faster                                                                |
| logging_simple           | 8.88 us                                                      | 6.81 us: 1.30x faster                                                               |
| chaos                    | 109 ms                                                       | 83.5 ms: 1.30x faster                                                               |
| bench_mp_pool            | 6.37 ms                                                      | 4.92 ms: 1.30x faster                                                               |
| logging_format           | 9.64 us                                                      | 7.50 us: 1.29x faster                                                               |
| crypto_pyaes             | 119 ms                                                       | 92.9 ms: 1.28x faster                                                               |
| json_dumps               | 14.5 ms                                                      | 11.4 ms: 1.27x faster                                                               |
| sqlglot_parse            | 2.24 ms                                                      | 1.76 ms: 1.27x faster                                                               |
| thrift                   | 1.18 ms                                                      | 934 us: 1.26x faster                                                                |
| pylint                   | 566 ms                                                       | 454 ms: 1.25x faster                                                                |
| go                       | 262 ms                                                       | 216 ms: 1.21x faster                                                                |
| json_loads               | 30.3 us                                                      | 25.1 us: 1.21x faster                                                               |
| sqlglot_transpile        | 2.68 ms                                                      | 2.26 ms: 1.19x faster                                                               |
| deltablue                | 7.50 ms                                                      | 6.33 ms: 1.18x faster                                                               |
| pyflate                  | 733 ms                                                       | 632 ms: 1.16x faster                                                                |
| richards_super           | 90.6 ms                                                      | 78.3 ms: 1.16x faster                                                               |
| pathlib                  | 21.4 ms                                                      | 18.5 ms: 1.15x faster                                                               |
| float                    | 111 ms                                                       | 98.7 ms: 1.13x faster                                                               |
| tornado_http             | 157 ms                                                       | 139 ms: 1.13x faster                                                                |
| scimark_lu               | 167 ms                                                       | 149 ms: 1.12x faster                                                                |
| pycparser                | 1.67 sec                                                     | 1.51 sec: 1.11x faster                                                              |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.10x faster                                                                |
| xml_etree_process        | 75.9 ms                                                      | 69.2 ms: 1.10x faster                                                               |
| mdp                      | 3.01 sec                                                     | 2.77 sec: 1.08x faster                                                              |
| bench_thread_pool        | 1.14 ms                                                      | 1.05 ms: 1.08x faster                                                               |
| scimark_sor              | 180 ms                                                       | 167 ms: 1.08x faster                                                                |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                                |
| django_template          | 50.2 ms                                                      | 46.8 ms: 1.07x faster                                                               |
| dask                     | 472 ms                                                       | 441 ms: 1.07x faster                                                                |
| richards                 | 75.1 ms                                                      | 70.8 ms: 1.06x faster                                                               |
| json                     | 5.86 ms                                                      | 5.53 ms: 1.06x faster                                                               |
| pidigits                 | 271 ms                                                       | 256 ms: 1.06x faster                                                                |
| chameleon                | 9.44 ms                                                      | 8.91 ms: 1.06x faster                                                               |
| async_generators         | 421 ms                                                       | 398 ms: 1.06x faster                                                                |
| nbody                    | 134 ms                                                       | 129 ms: 1.04x faster                                                                |
| mako                     | 14.7 ms                                                      | 14.2 ms: 1.03x faster                                                               |
| regex_v8                 | 27.2 ms                                                      | 26.3 ms: 1.03x faster                                                               |
| sqlite_synth             | 2.99 us                                                      | 2.95 us: 1.01x faster                                                               |
| scimark_monte_carlo      | 107 ms                                                       | 109 ms: 1.01x slower                                                                |
| fannkuch                 | 483 ms                                                       | 498 ms: 1.03x slower                                                                |
| unpickle_list            | 4.65 us                                                      | 4.80 us: 1.03x slower                                                               |
| deepcopy_reduce          | 4.01 us                                                      | 4.14 us: 1.03x slower                                                               |
| logging_silent           | 167 ns                                                       | 174 ns: 1.04x slower                                                                |
| pprint_safe_repr         | 1.05 sec                                                     | 1.10 sec: 1.05x slower                                                              |
| nqueens                  | 115 ms                                                       | 120 ms: 1.05x slower                                                                |
| pprint_pformat           | 2.15 sec                                                     | 2.25 sec: 1.05x slower                                                              |
| spectral_norm            | 139 ms                                                       | 146 ms: 1.05x slower                                                                |
| xml_etree_iterparse      | 110 ms                                                       | 116 ms: 1.05x slower                                                                |
| pickle_pure_python       | 455 us                                                       | 479 us: 1.05x slower                                                                |
| deepcopy                 | 468 us                                                       | 495 us: 1.06x slower                                                                |
| xml_etree_generate       | 92.3 ms                                                      | 97.6 ms: 1.06x slower                                                               |
| sqlglot_optimize         | 70.1 ms                                                      | 74.3 ms: 1.06x slower                                                               |
| comprehensions           | 26.7 us                                                      | 28.3 us: 1.06x slower                                                               |
| pickle_list              | 4.12 us                                                      | 4.37 us: 1.06x slower                                                               |
| sqlglot_normalize        | 144 ms                                                       | 153 ms: 1.06x slower                                                                |
| meteor_contest           | 138 ms                                                       | 148 ms: 1.07x slower                                                                |
| unpickle_pure_python     | 312 us                                                       | 335 us: 1.07x slower                                                                |
| sympy_sum                | 193 ms                                                       | 208 ms: 1.08x slower                                                                |
| sympy_integrate          | 28.2 ms                                                      | 30.4 ms: 1.08x slower                                                               |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.09x slower                                                               |
| gunicorn                 | 1.16 ms                                                      | 1.26 ms: 1.09x slower                                                               |
| mypy2                    | 933 ms                                                       | 1.01 sec: 1.09x slower                                                              |
| aiohttp                  | 1.19 ms                                                      | 1.30 ms: 1.09x slower                                                               |
| dulwich_log              | 81.1 ms                                                      | 88.7 ms: 1.09x slower                                                               |
| pickle_dict              | 29.5 us                                                      | 32.7 us: 1.11x slower                                                               |
| unpickle                 | 13.5 us                                                      | 15.2 us: 1.13x slower                                                               |
| python_startup           | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                               |
| create_gc_cycles         | 1.76 ms                                                      | 2.01 ms: 1.14x slower                                                               |
| sympy_str                | 360 ms                                                       | 410 ms: 1.14x slower                                                                |
| tomli_loads              | 2.92 sec                                                     | 3.32 sec: 1.14x slower                                                              |
| regex_effbot             | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                                               |
| sympy_expand             | 600 ms                                                       | 685 ms: 1.14x slower                                                                |
| hexiom                   | 9.42 ms                                                      | 10.9 ms: 1.16x slower                                                               |
| flaskblogging            | 4.39 ms                                                      | 5.19 ms: 1.18x slower                                                               |
| scimark_fft              | 361 ms                                                       | 437 ms: 1.21x slower                                                                |
| regex_compile            | 190 ms                                                       | 231 ms: 1.21x slower                                                                |
| python_startup_no_site   | 7.33 ms                                                      | 8.93 ms: 1.22x slower                                                               |
| deepcopy_memo            | 49.8 us                                                      | 62.1 us: 1.25x slower                                                               |
| coverage                 | 63.3 ms                                                      | 81.6 ms: 1.29x slower                                                               |
| telco                    | 7.23 ms                                                      | 9.35 ms: 1.29x slower                                                               |
| gc_traversal             | 3.42 ms                                                      | 4.47 ms: 1.31x slower                                                               |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 6.92 ms: 1.36x slower                                                               |
| Geometric mean           | (ref)                                                        | 1.06x faster                                                                        |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: 2to3, docutils, genshi_text, genshi_xml, html5lib, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240503-3.13.0a6+-b73d4ab-PYTHON_UOPS/bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 92.12% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x