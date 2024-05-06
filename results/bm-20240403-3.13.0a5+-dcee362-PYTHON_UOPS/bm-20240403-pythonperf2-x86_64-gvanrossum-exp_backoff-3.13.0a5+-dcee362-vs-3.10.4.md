# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 316 ms: 1.11x faster                                                    |
| chameleon      | 9.44 ms                                                      | 7.77 ms: 1.21x faster                                                   |
| docutils       | 3.41 sec                                                     | 3.24 sec: 1.05x faster                                                  |
| html5lib       | 94.6 ms                                                      | 79.7 ms: 1.19x faster                                                   |
| tornado_http   | 157 ms                                                       | 129 ms: 1.22x faster                                                    |
| Geometric mean | (ref)                                                        | 1.15x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization  | 819 ms                                                       | 463 ms: 1.77x faster                                                    |
| async_tree_io           | 1.60 sec                                                     | 912 ms: 1.75x faster                                                    |
| async_tree_none         | 692 ms                                                       | 395 ms: 1.75x faster                                                    |
| async_tree_cpu_io_mixed | 936 ms                                                       | 628 ms: 1.49x faster                                                    |
| Geometric mean          | (ref)                                                        | 1.69x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 111 ms                                                       | 91.6 ms: 1.21x faster                                                   |
| nbody          | 134 ms                                                       | 114 ms: 1.18x faster                                                    |
| pidigits       | 271 ms                                                       | 266 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                        | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 261 ms                                                       | 236 ms: 1.11x faster                                                    |
| regex_v8       | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                   |
| regex_compile  | 190 ms                                                       | 196 ms: 1.03x slower                                                    |
| regex_effbot   | 3.09 ms                                                      | 3.58 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 326 us: 1.39x faster                                                    |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                   |
| xml_etree_process    | 75.9 ms                                                      | 62.5 ms: 1.21x faster                                                   |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                   |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                    |
| tomli_loads          | 2.92 sec                                                     | 2.74 sec: 1.07x faster                                                  |
| unpickle_pure_python | 312 us                                                       | 293 us: 1.06x faster                                                    |
| xml_etree_generate   | 92.3 ms                                                      | 90.3 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 110 ms                                                       | 108 ms: 1.02x faster                                                    |
| unpickle_list        | 4.65 us                                                      | 4.77 us: 1.03x slower                                                   |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                   |
| pickle_dict          | 29.5 us                                                      | 31.2 us: 1.06x slower                                                   |
| pickle_list          | 4.12 us                                                      | 4.38 us: 1.06x slower                                                   |
| unpickle             | 13.5 us                                                      | 14.8 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                   |
| python_startup_no_site | 7.33 ms                                                      | 11.2 ms: 1.53x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text    | 31.4 ms                                                      | 27.9 ms: 1.13x faster                                                   |
| mako           | 14.7 ms                                                      | 13.2 ms: 1.11x faster                                                   |
| genshi_xml     | 63.3 ms                                                      | 62.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 127 us: 4.23x faster                                                    |
| asyncio_tcp              | 779 ms                                                       | 383 ms: 2.04x faster                                                    |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.60 sec: 1.94x faster                                                  |
| deltablue                | 7.50 ms                                                      | 4.14 ms: 1.81x faster                                                   |
| async_tree_memoization   | 819 ms                                                       | 463 ms: 1.77x faster                                                    |
| async_tree_io            | 1.60 sec                                                     | 912 ms: 1.75x faster                                                    |
| async_tree_none          | 692 ms                                                       | 395 ms: 1.75x faster                                                    |
| generators               | 57.3 ms                                                      | 33.7 ms: 1.70x faster                                                   |
| pylint                   | 566 ms                                                       | 347 ms: 1.63x faster                                                    |
| logging_silent           | 167 ns                                                       | 103 ns: 1.62x faster                                                    |
| raytrace                 | 489 ms                                                       | 304 ms: 1.61x faster                                                    |
| chaos                    | 109 ms                                                       | 72.5 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 628 ms: 1.49x faster                                                    |
| richards_super           | 90.6 ms                                                      | 60.9 ms: 1.49x faster                                                   |
| sqlglot_parse            | 2.24 ms                                                      | 1.55 ms: 1.44x faster                                                   |
| pickle_pure_python       | 455 us                                                       | 326 us: 1.39x faster                                                    |
| richards                 | 75.1 ms                                                      | 54.2 ms: 1.39x faster                                                   |
| sqlglot_transpile        | 2.68 ms                                                      | 1.95 ms: 1.37x faster                                                   |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                   |
| crypto_pyaes             | 119 ms                                                       | 87.7 ms: 1.36x faster                                                   |
| logging_simple           | 8.88 us                                                      | 6.59 us: 1.35x faster                                                   |
| coroutines               | 30.3 ms                                                      | 22.6 ms: 1.34x faster                                                   |
| bench_mp_pool            | 6.37 ms                                                      | 4.77 ms: 1.34x faster                                                   |
| thrift                   | 1.18 ms                                                      | 882 us: 1.33x faster                                                    |
| logging_format           | 9.64 us                                                      | 7.29 us: 1.32x faster                                                   |
| go                       | 262 ms                                                       | 210 ms: 1.25x faster                                                    |
| pycparser                | 1.67 sec                                                     | 1.35 sec: 1.24x faster                                                  |
| scimark_lu               | 167 ms                                                       | 135 ms: 1.23x faster                                                    |
| tornado_http             | 157 ms                                                       | 129 ms: 1.22x faster                                                    |
| chameleon                | 9.44 ms                                                      | 7.77 ms: 1.21x faster                                                   |
| pyflate                  | 733 ms                                                       | 604 ms: 1.21x faster                                                    |
| xml_etree_process        | 75.9 ms                                                      | 62.5 ms: 1.21x faster                                                   |
| float                    | 111 ms                                                       | 91.6 ms: 1.21x faster                                                   |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                   |
| bench_thread_pool        | 1.14 ms                                                      | 954 us: 1.20x faster                                                    |
| html5lib                 | 94.6 ms                                                      | 79.7 ms: 1.19x faster                                                   |
| nbody                    | 134 ms                                                       | 114 ms: 1.18x faster                                                    |
| scimark_monte_carlo      | 107 ms                                                       | 92.2 ms: 1.17x faster                                                   |
| deepcopy_memo            | 49.8 us                                                      | 43.7 us: 1.14x faster                                                   |
| scimark_sor              | 180 ms                                                       | 159 ms: 1.13x faster                                                    |
| dask                     | 472 ms                                                       | 419 ms: 1.13x faster                                                    |
| mdp                      | 3.01 sec                                                     | 2.67 sec: 1.13x faster                                                  |
| genshi_text              | 31.4 ms                                                      | 27.9 ms: 1.13x faster                                                   |
| deepcopy                 | 468 us                                                       | 417 us: 1.12x faster                                                    |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                    |
| mako                     | 14.7 ms                                                      | 13.2 ms: 1.11x faster                                                   |
| sqlglot_normalize        | 144 ms                                                       | 129 ms: 1.11x faster                                                    |
| 2to3                     | 350 ms                                                       | 316 ms: 1.11x faster                                                    |
| regex_dna                | 261 ms                                                       | 236 ms: 1.11x faster                                                    |
| mypy2                    | 933 ms                                                       | 852 ms: 1.10x faster                                                    |
| deepcopy_reduce          | 4.01 us                                                      | 3.66 us: 1.09x faster                                                   |
| async_generators         | 421 ms                                                       | 385 ms: 1.09x faster                                                    |
| pprint_pformat           | 2.15 sec                                                     | 1.98 sec: 1.09x faster                                                  |
| pprint_safe_repr         | 1.05 sec                                                     | 971 ms: 1.08x faster                                                    |
| json                     | 5.86 ms                                                      | 5.43 ms: 1.08x faster                                                   |
| comprehensions           | 26.7 us                                                      | 24.7 us: 1.08x faster                                                   |
| sqlite_synth             | 2.99 us                                                      | 2.78 us: 1.08x faster                                                   |
| sympy_sum                | 193 ms                                                       | 180 ms: 1.07x faster                                                    |
| tomli_loads              | 2.92 sec                                                     | 2.74 sec: 1.07x faster                                                  |
| unpickle_pure_python     | 312 us                                                       | 293 us: 1.06x faster                                                    |
| sympy_integrate          | 28.2 ms                                                      | 26.5 ms: 1.06x faster                                                   |
| regex_v8                 | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                   |
| docutils                 | 3.41 sec                                                     | 3.24 sec: 1.05x faster                                                  |
| dulwich_log              | 81.1 ms                                                      | 77.1 ms: 1.05x faster                                                   |
| sqlglot_optimize         | 70.1 ms                                                      | 67.0 ms: 1.05x faster                                                   |
| sympy_expand             | 600 ms                                                       | 577 ms: 1.04x faster                                                    |
| aiohttp                  | 1.19 ms                                                      | 1.14 ms: 1.04x faster                                                   |
| sympy_str                | 360 ms                                                       | 347 ms: 1.04x faster                                                    |
| pathlib                  | 21.4 ms                                                      | 20.6 ms: 1.04x faster                                                   |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.04x faster                                                   |
| fannkuch                 | 483 ms                                                       | 466 ms: 1.04x faster                                                    |
| xml_etree_generate       | 92.3 ms                                                      | 90.3 ms: 1.02x faster                                                   |
| xml_etree_iterparse      | 110 ms                                                       | 108 ms: 1.02x faster                                                    |
| pidigits                 | 271 ms                                                       | 266 ms: 1.02x faster                                                    |
| genshi_xml               | 63.3 ms                                                      | 62.3 ms: 1.02x faster                                                   |
| nqueens                  | 115 ms                                                       | 114 ms: 1.01x faster                                                    |
| spectral_norm            | 139 ms                                                       | 140 ms: 1.01x slower                                                    |
| unpickle_list            | 4.65 us                                                      | 4.77 us: 1.03x slower                                                   |
| meteor_contest           | 138 ms                                                       | 142 ms: 1.03x slower                                                    |
| regex_compile            | 190 ms                                                       | 196 ms: 1.03x slower                                                    |
| hexiom                   | 9.42 ms                                                      | 9.76 ms: 1.04x slower                                                   |
| create_gc_cycles         | 1.76 ms                                                      | 1.85 ms: 1.05x slower                                                   |
| pickle                   | 9.89 us                                                      | 10.4 us: 1.05x slower                                                   |
| pickle_dict              | 29.5 us                                                      | 31.2 us: 1.06x slower                                                   |
| pickle_list              | 4.12 us                                                      | 4.38 us: 1.06x slower                                                   |
| unpickle                 | 13.5 us                                                      | 14.8 us: 1.10x slower                                                   |
| scimark_fft              | 361 ms                                                       | 404 ms: 1.12x slower                                                    |
| python_startup           | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                   |
| regex_effbot             | 3.09 ms                                                      | 3.58 ms: 1.16x slower                                                   |
| telco                    | 7.23 ms                                                      | 8.59 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 6.14 ms: 1.21x slower                                                   |
| gc_traversal             | 3.42 ms                                                      | 4.69 ms: 1.37x slower                                                   |
| coverage                 | 63.3 ms                                                      | 87.8 ms: 1.39x slower                                                   |
| python_startup_no_site   | 7.33 ms                                                      | 11.2 ms: 1.53x slower                                                   |
| Geometric mean           | (ref)                                                        | 1.17x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-dcee362-PYTHON_UOPS/bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.11x