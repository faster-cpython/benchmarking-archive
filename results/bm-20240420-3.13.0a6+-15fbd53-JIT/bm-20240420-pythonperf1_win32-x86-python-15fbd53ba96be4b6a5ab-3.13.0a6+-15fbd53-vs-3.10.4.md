# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 253 ms: 1.05x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.02 ms: 1.07x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| html5lib       | 52.1 ms                                                         | 45.0 ms: 1.16x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.0 ms: 1.24x faster                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 484 ms: 1.90x faster                                                            |
| async_tree_io           | 940 ms                                                          | 540 ms: 1.74x faster                                                            |
| async_tree_none         | 394 ms                                                          | 240 ms: 1.64x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 289 ms: 1.62x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.72x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| float          | 69.6 ms                                                         | 52.2 ms: 1.33x faster                                                           |
| nbody          | 79.1 ms                                                         | 92.0 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                           | 1.43x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| regex_compile  | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 222 us: 1.26x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 164 us: 1.16x faster                                                            |
| json_loads           | 22.4 us                                                         | 19.8 us: 1.13x faster                                                           |
| tomli_loads          | 1.91 sec                                                        | 1.73 sec: 1.11x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 109 ms: 1.10x faster                                                            |
| xml_etree_process    | 48.1 ms                                                         | 43.7 ms: 1.10x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 66.4 ms: 1.07x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.87 us: 1.04x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.19 us: 1.01x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 62.6 ms: 1.02x slower                                                           |
| pickle               | 7.83 us                                                         | 7.96 us: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 20.7 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.10x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 6.88 ms: 1.32x faster                                                           |
| django_template | 36.0 ms                                                         | 33.3 ms: 1.08x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 44.7 ms: 1.04x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 20.4 ms: 1.03x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.11x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 95.5 us: 4.14x faster                                                           |
| pidigits                 | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 484 ms: 1.90x faster                                                            |
| async_tree_io            | 940 ms                                                          | 540 ms: 1.74x faster                                                            |
| pylint                   | 384 ms                                                          | 233 ms: 1.65x faster                                                            |
| async_tree_none          | 394 ms                                                          | 240 ms: 1.64x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 59.9 ns: 1.63x faster                                                           |
| async_tree_memoization   | 467 ms                                                          | 289 ms: 1.62x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.71 ms: 1.49x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.79 ms: 1.45x faster                                                           |
| generators               | 31.6 ms                                                         | 22.5 ms: 1.40x faster                                                           |
| raytrace                 | 303 ms                                                          | 223 ms: 1.36x faster                                                            |
| sqlglot_parse            | 1.33 ms                                                         | 994 us: 1.34x faster                                                            |
| float                    | 69.6 ms                                                         | 52.2 ms: 1.33x faster                                                           |
| richards_super           | 49.9 ms                                                         | 37.5 ms: 1.33x faster                                                           |
| mako                     | 9.10 ms                                                         | 6.88 ms: 1.32x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 63.2 ms: 1.29x faster                                                           |
| chaos                    | 74.4 ms                                                         | 58.0 ms: 1.28x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.25 ms: 1.27x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 222 us: 1.26x faster                                                            |
| pycparser                | 1.04 sec                                                        | 835 ms: 1.25x faster                                                            |
| tornado_http             | 118 ms                                                          | 95.0 ms: 1.24x faster                                                           |
| go                       | 146 ms                                                          | 119 ms: 1.22x faster                                                            |
| richards                 | 40.3 ms                                                         | 33.0 ms: 1.22x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 24.9 us: 1.19x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.93 us: 1.18x faster                                                           |
| scimark_sor              | 115 ms                                                          | 97.3 ms: 1.18x faster                                                           |
| comprehensions           | 17.7 us                                                         | 15.2 us: 1.17x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 164 us: 1.16x faster                                                            |
| html5lib                 | 52.1 ms                                                         | 45.0 ms: 1.16x faster                                                           |
| pyflate                  | 422 ms                                                          | 366 ms: 1.15x faster                                                            |
| json                     | 4.76 ms                                                         | 4.13 ms: 1.15x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.6 ms: 1.15x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 652 ms: 1.14x faster                                                            |
| spectral_norm            | 80.2 ms                                                         | 70.6 ms: 1.14x faster                                                           |
| json_loads               | 22.4 us                                                         | 19.8 us: 1.13x faster                                                           |
| sympy_sum                | 122 ms                                                          | 110 ms: 1.11x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.73 sec: 1.11x faster                                                          |
| bench_thread_pool        | 1.12 ms                                                         | 1.01 ms: 1.10x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 109 ms: 1.10x faster                                                            |
| xml_etree_process        | 48.1 ms                                                         | 43.7 ms: 1.10x faster                                                           |
| django_template          | 36.0 ms                                                         | 33.3 ms: 1.08x faster                                                           |
| regex_dna                | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 66.4 ms: 1.07x faster                                                           |
| chameleon                | 6.42 ms                                                         | 6.02 ms: 1.07x faster                                                           |
| regex_compile            | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.72 sec: 1.06x faster                                                          |
| 2to3                     | 265 ms                                                          | 253 ms: 1.05x faster                                                            |
| deepcopy                 | 310 us                                                          | 295 us: 1.05x faster                                                            |
| sympy_str                | 229 ms                                                          | 218 ms: 1.05x faster                                                            |
| hexiom                   | 6.13 ms                                                         | 5.86 ms: 1.05x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 44.7 ms: 1.04x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.87 us: 1.04x faster                                                           |
| sympy_expand             | 391 ms                                                          | 377 ms: 1.04x faster                                                            |
| genshi_text              | 21.0 ms                                                         | 20.4 ms: 1.03x faster                                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 60.4 ms: 1.02x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 16.3 ms: 1.02x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.17 ms: 1.02x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 88.0 ms: 1.02x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| deepcopy_reduce          | 2.68 us                                                         | 2.65 us: 1.01x faster                                                           |
| pickle_list              | 3.22 us                                                         | 3.19 us: 1.01x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 80.7 ms: 1.01x slower                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 62.6 ms: 1.02x slower                                                           |
| sqlglot_normalize        | 230 ms                                                          | 234 ms: 1.02x slower                                                            |
| pickle                   | 7.83 us                                                         | 7.96 us: 1.02x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 45.7 ms: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 83.9 ms: 1.03x slower                                                           |
| nqueens                  | 87.1 ms                                                         | 90.7 ms: 1.04x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 727 us: 1.05x slower                                                            |
| python_startup           | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.66 us: 1.10x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.50 sec: 1.10x slower                                                          |
| pickle_dict              | 18.2 us                                                         | 20.2 us: 1.11x slower                                                           |
| logging_simple           | 7.29 us                                                         | 8.09 us: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                           |
| pprint_safe_repr         | 658 ms                                                          | 735 ms: 1.12x slower                                                            |
| scimark_fft              | 216 ms                                                          | 241 ms: 1.12x slower                                                            |
| bench_mp_pool            | 66.4 ms                                                         | 74.2 ms: 1.12x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 20.7 ms: 1.15x slower                                                           |
| nbody                    | 79.1 ms                                                         | 92.0 ms: 1.16x slower                                                           |
| async_generators         | 241 ms                                                          | 289 ms: 1.20x slower                                                            |
| telco                    | 4.83 ms                                                         | 6.36 ms: 1.32x slower                                                           |
| coverage                 | 46.6 ms                                                         | 499 ms: 10.71x slower                                                           |
| thrift                   | 902 us                                                          | 10.6 ms: 11.76x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.07x faster                                                                    |

Benchmark hidden because not significant (1): fannkuch
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown