# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: cf5a818
- commit date: 2024-03-29
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                |
| chameleon      | 9.44 ms                                                      | 7.54 ms: 1.25x faster                                               |
| docutils       | 3.41 sec                                                     | 3.06 sec: 1.12x faster                                              |
| html5lib       | 94.6 ms                                                      | 73.7 ms: 1.28x faster                                               |
| tornado_http   | 157 ms                                                       | 124 ms: 1.27x faster                                                |
| Geometric mean | (ref)                                                        | 1.22x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|-------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 358 ms: 1.93x faster                                                |
| async_tree_memoization  | 819 ms                                                       | 441 ms: 1.86x faster                                                |
| async_tree_io           | 1.60 sec                                                     | 886 ms: 1.80x faster                                                |
| async_tree_cpu_io_mixed | 936 ms                                                       | 594 ms: 1.58x faster                                                |
| Geometric mean          | (ref)                                                        | 1.79x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.7 ms: 1.45x faster                                               |
| nbody          | 134 ms                                                       | 96.2 ms: 1.39x faster                                               |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| Geometric mean | (ref)                                                        | 1.28x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 149 ms: 1.28x faster                                                |
| regex_dna      | 261 ms                                                       | 241 ms: 1.08x faster                                                |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                               |
| regex_effbot   | 3.09 ms                                                      | 3.61 ms: 1.17x slower                                               |
| Geometric mean | (ref)                                                        | 1.06x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 313 us: 1.45x faster                                                |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                               |
| unpickle_pure_python | 312 us                                                       | 232 us: 1.34x faster                                                |
| tomli_loads          | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                              |
| xml_etree_process    | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                               |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                               |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                |
| xml_etree_generate   | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                               |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.08x faster                                                |
| pickle_dict          | 29.5 us                                                      | 30.7 us: 1.04x slower                                               |
| pickle_list          | 4.12 us                                                      | 4.37 us: 1.06x slower                                               |
| pickle               | 9.89 us                                                      | 10.6 us: 1.08x slower                                               |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                        |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                               |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                               |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.97 ms: 1.48x faster                                               |
| django_template | 50.2 ms                                                      | 40.0 ms: 1.25x faster                                               |
| genshi_text     | 31.4 ms                                                      | 27.1 ms: 1.16x faster                                               |
| genshi_xml      | 63.3 ms                                                      | 59.6 ms: 1.06x faster                                               |
| Geometric mean  | (ref)                                                        | 1.23x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 121 us: 4.43x faster                                                |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                |
| deltablue                | 7.50 ms                                                      | 3.74 ms: 2.00x faster                                               |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                              |
| async_tree_none          | 692 ms                                                       | 358 ms: 1.93x faster                                                |
| async_tree_memoization   | 819 ms                                                       | 441 ms: 1.86x faster                                                |
| async_tree_io            | 1.60 sec                                                     | 886 ms: 1.80x faster                                                |
| logging_silent           | 167 ns                                                       | 97.0 ns: 1.72x faster                                               |
| generators               | 57.3 ms                                                      | 33.6 ms: 1.70x faster                                               |
| raytrace                 | 489 ms                                                       | 297 ms: 1.64x faster                                                |
| chaos                    | 109 ms                                                       | 66.2 ms: 1.64x faster                                               |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.59x faster                                               |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 594 ms: 1.58x faster                                                |
| richards_super           | 90.6 ms                                                      | 57.6 ms: 1.57x faster                                               |
| pylint                   | 566 ms                                                       | 363 ms: 1.56x faster                                                |
| crypto_pyaes             | 119 ms                                                       | 77.4 ms: 1.54x faster                                               |
| richards                 | 75.1 ms                                                      | 50.0 ms: 1.50x faster                                               |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.48x faster                                               |
| spectral_norm            | 139 ms                                                       | 94.0 ms: 1.48x faster                                               |
| mako                     | 14.7 ms                                                      | 9.97 ms: 1.48x faster                                               |
| scimark_monte_carlo      | 107 ms                                                       | 73.5 ms: 1.46x faster                                               |
| go                       | 262 ms                                                       | 179 ms: 1.46x faster                                                |
| pickle_pure_python       | 455 us                                                       | 313 us: 1.45x faster                                                |
| float                    | 111 ms                                                       | 76.7 ms: 1.45x faster                                               |
| pyflate                  | 733 ms                                                       | 516 ms: 1.42x faster                                                |
| nbody                    | 134 ms                                                       | 96.2 ms: 1.39x faster                                               |
| scimark_lu               | 167 ms                                                       | 120 ms: 1.39x faster                                                |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                               |
| logging_simple           | 8.88 us                                                      | 6.56 us: 1.35x faster                                               |
| logging_format           | 9.64 us                                                      | 7.14 us: 1.35x faster                                               |
| unpickle_pure_python     | 312 us                                                       | 232 us: 1.34x faster                                                |
| comprehensions           | 26.7 us                                                      | 19.9 us: 1.34x faster                                               |
| coroutines               | 30.3 ms                                                      | 22.6 ms: 1.34x faster                                               |
| tomli_loads              | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                              |
| thrift                   | 1.18 ms                                                      | 885 us: 1.33x faster                                                |
| xml_etree_process        | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                               |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                              |
| deepcopy_memo            | 49.8 us                                                      | 38.1 us: 1.31x faster                                               |
| html5lib                 | 94.6 ms                                                      | 73.7 ms: 1.28x faster                                               |
| regex_compile            | 190 ms                                                       | 149 ms: 1.28x faster                                                |
| pprint_safe_repr         | 1.05 sec                                                     | 823 ms: 1.27x faster                                                |
| tornado_http             | 157 ms                                                       | 124 ms: 1.27x faster                                                |
| pprint_pformat           | 2.15 sec                                                     | 1.70 sec: 1.27x faster                                              |
| bench_mp_pool            | 6.37 ms                                                      | 5.05 ms: 1.26x faster                                               |
| fannkuch                 | 483 ms                                                       | 384 ms: 1.26x faster                                                |
| django_template          | 50.2 ms                                                      | 40.0 ms: 1.25x faster                                               |
| hexiom                   | 9.42 ms                                                      | 7.52 ms: 1.25x faster                                               |
| chameleon                | 9.44 ms                                                      | 7.54 ms: 1.25x faster                                               |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.17 ms: 1.22x faster                                               |
| deepcopy                 | 468 us                                                       | 389 us: 1.20x faster                                                |
| sympy_sum                | 193 ms                                                       | 161 ms: 1.20x faster                                                |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                               |
| sympy_str                | 360 ms                                                       | 302 ms: 1.19x faster                                                |
| deepcopy_reduce          | 4.01 us                                                      | 3.36 us: 1.19x faster                                               |
| dulwich_log              | 81.1 ms                                                      | 68.7 ms: 1.18x faster                                               |
| sympy_expand             | 600 ms                                                       | 509 ms: 1.18x faster                                                |
| dask                     | 472 ms                                                       | 404 ms: 1.17x faster                                                |
| scimark_sor              | 180 ms                                                       | 154 ms: 1.17x faster                                                |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                |
| genshi_text              | 31.4 ms                                                      | 27.1 ms: 1.16x faster                                               |
| mdp                      | 3.01 sec                                                     | 2.61 sec: 1.15x faster                                              |
| scimark_fft              | 361 ms                                                       | 315 ms: 1.15x faster                                                |
| sqlglot_normalize        | 144 ms                                                       | 126 ms: 1.14x faster                                                |
| mypy2                    | 933 ms                                                       | 827 ms: 1.13x faster                                                |
| sympy_integrate          | 28.2 ms                                                      | 25.0 ms: 1.13x faster                                               |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                |
| docutils                 | 3.41 sec                                                     | 3.06 sec: 1.12x faster                                              |
| nqueens                  | 115 ms                                                       | 103 ms: 1.11x faster                                                |
| sqlglot_optimize         | 70.1 ms                                                      | 63.1 ms: 1.11x faster                                               |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                               |
| pathlib                  | 21.4 ms                                                      | 19.3 ms: 1.11x faster                                               |
| xml_etree_generate       | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                               |
| async_generators         | 421 ms                                                       | 387 ms: 1.09x faster                                                |
| json                     | 5.86 ms                                                      | 5.40 ms: 1.09x faster                                               |
| regex_dna                | 261 ms                                                       | 241 ms: 1.08x faster                                                |
| gunicorn                 | 1.16 ms                                                      | 1.08 ms: 1.08x faster                                               |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.08x faster                                                |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                               |
| genshi_xml               | 63.3 ms                                                      | 59.6 ms: 1.06x faster                                               |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                               |
| meteor_contest           | 138 ms                                                       | 132 ms: 1.05x faster                                                |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| bench_thread_pool        | 1.14 ms                                                      | 1.11 ms: 1.03x faster                                               |
| asyncio_websockets       | 390 ms                                                       | 386 ms: 1.01x faster                                                |
| create_gc_cycles         | 1.76 ms                                                      | 1.80 ms: 1.02x slower                                               |
| pickle_dict              | 29.5 us                                                      | 30.7 us: 1.04x slower                                               |
| pickle_list              | 4.12 us                                                      | 4.37 us: 1.06x slower                                               |
| pickle                   | 9.89 us                                                      | 10.6 us: 1.08x slower                                               |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                               |
| telco                    | 7.23 ms                                                      | 8.15 ms: 1.13x slower                                               |
| regex_effbot             | 3.09 ms                                                      | 3.61 ms: 1.17x slower                                               |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                               |
| gc_traversal             | 3.42 ms                                                      | 4.56 ms: 1.34x slower                                               |
| coverage                 | 63.3 ms                                                      | 86.4 ms: 1.37x slower                                               |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                               |
| Geometric mean           | (ref)                                                        | 1.25x faster                                                        |

Benchmark hidden because not significant (2): unpack_sequence, unpickle_list
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-cf5a818-JIT/bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x