# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 242 ms: 1.10x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.74 ms: 1.12x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.90 sec: 1.02x faster                                                          |
| html5lib       | 52.1 ms                                                         | 44.8 ms: 1.16x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.6 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 473 ms: 1.95x faster                                                            |
| async_tree_io           | 940 ms                                                          | 535 ms: 1.76x faster                                                            |
| async_tree_none         | 394 ms                                                          | 231 ms: 1.71x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 278 ms: 1.68x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.77x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 200 ms: 2.51x faster                                                            |
| float          | 69.6 ms                                                         | 55.1 ms: 1.26x faster                                                           |
| Geometric mean | (ref)                                                           | 1.47x faster                                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 120 ms: 1.08x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| regex_compile  | 117 ms                                                          | 119 ms: 1.02x slower                                                            |
| regex_effbot   | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 7.02 ms: 1.40x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 218 us: 1.29x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| unpickle_pure_python | 189 us                                                          | 164 us: 1.15x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 106 ms: 1.13x faster                                                            |
| xml_etree_process    | 48.1 ms                                                         | 43.4 ms: 1.11x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.70 us: 1.11x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 67.1 ms: 1.06x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 60.1 ms: 1.03x faster                                                           |
| pickle               | 7.83 us                                                         | 7.76 us: 1.01x faster                                                           |
| unpickle             | 9.82 us                                                         | 9.94 us: 1.01x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.33 us: 1.04x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.3 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.9 ms                                                         | 21.9 ms: 1.05x faster                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.01 ms: 1.30x faster                                                           |
| django_template | 36.0 ms                                                         | 31.9 ms: 1.13x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 92.9 us: 4.26x faster                                                           |
| pidigits                 | 502 ms                                                          | 200 ms: 2.51x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 473 ms: 1.95x faster                                                            |
| async_tree_io            | 940 ms                                                          | 535 ms: 1.76x faster                                                            |
| async_tree_none          | 394 ms                                                          | 231 ms: 1.71x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 278 ms: 1.68x faster                                                            |
| pylint                   | 384 ms                                                          | 230 ms: 1.67x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 59.7 ns: 1.64x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.58 ms: 1.57x faster                                                           |
| raytrace                 | 303 ms                                                          | 203 ms: 1.49x faster                                                            |
| richards_super           | 49.9 ms                                                         | 33.7 ms: 1.48x faster                                                           |
| chaos                    | 74.4 ms                                                         | 52.6 ms: 1.42x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 7.02 ms: 1.40x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 58.4 ms: 1.39x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 955 us: 1.39x faster                                                            |
| richards                 | 40.3 ms                                                         | 29.7 ms: 1.36x faster                                                           |
| generators               | 31.6 ms                                                         | 23.4 ms: 1.35x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.20 ms: 1.32x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.01 ms: 1.30x faster                                                           |
| comprehensions           | 17.7 us                                                         | 13.7 us: 1.30x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 218 us: 1.29x faster                                                            |
| pyflate                  | 422 ms                                                          | 332 ms: 1.27x faster                                                            |
| float                    | 69.6 ms                                                         | 55.1 ms: 1.26x faster                                                           |
| go                       | 146 ms                                                          | 116 ms: 1.25x faster                                                            |
| pycparser                | 1.04 sec                                                        | 842 ms: 1.24x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 50.8 ms: 1.22x faster                                                           |
| tornado_http             | 118 ms                                                          | 96.6 ms: 1.22x faster                                                           |
| scimark_sor              | 115 ms                                                          | 95.3 ms: 1.21x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.93 us: 1.19x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 627 ms: 1.19x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 25.0 us: 1.18x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.2 ms: 1.18x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| html5lib                 | 52.1 ms                                                         | 44.8 ms: 1.16x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 164 us: 1.15x faster                                                            |
| json                     | 4.76 ms                                                         | 4.13 ms: 1.15x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 5.39 ms: 1.14x faster                                                           |
| django_template          | 36.0 ms                                                         | 31.9 ms: 1.13x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 106 ms: 1.13x faster                                                            |
| nqueens                  | 87.1 ms                                                         | 77.3 ms: 1.13x faster                                                           |
| fannkuch                 | 317 ms                                                          | 282 ms: 1.12x faster                                                            |
| chameleon                | 6.42 ms                                                         | 5.74 ms: 1.12x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 1.00 ms: 1.12x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 80.9 ms: 1.11x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 43.4 ms: 1.11x faster                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.23 sec: 1.11x faster                                                          |
| unpickle_list            | 2.98 us                                                         | 2.70 us: 1.11x faster                                                           |
| deepcopy                 | 310 us                                                          | 281 us: 1.10x faster                                                            |
| json_loads               | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| 2to3                     | 265 ms                                                          | 242 ms: 1.10x faster                                                            |
| pprint_safe_repr         | 658 ms                                                          | 603 ms: 1.09x faster                                                            |
| regex_dna                | 131 ms                                                          | 120 ms: 1.08x faster                                                            |
| sympy_sum                | 122 ms                                                          | 113 ms: 1.08x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.72 sec: 1.06x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 15.8 ms: 1.06x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 67.1 ms: 1.06x faster                                                           |
| python_startup           | 22.9 ms                                                         | 21.9 ms: 1.05x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.10 ms: 1.05x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.57 us: 1.05x faster                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 42.9 ms: 1.04x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 77.5 ms: 1.03x faster                                                           |
| scimark_fft              | 216 ms                                                          | 209 ms: 1.03x faster                                                            |
| sqlglot_normalize        | 230 ms                                                          | 224 ms: 1.03x faster                                                            |
| xml_etree_generate       | 61.6 ms                                                         | 60.1 ms: 1.03x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.90 sec: 1.02x faster                                                          |
| sympy_str                | 229 ms                                                          | 224 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.7 sec: 1.01x faster                                                          |
| pickle                   | 7.83 us                                                         | 7.76 us: 1.01x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 79.5 ms: 1.01x faster                                                           |
| sympy_expand             | 391 ms                                                          | 394 ms: 1.01x slower                                                            |
| unpickle                 | 9.82 us                                                         | 9.94 us: 1.01x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| regex_compile            | 117 ms                                                          | 119 ms: 1.02x slower                                                            |
| pickle_list              | 3.22 us                                                         | 3.33 us: 1.04x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 84.4 ms: 1.04x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 69.3 ms: 1.04x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 731 us: 1.05x slower                                                            |
| logging_simple           | 7.29 us                                                         | 7.92 us: 1.09x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.60 us: 1.09x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.3 us: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.11x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| async_generators         | 241 ms                                                          | 291 ms: 1.21x slower                                                            |
| telco                    | 4.83 ms                                                         | 6.08 ms: 1.26x slower                                                           |
| coverage                 | 46.6 ms                                                         | 512 ms: 11.00x slower                                                           |
| thrift                   | 902 us                                                          | 11.0 ms: 12.22x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (4): genshi_text, nbody, genshi_xml, python_startup_no_site
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown