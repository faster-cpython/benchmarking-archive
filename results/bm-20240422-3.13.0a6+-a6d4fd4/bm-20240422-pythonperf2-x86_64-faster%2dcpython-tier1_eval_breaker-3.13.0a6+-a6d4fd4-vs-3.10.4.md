# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 287 ms: 1.22x faster                                                                 |
| chameleon      | 9.44 ms                                                      | 7.29 ms: 1.30x faster                                                                |
| docutils       | 3.41 sec                                                     | 2.99 sec: 1.14x faster                                                               |
| html5lib       | 94.6 ms                                                      | 72.6 ms: 1.30x faster                                                                |
| tornado_http   | 157 ms                                                       | 120 ms: 1.30x faster                                                                 |
| Geometric mean | (ref)                                                        | 1.25x faster                                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 368 ms: 1.88x faster                                                                 |
| async_tree_io           | 1.60 sec                                                     | 900 ms: 1.78x faster                                                                 |
| async_tree_memoization  | 819 ms                                                       | 464 ms: 1.77x faster                                                                 |
| async_tree_cpu_io_mixed | 936 ms                                                       | 613 ms: 1.53x faster                                                                 |
| Geometric mean          | (ref)                                                        | 1.73x faster                                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 86.7 ms: 1.55x faster                                                                |
| float          | 111 ms                                                       | 77.2 ms: 1.44x faster                                                                |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                                 |
| Geometric mean | (ref)                                                        | 1.32x faster                                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                                 |
| regex_dna      | 261 ms                                                       | 238 ms: 1.10x faster                                                                 |
| regex_v8       | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                                                |
| regex_effbot   | 3.09 ms                                                      | 3.47 ms: 1.13x slower                                                                |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| unpickle_pure_python | 312 us                                                       | 204 us: 1.53x faster                                                                 |
| pickle_pure_python   | 455 us                                                       | 310 us: 1.47x faster                                                                 |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                                |
| tomli_loads          | 2.92 sec                                                     | 2.18 sec: 1.34x faster                                                               |
| xml_etree_process    | 75.9 ms                                                      | 59.6 ms: 1.27x faster                                                                |
| json_loads           | 30.3 us                                                      | 24.8 us: 1.22x faster                                                                |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.10x faster                                                                 |
| xml_etree_generate   | 92.3 ms                                                      | 85.1 ms: 1.08x faster                                                                |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.07x faster                                                                 |
| unpickle_list        | 4.65 us                                                      | 4.56 us: 1.02x faster                                                                |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                                |
| pickle_list          | 4.12 us                                                      | 4.44 us: 1.08x slower                                                                |
| unpickle             | 13.5 us                                                      | 14.8 us: 1.09x slower                                                                |
| pickle_dict          | 29.5 us                                                      | 33.3 us: 1.13x slower                                                                |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                                |
| python_startup_no_site | 7.33 ms                                                      | 8.84 ms: 1.21x slower                                                                |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.5 ms: 1.40x faster                                                                |
| django_template | 50.2 ms                                                      | 38.8 ms: 1.29x faster                                                                |
| genshi_text     | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                                                |
| genshi_xml      | 63.3 ms                                                      | 56.2 ms: 1.13x faster                                                                |
| Geometric mean  | (ref)                                                        | 1.25x faster                                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 118 us: 4.56x faster                                                                 |
| deltablue                | 7.50 ms                                                      | 3.32 ms: 2.26x faster                                                                |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                                 |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                               |
| raytrace                 | 489 ms                                                       | 253 ms: 1.93x faster                                                                 |
| async_tree_none          | 692 ms                                                       | 368 ms: 1.88x faster                                                                 |
| chaos                    | 109 ms                                                       | 58.6 ms: 1.85x faster                                                                |
| async_tree_io            | 1.60 sec                                                     | 900 ms: 1.78x faster                                                                 |
| logging_silent           | 167 ns                                                       | 94.6 ns: 1.77x faster                                                                |
| async_tree_memoization   | 819 ms                                                       | 464 ms: 1.77x faster                                                                 |
| generators               | 57.3 ms                                                      | 33.1 ms: 1.73x faster                                                                |
| scimark_monte_carlo      | 107 ms                                                       | 63.2 ms: 1.70x faster                                                                |
| scimark_lu               | 167 ms                                                       | 98.6 ms: 1.69x faster                                                                |
| go                       | 262 ms                                                       | 155 ms: 1.69x faster                                                                 |
| crypto_pyaes             | 119 ms                                                       | 72.6 ms: 1.64x faster                                                                |
| pylint                   | 566 ms                                                       | 345 ms: 1.64x faster                                                                 |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.59x faster                                                                |
| comprehensions           | 26.7 us                                                      | 16.8 us: 1.59x faster                                                                |
| pyflate                  | 733 ms                                                       | 468 ms: 1.57x faster                                                                 |
| richards_super           | 90.6 ms                                                      | 58.0 ms: 1.56x faster                                                                |
| nbody                    | 134 ms                                                       | 86.7 ms: 1.55x faster                                                                |
| hexiom                   | 9.42 ms                                                      | 6.10 ms: 1.54x faster                                                                |
| unpickle_pure_python     | 312 us                                                       | 204 us: 1.53x faster                                                                 |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 613 ms: 1.53x faster                                                                 |
| scimark_sor              | 180 ms                                                       | 119 ms: 1.51x faster                                                                 |
| sqlglot_transpile        | 2.68 ms                                                      | 1.79 ms: 1.50x faster                                                                |
| pickle_pure_python       | 455 us                                                       | 310 us: 1.47x faster                                                                 |
| richards                 | 75.1 ms                                                      | 51.5 ms: 1.46x faster                                                                |
| float                    | 111 ms                                                       | 77.2 ms: 1.44x faster                                                                |
| spectral_norm            | 139 ms                                                       | 96.6 ms: 1.44x faster                                                                |
| coroutines               | 30.3 ms                                                      | 21.2 ms: 1.43x faster                                                                |
| bench_mp_pool            | 6.37 ms                                                      | 4.50 ms: 1.42x faster                                                                |
| mako                     | 14.7 ms                                                      | 10.5 ms: 1.40x faster                                                                |
| logging_simple           | 8.88 us                                                      | 6.32 us: 1.40x faster                                                                |
| logging_format           | 9.64 us                                                      | 6.91 us: 1.40x faster                                                                |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                                |
| fannkuch                 | 483 ms                                                       | 361 ms: 1.34x faster                                                                 |
| tomli_loads              | 2.92 sec                                                     | 2.18 sec: 1.34x faster                                                               |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                                 |
| nqueens                  | 115 ms                                                       | 86.6 ms: 1.33x faster                                                                |
| pprint_pformat           | 2.15 sec                                                     | 1.64 sec: 1.32x faster                                                               |
| deepcopy_memo            | 49.8 us                                                      | 37.9 us: 1.31x faster                                                                |
| pprint_safe_repr         | 1.05 sec                                                     | 801 ms: 1.31x faster                                                                 |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                                               |
| thrift                   | 1.18 ms                                                      | 900 us: 1.31x faster                                                                 |
| html5lib                 | 94.6 ms                                                      | 72.6 ms: 1.30x faster                                                                |
| tornado_http             | 157 ms                                                       | 120 ms: 1.30x faster                                                                 |
| chameleon                | 9.44 ms                                                      | 7.29 ms: 1.30x faster                                                                |
| django_template          | 50.2 ms                                                      | 38.8 ms: 1.29x faster                                                                |
| bench_thread_pool        | 1.14 ms                                                      | 884 us: 1.29x faster                                                                 |
| xml_etree_process        | 75.9 ms                                                      | 59.6 ms: 1.27x faster                                                                |
| sympy_sum                | 193 ms                                                       | 154 ms: 1.25x faster                                                                 |
| pathlib                  | 21.4 ms                                                      | 17.1 ms: 1.25x faster                                                                |
| deepcopy                 | 468 us                                                       | 379 us: 1.24x faster                                                                 |
| sqlglot_normalize        | 144 ms                                                       | 117 ms: 1.22x faster                                                                 |
| json_loads               | 30.3 us                                                      | 24.8 us: 1.22x faster                                                                |
| 2to3                     | 350 ms                                                       | 287 ms: 1.22x faster                                                                 |
| sympy_integrate          | 28.2 ms                                                      | 23.1 ms: 1.22x faster                                                                |
| scimark_fft              | 361 ms                                                       | 298 ms: 1.21x faster                                                                 |
| sympy_str                | 360 ms                                                       | 298 ms: 1.21x faster                                                                 |
| dask                     | 472 ms                                                       | 391 ms: 1.21x faster                                                                 |
| mypy2                    | 933 ms                                                       | 774 ms: 1.20x faster                                                                 |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                               |
| dulwich_log              | 81.1 ms                                                      | 67.7 ms: 1.20x faster                                                                |
| sympy_expand             | 600 ms                                                       | 504 ms: 1.19x faster                                                                 |
| genshi_text              | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                                                |
| sqlglot_optimize         | 70.1 ms                                                      | 59.0 ms: 1.19x faster                                                                |
| async_generators         | 421 ms                                                       | 356 ms: 1.18x faster                                                                 |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.32 ms: 1.18x faster                                                                |
| deepcopy_reduce          | 4.01 us                                                      | 3.42 us: 1.17x faster                                                                |
| docutils                 | 3.41 sec                                                     | 2.99 sec: 1.14x faster                                                               |
| genshi_xml               | 63.3 ms                                                      | 56.2 ms: 1.13x faster                                                                |
| aiohttp                  | 1.19 ms                                                      | 1.07 ms: 1.11x faster                                                                |
| gunicorn                 | 1.16 ms                                                      | 1.05 ms: 1.11x faster                                                                |
| regex_dna                | 261 ms                                                       | 238 ms: 1.10x faster                                                                 |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.10x faster                                                                 |
| meteor_contest           | 138 ms                                                       | 127 ms: 1.09x faster                                                                 |
| xml_etree_generate       | 92.3 ms                                                      | 85.1 ms: 1.08x faster                                                                |
| sqlite_synth             | 2.99 us                                                      | 2.77 us: 1.08x faster                                                                |
| json                     | 5.86 ms                                                      | 5.46 ms: 1.07x faster                                                                |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.07x faster                                                                 |
| regex_v8                 | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                                                |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                                 |
| unpickle_list            | 4.65 us                                                      | 4.56 us: 1.02x faster                                                                |
| asyncio_websockets       | 390 ms                                                       | 396 ms: 1.02x slower                                                                 |
| pickle                   | 9.89 us                                                      | 10.5 us: 1.06x slower                                                                |
| pickle_list              | 4.12 us                                                      | 4.44 us: 1.08x slower                                                                |
| create_gc_cycles         | 1.76 ms                                                      | 1.93 ms: 1.09x slower                                                                |
| unpickle                 | 13.5 us                                                      | 14.8 us: 1.09x slower                                                                |
| telco                    | 7.23 ms                                                      | 8.06 ms: 1.11x slower                                                                |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                                |
| regex_effbot             | 3.09 ms                                                      | 3.47 ms: 1.13x slower                                                                |
| pickle_dict              | 29.5 us                                                      | 33.3 us: 1.13x slower                                                                |
| python_startup_no_site   | 7.33 ms                                                      | 8.84 ms: 1.21x slower                                                                |
| gc_traversal             | 3.42 ms                                                      | 4.42 ms: 1.29x slower                                                                |
| coverage                 | 63.3 ms                                                      | 86.3 ms: 1.36x slower                                                                |
| Geometric mean           | (ref)                                                        | 1.31x faster                                                                         |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.11x