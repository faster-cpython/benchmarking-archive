# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 231 ms: 1.15x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.57 ms: 1.15x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.77 sec: 1.10x faster                                                          |
| html5lib       | 52.1 ms                                                         | 42.8 ms: 1.22x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.4 ms: 1.25x faster                                                           |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 447 ms: 2.06x faster                                                            |
| async_tree_none         | 394 ms                                                          | 213 ms: 1.85x faster                                                            |
| async_tree_io           | 940 ms                                                          | 515 ms: 1.83x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 262 ms: 1.78x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.88x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 200 ms: 2.52x faster                                                            |
| float          | 69.6 ms                                                         | 51.3 ms: 1.36x faster                                                           |
| nbody          | 79.1 ms                                                         | 74.3 ms: 1.07x faster                                                           |
| Geometric mean | (ref)                                                           | 1.54x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 95.0 ms: 1.23x faster                                                           |
| regex_dna      | 131 ms                                                          | 131 ms: 1.01x slower                                                            |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 202 us: 1.38x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 139 us: 1.36x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.60 sec: 1.19x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 105 ms: 1.14x faster                                                            |
| xml_etree_process    | 48.1 ms                                                         | 42.9 ms: 1.12x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 64.0 ms: 1.11x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 57.9 ms: 1.06x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.87 us: 1.04x faster                                                           |
| pickle               | 7.83 us                                                         | 7.87 us: 1.01x slower                                                           |
| unpickle             | 9.82 us                                                         | 9.93 us: 1.01x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.2 ms: 1.03x faster                                                           |
| python_startup_no_site | 18.1 ms                                                         | 19.8 ms: 1.10x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.89 ms: 1.32x faster                                                           |
| django_template | 36.0 ms                                                         | 28.8 ms: 1.25x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 18.8 ms: 1.12x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 43.2 ms: 1.08x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.19x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 90.5 us: 4.37x faster                                                           |
| pidigits                 | 502 ms                                                          | 200 ms: 2.52x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 447 ms: 2.06x faster                                                            |
| pylint                   | 384 ms                                                          | 204 ms: 1.88x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.15 ms: 1.88x faster                                                           |
| async_tree_none          | 394 ms                                                          | 213 ms: 1.85x faster                                                            |
| async_tree_io            | 940 ms                                                          | 515 ms: 1.83x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 262 ms: 1.78x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 57.2 ns: 1.71x faster                                                           |
| raytrace                 | 303 ms                                                          | 184 ms: 1.65x faster                                                            |
| chaos                    | 74.4 ms                                                         | 46.5 ms: 1.60x faster                                                           |
| comprehensions           | 17.7 us                                                         | 11.2 us: 1.58x faster                                                           |
| richards_super           | 49.9 ms                                                         | 32.2 ms: 1.55x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 860 us: 1.55x faster                                                            |
| go                       | 146 ms                                                          | 96.6 ms: 1.51x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 54.1 ms: 1.50x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 4.18 ms: 1.47x faster                                                           |
| scimark_sor              | 115 ms                                                          | 78.5 ms: 1.47x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 61.7 ms: 1.46x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.09 ms: 1.45x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                           |
| richards                 | 40.3 ms                                                         | 28.1 ms: 1.43x faster                                                           |
| generators               | 31.6 ms                                                         | 22.3 ms: 1.42x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 202 us: 1.38x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 44.7 ms: 1.38x faster                                                           |
| pyflate                  | 422 ms                                                          | 308 ms: 1.37x faster                                                            |
| unpickle_pure_python     | 189 us                                                          | 139 us: 1.36x faster                                                            |
| float                    | 69.6 ms                                                         | 51.3 ms: 1.36x faster                                                           |
| pycparser                | 1.04 sec                                                        | 772 ms: 1.35x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 22.0 us: 1.34x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 66.0 ms: 1.32x faster                                                           |
| mako                     | 9.10 ms                                                         | 6.89 ms: 1.32x faster                                                           |
| coroutines               | 17.9 ms                                                         | 13.9 ms: 1.29x faster                                                           |
| django_template          | 36.0 ms                                                         | 28.8 ms: 1.25x faster                                                           |
| tornado_http             | 118 ms                                                          | 94.4 ms: 1.25x faster                                                           |
| regex_compile            | 117 ms                                                          | 95.0 ms: 1.23x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 42.8 ms: 1.22x faster                                                           |
| sympy_sum                | 122 ms                                                          | 101 ms: 1.21x faster                                                            |
| spectral_norm            | 80.2 ms                                                         | 66.3 ms: 1.21x faster                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.14 sec: 1.20x faster                                                          |
| asyncio_tcp              | 744 ms                                                          | 623 ms: 1.19x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.60 sec: 1.19x faster                                                          |
| sqlite_synth             | 2.29 us                                                         | 1.93 us: 1.19x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 14.0 ms: 1.19x faster                                                           |
| fannkuch                 | 317 ms                                                          | 270 ms: 1.17x faster                                                            |
| pprint_safe_repr         | 658 ms                                                          | 562 ms: 1.17x faster                                                            |
| sympy_str                | 229 ms                                                          | 196 ms: 1.17x faster                                                            |
| sqlglot_optimize         | 44.7 ms                                                         | 38.3 ms: 1.17x faster                                                           |
| deepcopy                 | 310 us                                                          | 266 us: 1.17x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.57 sec: 1.16x faster                                                          |
| chameleon                | 6.42 ms                                                         | 5.57 ms: 1.15x faster                                                           |
| sqlglot_normalize        | 230 ms                                                          | 200 ms: 1.15x faster                                                            |
| 2to3                     | 265 ms                                                          | 231 ms: 1.15x faster                                                            |
| json                     | 4.76 ms                                                         | 4.17 ms: 1.14x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 983 us: 1.14x faster                                                            |
| xml_etree_parse          | 120 ms                                                          | 105 ms: 1.14x faster                                                            |
| deepcopy_reduce          | 2.68 us                                                         | 2.36 us: 1.13x faster                                                           |
| sympy_expand             | 391 ms                                                          | 345 ms: 1.13x faster                                                            |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 2.89 ms: 1.12x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 42.9 ms: 1.12x faster                                                           |
| genshi_text              | 21.0 ms                                                         | 18.8 ms: 1.12x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 64.0 ms: 1.11x faster                                                           |
| json_loads               | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.77 sec: 1.10x faster                                                          |
| unpack_sequence          | 40.0 ns                                                         | 36.9 ns: 1.09x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 74.0 ms: 1.08x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 43.2 ms: 1.08x faster                                                           |
| nbody                    | 79.1 ms                                                         | 74.3 ms: 1.07x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 57.9 ms: 1.06x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.87 us: 1.04x faster                                                           |
| python_startup           | 22.9 ms                                                         | 22.2 ms: 1.03x faster                                                           |
| scimark_fft              | 216 ms                                                          | 210 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.7 sec: 1.01x faster                                                          |
| pickle                   | 7.83 us                                                         | 7.87 us: 1.01x slower                                                           |
| regex_dna                | 131 ms                                                          | 131 ms: 1.01x slower                                                            |
| unpickle                 | 9.82 us                                                         | 9.93 us: 1.01x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.47 us: 1.02x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 68.0 ms: 1.03x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.12 us: 1.03x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 726 us: 1.05x slower                                                            |
| pathlib                  | 81.2 ms                                                         | 86.4 ms: 1.06x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 19.8 ms: 1.10x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.12x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| async_generators         | 241 ms                                                          | 286 ms: 1.18x slower                                                            |
| telco                    | 4.83 ms                                                         | 5.86 ms: 1.21x slower                                                           |
| coverage                 | 46.6 ms                                                         | 470 ms: 10.09x slower                                                           |
| thrift                   | 902 us                                                          | 9.91 ms: 10.99x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.18x faster                                                                    |

Benchmark hidden because not significant (1): pickle_list
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown