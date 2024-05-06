# Results vs. 3.10.4

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-x86
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 258 ms: 1.03x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.05 ms: 1.06x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| html5lib       | 52.1 ms                                                         | 45.7 ms: 1.14x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.3 ms: 1.23x faster                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 483 ms: 1.91x faster                                                            |
| async_tree_io           | 940 ms                                                          | 539 ms: 1.75x faster                                                            |
| async_tree_none         | 394 ms                                                          | 238 ms: 1.66x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 286 ms: 1.63x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.73x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 199 ms: 2.53x faster                                                            |
| float          | 69.6 ms                                                         | 53.3 ms: 1.30x faster                                                           |
| nbody          | 79.1 ms                                                         | 101 ms: 1.27x slower                                                            |
| Geometric mean | (ref)                                                           | 1.37x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 118 ms: 1.10x faster                                                            |
| regex_compile  | 117 ms                                                          | 112 ms: 1.04x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.82 ms: 1.44x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 223 us: 1.26x faster                                                            |
| json_loads           | 22.4 us                                                         | 19.8 us: 1.13x faster                                                           |
| xml_etree_process    | 48.1 ms                                                         | 43.0 ms: 1.12x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 170 us: 1.11x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                          |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.91 us: 1.02x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.17 us: 1.01x faster                                                           |
| pickle_dict          | 18.2 us                                                         | 20.0 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (2): unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.6 ms: 1.07x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 22.4 ms: 1.24x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.16x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 7.13 ms: 1.28x faster                                                           |
| genshi_xml     | 46.6 ms                                                         | 47.6 ms: 1.02x slower                                                           |
| genshi_text    | 21.0 ms                                                         | 21.6 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 99.8 us: 3.97x faster                                                           |
| pidigits                 | 502 ms                                                          | 199 ms: 2.53x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 483 ms: 1.91x faster                                                            |
| async_tree_io            | 940 ms                                                          | 539 ms: 1.75x faster                                                            |
| pylint                   | 384 ms                                                          | 222 ms: 1.73x faster                                                            |
| async_tree_none          | 394 ms                                                          | 238 ms: 1.66x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 286 ms: 1.63x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 60.1 ns: 1.63x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.70 ms: 1.50x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.82 ms: 1.44x faster                                                           |
| generators               | 31.6 ms                                                         | 22.8 ms: 1.39x faster                                                           |
| raytrace                 | 303 ms                                                          | 222 ms: 1.36x faster                                                            |
| sqlglot_parse            | 1.33 ms                                                         | 990 us: 1.34x faster                                                            |
| richards_super           | 49.9 ms                                                         | 38.2 ms: 1.31x faster                                                           |
| float                    | 69.6 ms                                                         | 53.3 ms: 1.30x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 63.6 ms: 1.28x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.13 ms: 1.28x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.24 ms: 1.28x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 223 us: 1.26x faster                                                            |
| pycparser                | 1.04 sec                                                        | 839 ms: 1.24x faster                                                            |
| chaos                    | 74.4 ms                                                         | 60.2 ms: 1.24x faster                                                           |
| tornado_http             | 118 ms                                                          | 95.3 ms: 1.23x faster                                                           |
| go                       | 146 ms                                                          | 119 ms: 1.22x faster                                                            |
| richards                 | 40.3 ms                                                         | 33.4 ms: 1.20x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.0 ms: 1.20x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 24.9 us: 1.19x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 626 ms: 1.19x faster                                                            |
| json                     | 4.76 ms                                                         | 4.01 ms: 1.19x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.94 us: 1.18x faster                                                           |
| pyflate                  | 422 ms                                                          | 364 ms: 1.16x faster                                                            |
| html5lib                 | 52.1 ms                                                         | 45.7 ms: 1.14x faster                                                           |
| comprehensions           | 17.7 us                                                         | 15.6 us: 1.14x faster                                                           |
| json_loads               | 22.4 us                                                         | 19.8 us: 1.13x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 71.5 ms: 1.12x faster                                                           |
| scimark_sor              | 115 ms                                                          | 103 ms: 1.12x faster                                                            |
| xml_etree_process        | 48.1 ms                                                         | 43.0 ms: 1.12x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 170 us: 1.11x faster                                                            |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 1.01 ms: 1.10x faster                                                           |
| regex_dna                | 131 ms                                                          | 118 ms: 1.10x faster                                                            |
| sympy_sum                | 122 ms                                                          | 112 ms: 1.09x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                          |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| deepcopy                 | 310 us                                                          | 290 us: 1.07x faster                                                            |
| chameleon                | 6.42 ms                                                         | 6.05 ms: 1.06x faster                                                           |
| regex_compile            | 117 ms                                                          | 112 ms: 1.04x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.77 sec: 1.03x faster                                                          |
| sympy_str                | 229 ms                                                          | 222 ms: 1.03x faster                                                            |
| 2to3                     | 265 ms                                                          | 258 ms: 1.03x faster                                                            |
| unpickle_list            | 2.98 us                                                         | 2.91 us: 1.02x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| sympy_expand             | 391 ms                                                          | 383 ms: 1.02x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 60.9 ms: 1.02x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 16.4 ms: 1.02x faster                                                           |
| pickle_list              | 3.22 us                                                         | 3.17 us: 1.01x faster                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| scimark_lu               | 89.8 ms                                                         | 88.9 ms: 1.01x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 6.09 ms: 1.01x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.22 ms: 1.01x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 47.6 ms: 1.02x slower                                                           |
| sqlglot_normalize        | 230 ms                                                          | 235 ms: 1.02x slower                                                            |
| genshi_text              | 21.0 ms                                                         | 21.6 ms: 1.03x slower                                                           |
| fannkuch                 | 317 ms                                                          | 327 ms: 1.03x slower                                                            |
| meteor_contest           | 80.0 ms                                                         | 82.5 ms: 1.03x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 46.8 ms: 1.05x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 85.9 ms: 1.06x slower                                                           |
| nqueens                  | 87.1 ms                                                         | 92.2 ms: 1.06x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 740 us: 1.07x slower                                                            |
| python_startup           | 22.9 ms                                                         | 24.6 ms: 1.07x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 72.5 ms: 1.09x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.65 us: 1.09x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.0 us: 1.09x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.50 sec: 1.10x slower                                                          |
| logging_simple           | 7.29 us                                                         | 8.02 us: 1.10x slower                                                           |
| pprint_safe_repr         | 658 ms                                                          | 732 ms: 1.11x slower                                                            |
| scimark_fft              | 216 ms                                                          | 244 ms: 1.13x slower                                                            |
| gc_traversal             | 1.28 ms                                                         | 1.46 ms: 1.14x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| async_generators         | 241 ms                                                          | 287 ms: 1.19x slower                                                            |
| python_startup_no_site   | 18.1 ms                                                         | 22.4 ms: 1.24x slower                                                           |
| nbody                    | 79.1 ms                                                         | 101 ms: 1.27x slower                                                            |
| telco                    | 4.83 ms                                                         | 6.40 ms: 1.33x slower                                                           |
| coverage                 | 46.6 ms                                                         | 514 ms: 11.03x slower                                                           |
| thrift                   | 902 us                                                          | 10.6 ms: 11.74x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.06x faster                                                                    |

Benchmark hidden because not significant (3): deepcopy_reduce, unpickle, pickle
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown