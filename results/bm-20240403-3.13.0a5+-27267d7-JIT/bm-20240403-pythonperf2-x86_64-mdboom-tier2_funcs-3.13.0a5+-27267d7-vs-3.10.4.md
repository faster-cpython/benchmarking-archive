# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: 27267d7
- commit date: 2024-04-03
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                |
| chameleon      | 9.44 ms                                                      | 7.44 ms: 1.27x faster                                               |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                              |
| html5lib       | 94.6 ms                                                      | 73.8 ms: 1.28x faster                                               |
| tornado_http   | 157 ms                                                       | 123 ms: 1.27x faster                                                |
| Geometric mean | (ref)                                                        | 1.22x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 361 ms: 1.92x faster                                                |
| async_tree_memoization  | 819 ms                                                       | 443 ms: 1.85x faster                                                |
| async_tree_io           | 1.60 sec                                                     | 889 ms: 1.80x faster                                                |
| async_tree_cpu_io_mixed | 936 ms                                                       | 598 ms: 1.57x faster                                                |
| Geometric mean          | (ref)                                                        | 1.78x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 111 ms                                                       | 77.6 ms: 1.43x faster                                               |
| nbody          | 134 ms                                                       | 98.4 ms: 1.36x faster                                               |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| Geometric mean | (ref)                                                        | 1.27x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 150 ms: 1.27x faster                                                |
| regex_dna      | 261 ms                                                       | 241 ms: 1.08x faster                                                |
| regex_v8       | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                               |
| regex_effbot   | 3.09 ms                                                      | 3.57 ms: 1.16x slower                                               |
| Geometric mean | (ref)                                                        | 1.05x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 306 us: 1.49x faster                                                |
| tomli_loads          | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                              |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.35x faster                                               |
| xml_etree_process    | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                               |
| unpickle_pure_python | 312 us                                                       | 240 us: 1.30x faster                                                |
| json_loads           | 30.3 us                                                      | 25.2 us: 1.21x faster                                               |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.10x faster                                                |
| xml_etree_generate   | 92.3 ms                                                      | 85.2 ms: 1.08x faster                                               |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.06x faster                                                |
| unpickle_list        | 4.65 us                                                      | 4.55 us: 1.02x faster                                               |
| pickle_dict          | 29.5 us                                                      | 31.0 us: 1.05x slower                                               |
| pickle               | 9.89 us                                                      | 10.5 us: 1.07x slower                                               |
| pickle_list          | 4.12 us                                                      | 4.46 us: 1.08x slower                                               |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                               |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                               |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.1 ms: 1.46x faster                                               |
| django_template | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                               |
| genshi_text     | 31.4 ms                                                      | 27.2 ms: 1.16x faster                                               |
| genshi_xml      | 63.3 ms                                                      | 58.8 ms: 1.08x faster                                               |
| Geometric mean  | (ref)                                                        | 1.23x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 121 us: 4.42x faster                                                |
| asyncio_tcp              | 779 ms                                                       | 371 ms: 2.10x faster                                                |
| deltablue                | 7.50 ms                                                      | 3.73 ms: 2.01x faster                                               |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                              |
| async_tree_none          | 692 ms                                                       | 361 ms: 1.92x faster                                                |
| async_tree_memoization   | 819 ms                                                       | 443 ms: 1.85x faster                                                |
| async_tree_io            | 1.60 sec                                                     | 889 ms: 1.80x faster                                                |
| logging_silent           | 167 ns                                                       | 97.2 ns: 1.72x faster                                               |
| generators               | 57.3 ms                                                      | 33.3 ms: 1.72x faster                                               |
| chaos                    | 109 ms                                                       | 66.8 ms: 1.63x faster                                               |
| raytrace                 | 489 ms                                                       | 302 ms: 1.62x faster                                                |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                               |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 598 ms: 1.57x faster                                                |
| pylint                   | 566 ms                                                       | 366 ms: 1.55x faster                                                |
| crypto_pyaes             | 119 ms                                                       | 77.9 ms: 1.53x faster                                               |
| richards_super           | 90.6 ms                                                      | 59.4 ms: 1.52x faster                                               |
| go                       | 262 ms                                                       | 174 ms: 1.51x faster                                                |
| sqlglot_transpile        | 2.68 ms                                                      | 1.80 ms: 1.49x faster                                               |
| pickle_pure_python       | 455 us                                                       | 306 us: 1.49x faster                                                |
| mako                     | 14.7 ms                                                      | 10.1 ms: 1.46x faster                                               |
| pyflate                  | 733 ms                                                       | 502 ms: 1.46x faster                                                |
| spectral_norm            | 139 ms                                                       | 95.7 ms: 1.45x faster                                               |
| scimark_monte_carlo      | 107 ms                                                       | 74.4 ms: 1.44x faster                                               |
| float                    | 111 ms                                                       | 77.6 ms: 1.43x faster                                               |
| richards                 | 75.1 ms                                                      | 52.9 ms: 1.42x faster                                               |
| nbody                    | 134 ms                                                       | 98.4 ms: 1.36x faster                                               |
| tomli_loads              | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                              |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.35x faster                                               |
| comprehensions           | 26.7 us                                                      | 20.0 us: 1.34x faster                                               |
| scimark_lu               | 167 ms                                                       | 125 ms: 1.33x faster                                                |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.33x faster                                              |
| thrift                   | 1.18 ms                                                      | 887 us: 1.32x faster                                                |
| coroutines               | 30.3 ms                                                      | 22.9 ms: 1.32x faster                                               |
| logging_format           | 9.64 us                                                      | 7.37 us: 1.31x faster                                               |
| xml_etree_process        | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                               |
| logging_simple           | 8.88 us                                                      | 6.82 us: 1.30x faster                                               |
| unpickle_pure_python     | 312 us                                                       | 240 us: 1.30x faster                                                |
| deepcopy_memo            | 49.8 us                                                      | 38.5 us: 1.29x faster                                               |
| html5lib                 | 94.6 ms                                                      | 73.8 ms: 1.28x faster                                               |
| fannkuch                 | 483 ms                                                       | 378 ms: 1.28x faster                                                |
| tornado_http             | 157 ms                                                       | 123 ms: 1.27x faster                                                |
| regex_compile            | 190 ms                                                       | 150 ms: 1.27x faster                                                |
| chameleon                | 9.44 ms                                                      | 7.44 ms: 1.27x faster                                               |
| pprint_safe_repr         | 1.05 sec                                                     | 827 ms: 1.27x faster                                                |
| bench_mp_pool            | 6.37 ms                                                      | 5.04 ms: 1.26x faster                                               |
| django_template          | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                               |
| hexiom                   | 9.42 ms                                                      | 7.56 ms: 1.25x faster                                               |
| pprint_pformat           | 2.15 sec                                                     | 1.73 sec: 1.24x faster                                              |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.13 ms: 1.23x faster                                               |
| deepcopy                 | 468 us                                                       | 388 us: 1.21x faster                                                |
| json_loads               | 30.3 us                                                      | 25.2 us: 1.21x faster                                               |
| sympy_str                | 360 ms                                                       | 302 ms: 1.19x faster                                                |
| deepcopy_reduce          | 4.01 us                                                      | 3.37 us: 1.19x faster                                               |
| sympy_sum                | 193 ms                                                       | 162 ms: 1.19x faster                                                |
| sympy_expand             | 600 ms                                                       | 510 ms: 1.18x faster                                                |
| dulwich_log              | 81.1 ms                                                      | 69.2 ms: 1.17x faster                                               |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                |
| scimark_sor              | 180 ms                                                       | 155 ms: 1.16x faster                                                |
| genshi_text              | 31.4 ms                                                      | 27.2 ms: 1.16x faster                                               |
| mdp                      | 3.01 sec                                                     | 2.62 sec: 1.15x faster                                              |
| scimark_fft              | 361 ms                                                       | 316 ms: 1.14x faster                                                |
| mypy2                    | 933 ms                                                       | 826 ms: 1.13x faster                                                |
| sqlglot_optimize         | 70.1 ms                                                      | 62.6 ms: 1.12x faster                                               |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.11x faster                                               |
| sqlite_synth             | 2.99 us                                                      | 2.69 us: 1.11x faster                                               |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                              |
| nqueens                  | 115 ms                                                       | 104 ms: 1.10x faster                                                |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.10x faster                                                |
| json                     | 5.86 ms                                                      | 5.38 ms: 1.09x faster                                               |
| xml_etree_generate       | 92.3 ms                                                      | 85.2 ms: 1.08x faster                                               |
| regex_dna                | 261 ms                                                       | 241 ms: 1.08x faster                                                |
| pathlib                  | 21.4 ms                                                      | 19.8 ms: 1.08x faster                                               |
| genshi_xml               | 63.3 ms                                                      | 58.8 ms: 1.08x faster                                               |
| async_generators         | 421 ms                                                       | 391 ms: 1.08x faster                                                |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                               |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.06x faster                                                |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.06x faster                                               |
| meteor_contest           | 138 ms                                                       | 132 ms: 1.05x faster                                                |
| regex_v8                 | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                               |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| unpickle_list            | 4.65 us                                                      | 4.55 us: 1.02x faster                                               |
| bench_thread_pool        | 1.14 ms                                                      | 1.12 ms: 1.02x faster                                               |
| create_gc_cycles         | 1.76 ms                                                      | 1.82 ms: 1.03x slower                                               |
| pickle_dict              | 29.5 us                                                      | 31.0 us: 1.05x slower                                               |
| pickle                   | 9.89 us                                                      | 10.5 us: 1.07x slower                                               |
| pickle_list              | 4.12 us                                                      | 4.46 us: 1.08x slower                                               |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                               |
| telco                    | 7.23 ms                                                      | 8.18 ms: 1.13x slower                                               |
| regex_effbot             | 3.09 ms                                                      | 3.57 ms: 1.16x slower                                               |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                               |
| coverage                 | 63.3 ms                                                      | 83.6 ms: 1.32x slower                                               |
| gc_traversal             | 3.42 ms                                                      | 4.80 ms: 1.41x slower                                               |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                               |
| Geometric mean           | (ref)                                                        | 1.25x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-27267d7-JIT/bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x