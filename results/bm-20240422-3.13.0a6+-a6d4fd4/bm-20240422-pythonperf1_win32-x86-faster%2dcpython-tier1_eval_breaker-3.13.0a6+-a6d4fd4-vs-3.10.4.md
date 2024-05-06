# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-x86
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 232 ms: 1.14x faster                                                                    |
| chameleon      | 6.42 ms                                                         | 5.61 ms: 1.14x faster                                                                   |
| docutils       | 1.95 sec                                                        | 1.80 sec: 1.09x faster                                                                  |
| html5lib       | 52.1 ms                                                         | 42.8 ms: 1.22x faster                                                                   |
| tornado_http   | 118 ms                                                          | 94.0 ms: 1.25x faster                                                                   |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 468 ms: 1.97x faster                                                                    |
| async_tree_io           | 940 ms                                                          | 529 ms: 1.78x faster                                                                    |
| async_tree_none         | 394 ms                                                          | 226 ms: 1.74x faster                                                                    |
| async_tree_memoization  | 467 ms                                                          | 270 ms: 1.73x faster                                                                    |
| Geometric mean          | (ref)                                                           | 1.80x faster                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                                    |
| float          | 69.6 ms                                                         | 53.4 ms: 1.30x faster                                                                   |
| nbody          | 79.1 ms                                                         | 76.4 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                           | 1.51x faster                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 97.4 ms: 1.20x faster                                                                   |
| regex_dna      | 131 ms                                                          | 121 ms: 1.08x faster                                                                    |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                                   |
| regex_effbot   | 1.66 ms                                                         | 1.90 ms: 1.15x slower                                                                   |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.92 ms: 1.42x faster                                                                   |
| unpickle_pure_python | 189 us                                                          | 140 us: 1.35x faster                                                                    |
| pickle_pure_python   | 280 us                                                          | 209 us: 1.34x faster                                                                    |
| tomli_loads          | 1.91 sec                                                        | 1.63 sec: 1.18x faster                                                                  |
| xml_etree_process    | 48.1 ms                                                         | 42.3 ms: 1.14x faster                                                                   |
| xml_etree_parse      | 120 ms                                                          | 107 ms: 1.12x faster                                                                    |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.0 ms: 1.09x faster                                                                   |
| json_loads           | 22.4 us                                                         | 20.6 us: 1.09x faster                                                                   |
| unpickle_list        | 2.98 us                                                         | 2.86 us: 1.04x faster                                                                   |
| xml_etree_generate   | 61.6 ms                                                         | 60.0 ms: 1.03x faster                                                                   |
| pickle               | 7.83 us                                                         | 7.97 us: 1.02x slower                                                                   |
| pickle_list          | 3.22 us                                                         | 3.29 us: 1.02x slower                                                                   |
| pickle_dict          | 18.2 us                                                         | 20.4 us: 1.12x slower                                                                   |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                            |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.0 ms: 1.04x faster                                                                   |
| python_startup_no_site | 18.1 ms                                                         | 18.3 ms: 1.01x slower                                                                   |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.87 ms: 1.32x faster                                                                   |
| django_template | 36.0 ms                                                         | 29.5 ms: 1.22x faster                                                                   |
| genshi_text     | 21.0 ms                                                         | 18.8 ms: 1.12x faster                                                                   |
| genshi_xml      | 46.6 ms                                                         | 42.7 ms: 1.09x faster                                                                   |
| Geometric mean  | (ref)                                                           | 1.19x faster                                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 90.7 us: 4.36x faster                                                                   |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                                    |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 468 ms: 1.97x faster                                                                    |
| deltablue                | 4.04 ms                                                         | 2.20 ms: 1.83x faster                                                                   |
| async_tree_io            | 940 ms                                                          | 529 ms: 1.78x faster                                                                    |
| pylint                   | 384 ms                                                          | 219 ms: 1.75x faster                                                                    |
| async_tree_none          | 394 ms                                                          | 226 ms: 1.74x faster                                                                    |
| async_tree_memoization   | 467 ms                                                          | 270 ms: 1.73x faster                                                                    |
| logging_silent           | 97.9 ns                                                         | 59.8 ns: 1.64x faster                                                                   |
| raytrace                 | 303 ms                                                          | 189 ms: 1.60x faster                                                                    |
| comprehensions           | 17.7 us                                                         | 11.7 us: 1.52x faster                                                                   |
| chaos                    | 74.4 ms                                                         | 49.1 ms: 1.52x faster                                                                   |
| sqlglot_parse            | 1.33 ms                                                         | 878 us: 1.51x faster                                                                    |
| go                       | 146 ms                                                          | 98.3 ms: 1.48x faster                                                                   |
| scimark_lu               | 89.8 ms                                                         | 61.4 ms: 1.46x faster                                                                   |
| richards_super           | 49.9 ms                                                         | 34.2 ms: 1.46x faster                                                                   |
| crypto_pyaes             | 81.3 ms                                                         | 56.5 ms: 1.44x faster                                                                   |
| sqlglot_transpile        | 1.58 ms                                                         | 1.10 ms: 1.44x faster                                                                   |
| scimark_sor              | 115 ms                                                          | 80.9 ms: 1.42x faster                                                                   |
| hexiom                   | 6.13 ms                                                         | 4.32 ms: 1.42x faster                                                                   |
| json_dumps               | 9.82 ms                                                         | 6.92 ms: 1.42x faster                                                                   |
| generators               | 31.6 ms                                                         | 23.0 ms: 1.37x faster                                                                   |
| pycparser                | 1.04 sec                                                        | 772 ms: 1.35x faster                                                                    |
| unpickle_pure_python     | 189 us                                                          | 140 us: 1.35x faster                                                                    |
| pickle_pure_python       | 280 us                                                          | 209 us: 1.34x faster                                                                    |
| pyflate                  | 422 ms                                                          | 316 ms: 1.34x faster                                                                    |
| richards                 | 40.3 ms                                                         | 30.3 ms: 1.33x faster                                                                   |
| scimark_monte_carlo      | 61.9 ms                                                         | 46.7 ms: 1.33x faster                                                                   |
| mako                     | 9.10 ms                                                         | 6.87 ms: 1.32x faster                                                                   |
| float                    | 69.6 ms                                                         | 53.4 ms: 1.30x faster                                                                   |
| deepcopy_memo            | 29.6 us                                                         | 22.9 us: 1.29x faster                                                                   |
| tornado_http             | 118 ms                                                          | 94.0 ms: 1.25x faster                                                                   |
| nqueens                  | 87.1 ms                                                         | 70.6 ms: 1.23x faster                                                                   |
| django_template          | 36.0 ms                                                         | 29.5 ms: 1.22x faster                                                                   |
| coroutines               | 17.9 ms                                                         | 14.7 ms: 1.22x faster                                                                   |
| html5lib                 | 52.1 ms                                                         | 42.8 ms: 1.22x faster                                                                   |
| regex_compile            | 117 ms                                                          | 97.4 ms: 1.20x faster                                                                   |
| pprint_pformat           | 1.37 sec                                                        | 1.15 sec: 1.19x faster                                                                  |
| pprint_safe_repr         | 658 ms                                                          | 558 ms: 1.18x faster                                                                    |
| deepcopy                 | 310 us                                                          | 264 us: 1.18x faster                                                                    |
| tomli_loads              | 1.91 sec                                                        | 1.63 sec: 1.18x faster                                                                  |
| sympy_sum                | 122 ms                                                          | 104 ms: 1.17x faster                                                                    |
| sqlite_synth             | 2.29 us                                                         | 1.97 us: 1.16x faster                                                                   |
| json                     | 4.76 ms                                                         | 4.12 ms: 1.16x faster                                                                   |
| sympy_integrate          | 16.6 ms                                                         | 14.5 ms: 1.15x faster                                                                   |
| bench_thread_pool        | 1.12 ms                                                         | 977 us: 1.15x faster                                                                    |
| chameleon                | 6.42 ms                                                         | 5.61 ms: 1.14x faster                                                                   |
| 2to3                     | 265 ms                                                          | 232 ms: 1.14x faster                                                                    |
| fannkuch                 | 317 ms                                                          | 279 ms: 1.14x faster                                                                    |
| xml_etree_process        | 48.1 ms                                                         | 42.3 ms: 1.14x faster                                                                   |
| deepcopy_reduce          | 2.68 us                                                         | 2.36 us: 1.14x faster                                                                   |
| sqlglot_normalize        | 230 ms                                                          | 203 ms: 1.14x faster                                                                    |
| sqlglot_optimize         | 44.7 ms                                                         | 39.5 ms: 1.13x faster                                                                   |
| spectral_norm            | 80.2 ms                                                         | 71.0 ms: 1.13x faster                                                                   |
| asyncio_tcp              | 744 ms                                                          | 659 ms: 1.13x faster                                                                    |
| xml_etree_parse          | 120 ms                                                          | 107 ms: 1.12x faster                                                                    |
| genshi_text              | 21.0 ms                                                         | 18.8 ms: 1.12x faster                                                                   |
| sympy_str                | 229 ms                                                          | 205 ms: 1.12x faster                                                                    |
| mdp                      | 1.83 sec                                                        | 1.64 sec: 1.11x faster                                                                  |
| genshi_xml               | 46.6 ms                                                         | 42.7 ms: 1.09x faster                                                                   |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.0 ms: 1.09x faster                                                                   |
| json_loads               | 22.4 us                                                         | 20.6 us: 1.09x faster                                                                   |
| sympy_expand             | 391 ms                                                          | 359 ms: 1.09x faster                                                                    |
| docutils                 | 1.95 sec                                                        | 1.80 sec: 1.09x faster                                                                  |
| regex_dna                | 131 ms                                                          | 121 ms: 1.08x faster                                                                    |
| meteor_contest           | 80.0 ms                                                         | 75.2 ms: 1.06x faster                                                                   |
| unpickle_list            | 2.98 us                                                         | 2.86 us: 1.04x faster                                                                   |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.11 ms: 1.04x faster                                                                   |
| python_startup           | 22.9 ms                                                         | 22.0 ms: 1.04x faster                                                                   |
| nbody                    | 79.1 ms                                                         | 76.4 ms: 1.04x faster                                                                   |
| xml_etree_generate       | 61.6 ms                                                         | 60.0 ms: 1.03x faster                                                                   |
| scimark_fft              | 216 ms                                                          | 212 ms: 1.02x faster                                                                    |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                                  |
| python_startup_no_site   | 18.1 ms                                                         | 18.3 ms: 1.01x slower                                                                   |
| logging_format           | 7.91 us                                                         | 8.01 us: 1.01x slower                                                                   |
| pickle                   | 7.83 us                                                         | 7.97 us: 1.02x slower                                                                   |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                                   |
| pickle_list              | 3.22 us                                                         | 3.29 us: 1.02x slower                                                                   |
| logging_simple           | 7.29 us                                                         | 7.47 us: 1.03x slower                                                                   |
| bench_mp_pool            | 66.4 ms                                                         | 68.1 ms: 1.03x slower                                                                   |
| pathlib                  | 81.2 ms                                                         | 84.8 ms: 1.04x slower                                                                   |
| create_gc_cycles         | 694 us                                                          | 732 us: 1.06x slower                                                                    |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                                   |
| pickle_dict              | 18.2 us                                                         | 20.4 us: 1.12x slower                                                                   |
| regex_effbot             | 1.66 ms                                                         | 1.90 ms: 1.15x slower                                                                   |
| async_generators         | 241 ms                                                          | 280 ms: 1.16x slower                                                                    |
| telco                    | 4.83 ms                                                         | 5.90 ms: 1.22x slower                                                                   |
| coverage                 | 46.6 ms                                                         | 506 ms: 10.86x slower                                                                   |
| thrift                   | 902 us                                                          | 9.88 ms: 10.95x slower                                                                  |
| Geometric mean           | (ref)                                                           | 1.16x faster                                                                            |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: unknown