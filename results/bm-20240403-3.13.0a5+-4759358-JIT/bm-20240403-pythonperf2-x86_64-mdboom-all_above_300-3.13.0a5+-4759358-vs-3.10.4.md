# Results vs. 3.10.4

- fork: mdboom
- ref: all_above_300
- machine: linux-x86_64
- commit hash: 4759358
- commit date: 2024-04-03
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 301 ms: 1.16x faster                                                  |
| chameleon      | 9.44 ms                                                      | 7.23 ms: 1.31x faster                                                 |
| docutils       | 3.41 sec                                                     | 3.05 sec: 1.12x faster                                                |
| html5lib       | 94.6 ms                                                      | 73.5 ms: 1.29x faster                                                 |
| tornado_http   | 157 ms                                                       | 125 ms: 1.26x faster                                                  |
| Geometric mean | (ref)                                                        | 1.22x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 380 ms: 1.82x faster                                                  |
| async_tree_memoization  | 819 ms                                                       | 455 ms: 1.80x faster                                                  |
| async_tree_io           | 1.60 sec                                                     | 909 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed | 936 ms                                                       | 600 ms: 1.56x faster                                                  |
| Geometric mean          | (ref)                                                        | 1.73x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 95.4 ms: 1.41x faster                                                 |
| float          | 111 ms                                                       | 79.5 ms: 1.40x faster                                                 |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 149 ms: 1.27x faster                                                  |
| regex_dna      | 261 ms                                                       | 246 ms: 1.06x faster                                                  |
| regex_v8       | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                 |
| regex_effbot   | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 308 us: 1.48x faster                                                  |
| json_dumps           | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                 |
| tomli_loads          | 2.92 sec                                                     | 2.21 sec: 1.32x faster                                                |
| xml_etree_process    | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                                 |
| unpickle_pure_python | 312 us                                                       | 241 us: 1.30x faster                                                  |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                 |
| xml_etree_parse      | 160 ms                                                       | 142 ms: 1.13x faster                                                  |
| xml_etree_generate   | 92.3 ms                                                      | 84.3 ms: 1.09x faster                                                 |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.09x faster                                                  |
| unpickle_list        | 4.65 us                                                      | 4.71 us: 1.01x slower                                                 |
| pickle_list          | 4.12 us                                                      | 4.38 us: 1.06x slower                                                 |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                 |
| unpickle             | 13.5 us                                                      | 14.9 us: 1.11x slower                                                 |
| pickle_dict          | 29.5 us                                                      | 32.7 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.92 ms: 1.48x faster                                                 |
| django_template | 50.2 ms                                                      | 40.2 ms: 1.25x faster                                                 |
| genshi_text     | 31.4 ms                                                      | 26.7 ms: 1.18x faster                                                 |
| genshi_xml      | 63.3 ms                                                      | 60.3 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.23x faster                                                          |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 120 us: 4.49x faster                                                  |
| asyncio_tcp              | 779 ms                                                       | 370 ms: 2.10x faster                                                  |
| deltablue                | 7.50 ms                                                      | 3.76 ms: 1.99x faster                                                 |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                |
| async_tree_none          | 692 ms                                                       | 380 ms: 1.82x faster                                                  |
| async_tree_memoization   | 819 ms                                                       | 455 ms: 1.80x faster                                                  |
| async_tree_io            | 1.60 sec                                                     | 909 ms: 1.76x faster                                                  |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.71x faster                                                 |
| logging_silent           | 167 ns                                                       | 97.7 ns: 1.71x faster                                                 |
| chaos                    | 109 ms                                                       | 67.9 ms: 1.60x faster                                                 |
| raytrace                 | 489 ms                                                       | 306 ms: 1.60x faster                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.56x faster                                                 |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 600 ms: 1.56x faster                                                  |
| richards_super           | 90.6 ms                                                      | 58.3 ms: 1.55x faster                                                 |
| pylint                   | 566 ms                                                       | 365 ms: 1.55x faster                                                  |
| crypto_pyaes             | 119 ms                                                       | 78.7 ms: 1.52x faster                                                 |
| mako                     | 14.7 ms                                                      | 9.92 ms: 1.48x faster                                                 |
| pickle_pure_python       | 455 us                                                       | 308 us: 1.48x faster                                                  |
| sqlglot_transpile        | 2.68 ms                                                      | 1.83 ms: 1.47x faster                                                 |
| go                       | 262 ms                                                       | 180 ms: 1.46x faster                                                  |
| richards                 | 75.1 ms                                                      | 51.9 ms: 1.45x faster                                                 |
| spectral_norm            | 139 ms                                                       | 96.8 ms: 1.44x faster                                                 |
| scimark_monte_carlo      | 107 ms                                                       | 74.8 ms: 1.44x faster                                                 |
| nbody                    | 134 ms                                                       | 95.4 ms: 1.41x faster                                                 |
| float                    | 111 ms                                                       | 79.5 ms: 1.40x faster                                                 |
| pyflate                  | 733 ms                                                       | 525 ms: 1.40x faster                                                  |
| comprehensions           | 26.7 us                                                      | 19.8 us: 1.35x faster                                                 |
| logging_format           | 9.64 us                                                      | 7.15 us: 1.35x faster                                                 |
| json_dumps               | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                 |
| coroutines               | 30.3 ms                                                      | 22.6 ms: 1.34x faster                                                 |
| logging_simple           | 8.88 us                                                      | 6.66 us: 1.33x faster                                                 |
| scimark_lu               | 167 ms                                                       | 126 ms: 1.33x faster                                                  |
| tomli_loads              | 2.92 sec                                                     | 2.21 sec: 1.32x faster                                                |
| thrift                   | 1.18 ms                                                      | 893 us: 1.32x faster                                                  |
| xml_etree_process        | 75.9 ms                                                      | 58.0 ms: 1.31x faster                                                 |
| chameleon                | 9.44 ms                                                      | 7.23 ms: 1.31x faster                                                 |
| pycparser                | 1.67 sec                                                     | 1.29 sec: 1.30x faster                                                |
| deepcopy_memo            | 49.8 us                                                      | 38.4 us: 1.30x faster                                                 |
| unpickle_pure_python     | 312 us                                                       | 241 us: 1.30x faster                                                  |
| html5lib                 | 94.6 ms                                                      | 73.5 ms: 1.29x faster                                                 |
| regex_compile            | 190 ms                                                       | 149 ms: 1.27x faster                                                  |
| tornado_http             | 157 ms                                                       | 125 ms: 1.26x faster                                                  |
| django_template          | 50.2 ms                                                      | 40.2 ms: 1.25x faster                                                 |
| pprint_pformat           | 2.15 sec                                                     | 1.75 sec: 1.23x faster                                                |
| fannkuch                 | 483 ms                                                       | 393 ms: 1.23x faster                                                  |
| pprint_safe_repr         | 1.05 sec                                                     | 858 ms: 1.22x faster                                                  |
| bench_mp_pool            | 6.37 ms                                                      | 5.22 ms: 1.22x faster                                                 |
| hexiom                   | 9.42 ms                                                      | 7.75 ms: 1.22x faster                                                 |
| deepcopy                 | 468 us                                                       | 390 us: 1.20x faster                                                  |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                 |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.25 ms: 1.20x faster                                                 |
| deepcopy_reduce          | 4.01 us                                                      | 3.37 us: 1.19x faster                                                 |
| sympy_sum                | 193 ms                                                       | 163 ms: 1.18x faster                                                  |
| sympy_str                | 360 ms                                                       | 305 ms: 1.18x faster                                                  |
| genshi_text              | 31.4 ms                                                      | 26.7 ms: 1.18x faster                                                 |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                  |
| sympy_expand             | 600 ms                                                       | 513 ms: 1.17x faster                                                  |
| dulwich_log              | 81.1 ms                                                      | 69.4 ms: 1.17x faster                                                 |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                  |
| scimark_sor              | 180 ms                                                       | 155 ms: 1.16x faster                                                  |
| 2to3                     | 350 ms                                                       | 301 ms: 1.16x faster                                                  |
| mdp                      | 3.01 sec                                                     | 2.62 sec: 1.15x faster                                                |
| scimark_fft              | 361 ms                                                       | 320 ms: 1.13x faster                                                  |
| mypy2                    | 933 ms                                                       | 828 ms: 1.13x faster                                                  |
| xml_etree_parse          | 160 ms                                                       | 142 ms: 1.13x faster                                                  |
| docutils                 | 3.41 sec                                                     | 3.05 sec: 1.12x faster                                                |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.11x faster                                                 |
| sqlglot_optimize         | 70.1 ms                                                      | 63.2 ms: 1.11x faster                                                 |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                                 |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                 |
| xml_etree_generate       | 92.3 ms                                                      | 84.3 ms: 1.09x faster                                                 |
| json                     | 5.86 ms                                                      | 5.36 ms: 1.09x faster                                                 |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.09x faster                                                  |
| nqueens                  | 115 ms                                                       | 107 ms: 1.08x faster                                                  |
| async_generators         | 421 ms                                                       | 394 ms: 1.07x faster                                                  |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                 |
| regex_dna                | 261 ms                                                       | 246 ms: 1.06x faster                                                  |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                 |
| regex_v8                 | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                 |
| genshi_xml               | 63.3 ms                                                      | 60.3 ms: 1.05x faster                                                 |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                  |
| meteor_contest           | 138 ms                                                       | 135 ms: 1.03x faster                                                  |
| unpickle_list            | 4.65 us                                                      | 4.71 us: 1.01x slower                                                 |
| create_gc_cycles         | 1.76 ms                                                      | 1.80 ms: 1.02x slower                                                 |
| pickle_list              | 4.12 us                                                      | 4.38 us: 1.06x slower                                                 |
| pickle                   | 9.89 us                                                      | 10.8 us: 1.09x slower                                                 |
| unpickle                 | 13.5 us                                                      | 14.9 us: 1.11x slower                                                 |
| pickle_dict              | 29.5 us                                                      | 32.7 us: 1.11x slower                                                 |
| telco                    | 7.23 ms                                                      | 8.03 ms: 1.11x slower                                                 |
| regex_effbot             | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                 |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                 |
| gc_traversal             | 3.42 ms                                                      | 4.37 ms: 1.28x slower                                                 |
| coverage                 | 63.3 ms                                                      | 88.1 ms: 1.39x slower                                                 |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.24x faster                                                          |

Benchmark hidden because not significant (2): bench_thread_pool, asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-4759358-JIT/bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x