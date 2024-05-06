# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 297 ms: 1.18x faster                                                      |
| chameleon      | 9.44 ms                                                      | 7.43 ms: 1.27x faster                                                     |
| docutils       | 3.41 sec                                                     | 3.08 sec: 1.11x faster                                                    |
| html5lib       | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                     |
| tornado_http   | 157 ms                                                       | 121 ms: 1.29x faster                                                      |
| Geometric mean | (ref)                                                        | 1.23x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 856 ms: 1.87x faster                                                      |
| async_tree_memoization  | 819 ms                                                       | 446 ms: 1.84x faster                                                      |
| async_tree_none         | 692 ms                                                       | 378 ms: 1.83x faster                                                      |
| async_tree_cpu_io_mixed | 936 ms                                                       | 611 ms: 1.53x faster                                                      |
| Geometric mean          | (ref)                                                        | 1.76x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.2 ms: 1.48x faster                                                     |
| nbody          | 134 ms                                                       | 103 ms: 1.30x faster                                                      |
| pidigits       | 271 ms                                                       | 262 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                        | 1.26x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.29x faster                                                      |
| regex_dna      | 261 ms                                                       | 241 ms: 1.09x faster                                                      |
| regex_effbot   | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                     |
| Geometric mean | (ref)                                                        | 1.06x faster                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 313 us: 1.46x faster                                                      |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                     |
| tomli_loads          | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                                    |
| unpickle_pure_python | 312 us                                                       | 230 us: 1.36x faster                                                      |
| xml_etree_process    | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                                     |
| json_loads           | 30.3 us                                                      | 25.4 us: 1.19x faster                                                     |
| xml_etree_parse      | 160 ms                                                       | 142 ms: 1.13x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                       | 99.8 ms: 1.11x faster                                                     |
| xml_etree_generate   | 92.3 ms                                                      | 83.5 ms: 1.10x faster                                                     |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                     |
| pickle_dict          | 29.5 us                                                      | 30.8 us: 1.04x slower                                                     |
| pickle_list          | 4.12 us                                                      | 4.38 us: 1.06x slower                                                     |
| unpickle             | 13.5 us                                                      | 14.8 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.14x faster                                                              |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                     |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.1 ms: 1.45x faster                                                     |
| genshi_text    | 31.4 ms                                                      | 26.1 ms: 1.21x faster                                                     |
| genshi_xml     | 63.3 ms                                                      | 56.4 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                        | 1.25x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 118 us: 4.54x faster                                                      |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.09x faster                                                      |
| deltablue                | 7.50 ms                                                      | 3.75 ms: 2.00x faster                                                     |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                    |
| async_tree_io            | 1.60 sec                                                     | 856 ms: 1.87x faster                                                      |
| async_tree_memoization   | 819 ms                                                       | 446 ms: 1.84x faster                                                      |
| async_tree_none          | 692 ms                                                       | 378 ms: 1.83x faster                                                      |
| raytrace                 | 489 ms                                                       | 270 ms: 1.81x faster                                                      |
| richards_super           | 90.6 ms                                                      | 52.3 ms: 1.73x faster                                                     |
| logging_silent           | 167 ns                                                       | 97.2 ns: 1.72x faster                                                     |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.71x faster                                                     |
| pylint                   | 566 ms                                                       | 335 ms: 1.69x faster                                                      |
| chaos                    | 109 ms                                                       | 64.7 ms: 1.68x faster                                                     |
| richards                 | 75.1 ms                                                      | 45.7 ms: 1.64x faster                                                     |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.59x faster                                                     |
| scimark_monte_carlo      | 107 ms                                                       | 69.4 ms: 1.55x faster                                                     |
| crypto_pyaes             | 119 ms                                                       | 77.3 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 611 ms: 1.53x faster                                                      |
| sqlglot_transpile        | 2.68 ms                                                      | 1.80 ms: 1.49x faster                                                     |
| spectral_norm            | 139 ms                                                       | 93.4 ms: 1.49x faster                                                     |
| go                       | 262 ms                                                       | 177 ms: 1.48x faster                                                      |
| float                    | 111 ms                                                       | 75.2 ms: 1.48x faster                                                     |
| pickle_pure_python       | 455 us                                                       | 313 us: 1.46x faster                                                      |
| pyflate                  | 733 ms                                                       | 504 ms: 1.46x faster                                                      |
| mako                     | 14.7 ms                                                      | 10.1 ms: 1.45x faster                                                     |
| scimark_lu               | 167 ms                                                       | 118 ms: 1.41x faster                                                      |
| logging_simple           | 8.88 us                                                      | 6.36 us: 1.40x faster                                                     |
| comprehensions           | 26.7 us                                                      | 19.3 us: 1.39x faster                                                     |
| logging_format           | 9.64 us                                                      | 7.02 us: 1.37x faster                                                     |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                     |
| coroutines               | 30.3 ms                                                      | 22.3 ms: 1.36x faster                                                     |
| tomli_loads              | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                                    |
| unpickle_pure_python     | 312 us                                                       | 230 us: 1.36x faster                                                      |
| pycparser                | 1.67 sec                                                     | 1.24 sec: 1.35x faster                                                    |
| bench_mp_pool            | 6.37 ms                                                      | 4.74 ms: 1.34x faster                                                     |
| deepcopy_memo            | 49.8 us                                                      | 37.2 us: 1.34x faster                                                     |
| thrift                   | 1.18 ms                                                      | 880 us: 1.34x faster                                                      |
| hexiom                   | 9.42 ms                                                      | 7.13 ms: 1.32x faster                                                     |
| xml_etree_process        | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                                     |
| nbody                    | 134 ms                                                       | 103 ms: 1.30x faster                                                      |
| html5lib                 | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                     |
| tornado_http             | 157 ms                                                       | 121 ms: 1.29x faster                                                      |
| regex_compile            | 190 ms                                                       | 148 ms: 1.29x faster                                                      |
| chameleon                | 9.44 ms                                                      | 7.43 ms: 1.27x faster                                                     |
| pprint_pformat           | 2.15 sec                                                     | 1.70 sec: 1.26x faster                                                    |
| pprint_safe_repr         | 1.05 sec                                                     | 833 ms: 1.26x faster                                                      |
| deepcopy                 | 468 us                                                       | 379 us: 1.23x faster                                                      |
| fannkuch                 | 483 ms                                                       | 393 ms: 1.23x faster                                                      |
| genshi_text              | 31.4 ms                                                      | 26.1 ms: 1.21x faster                                                     |
| bench_thread_pool        | 1.14 ms                                                      | 951 us: 1.20x faster                                                      |
| dulwich_log              | 81.1 ms                                                      | 67.7 ms: 1.20x faster                                                     |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.24 ms: 1.20x faster                                                     |
| json_loads               | 30.3 us                                                      | 25.4 us: 1.19x faster                                                     |
| scimark_sor              | 180 ms                                                       | 152 ms: 1.19x faster                                                      |
| 2to3                     | 350 ms                                                       | 297 ms: 1.18x faster                                                      |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                      |
| deepcopy_reduce          | 4.01 us                                                      | 3.43 us: 1.17x faster                                                     |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                      |
| sympy_sum                | 193 ms                                                       | 165 ms: 1.17x faster                                                      |
| sympy_expand             | 600 ms                                                       | 516 ms: 1.16x faster                                                      |
| sympy_str                | 360 ms                                                       | 310 ms: 1.16x faster                                                      |
| nqueens                  | 115 ms                                                       | 100 ms: 1.14x faster                                                      |
| mdp                      | 3.01 sec                                                     | 2.63 sec: 1.14x faster                                                    |
| mypy2                    | 933 ms                                                       | 820 ms: 1.14x faster                                                      |
| scimark_fft              | 361 ms                                                       | 319 ms: 1.13x faster                                                      |
| xml_etree_parse          | 160 ms                                                       | 142 ms: 1.13x faster                                                      |
| genshi_xml               | 63.3 ms                                                      | 56.4 ms: 1.12x faster                                                     |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.12x faster                                                     |
| sqlglot_optimize         | 70.1 ms                                                      | 62.9 ms: 1.12x faster                                                     |
| sympy_integrate          | 28.2 ms                                                      | 25.4 ms: 1.11x faster                                                     |
| docutils                 | 3.41 sec                                                     | 3.08 sec: 1.11x faster                                                    |
| xml_etree_iterparse      | 110 ms                                                       | 99.8 ms: 1.11x faster                                                     |
| xml_etree_generate       | 92.3 ms                                                      | 83.5 ms: 1.10x faster                                                     |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                     |
| async_generators         | 421 ms                                                       | 383 ms: 1.10x faster                                                      |
| regex_dna                | 261 ms                                                       | 241 ms: 1.09x faster                                                      |
| json                     | 5.86 ms                                                      | 5.48 ms: 1.07x faster                                                     |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                     |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                     |
| meteor_contest           | 138 ms                                                       | 133 ms: 1.04x faster                                                      |
| pidigits                 | 271 ms                                                       | 262 ms: 1.04x faster                                                      |
| pickle                   | 9.89 us                                                      | 10.3 us: 1.04x slower                                                     |
| pickle_dict              | 29.5 us                                                      | 30.8 us: 1.04x slower                                                     |
| create_gc_cycles         | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                     |
| pickle_list              | 4.12 us                                                      | 4.38 us: 1.06x slower                                                     |
| unpickle                 | 13.5 us                                                      | 14.8 us: 1.10x slower                                                     |
| regex_effbot             | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                     |
| telco                    | 7.23 ms                                                      | 8.29 ms: 1.15x slower                                                     |
| python_startup           | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                     |
| coverage                 | 63.3 ms                                                      | 80.7 ms: 1.28x slower                                                     |
| gc_traversal             | 3.42 ms                                                      | 4.44 ms: 1.30x slower                                                     |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                     |
| Geometric mean           | (ref)                                                        | 1.27x faster                                                              |

Benchmark hidden because not significant (3): regex_v8, unpickle_list, asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x