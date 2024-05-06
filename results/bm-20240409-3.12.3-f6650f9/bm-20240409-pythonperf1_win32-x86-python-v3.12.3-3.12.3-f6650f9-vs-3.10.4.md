# Results vs. 3.10.4

- fork: python
- ref: v3.12.3
- machine: windows-x86
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.01x faster
- HPT reliability: 71.82%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 269 ms: 1.01x slower                                            |
| chameleon      | 6.42 ms                                                         | 7.39 ms: 1.15x slower                                           |
| docutils       | 1.95 sec                                                        | 1.94 sec: 1.00x faster                                          |
| html5lib       | 52.1 ms                                                         | 51.5 ms: 1.01x faster                                           |
| tornado_http   | 118 ms                                                          | 104 ms: 1.13x faster                                            |
| Geometric mean | (ref)                                                           | 1.00x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 553 ms: 1.67x faster                                            |
| async_tree_io           | 940 ms                                                          | 683 ms: 1.38x faster                                            |
| async_tree_none         | 394 ms                                                          | 296 ms: 1.33x faster                                            |
| async_tree_memoization  | 467 ms                                                          | 358 ms: 1.30x faster                                            |
| Geometric mean          | (ref)                                                           | 1.41x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 199 ms: 2.52x faster                                            |
| float          | 69.6 ms                                                         | 76.5 ms: 1.10x slower                                           |
| nbody          | 79.1 ms                                                         | 125 ms: 1.57x slower                                            |
| Geometric mean | (ref)                                                           | 1.13x faster                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 15.3 ms: 1.03x faster                                           |
| regex_dna      | 131 ms                                                          | 129 ms: 1.01x faster                                            |
| regex_compile  | 117 ms                                                          | 130 ms: 1.12x slower                                            |
| regex_effbot   | 1.66 ms                                                         | 2.00 ms: 1.21x slower                                           |
| Geometric mean | (ref)                                                           | 1.07x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 7.49 ms: 1.31x faster                                           |
| json_loads           | 22.4 us                                                         | 20.9 us: 1.07x faster                                           |
| xml_etree_parse      | 120 ms                                                          | 113 ms: 1.06x faster                                            |
| unpickle             | 9.82 us                                                         | 9.53 us: 1.03x faster                                           |
| pickle_pure_python   | 280 us                                                          | 299 us: 1.07x slower                                            |
| unpickle_list        | 2.98 us                                                         | 3.27 us: 1.09x slower                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 77.8 ms: 1.10x slower                                           |
| pickle_dict          | 18.2 us                                                         | 20.1 us: 1.10x slower                                           |
| xml_etree_process    | 48.1 ms                                                         | 53.5 ms: 1.11x slower                                           |
| unpickle_pure_python | 189 us                                                          | 217 us: 1.14x slower                                            |
| tomli_loads          | 1.91 sec                                                        | 2.19 sec: 1.15x slower                                          |
| xml_etree_generate   | 61.6 ms                                                         | 73.6 ms: 1.19x slower                                           |
| Geometric mean       | (ref)                                                           | 1.03x slower                                                    |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup | 22.9 ms                                                         | 21.3 ms: 1.08x faster                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 36.0 ms                                                         | 36.7 ms: 1.02x slower                                           |
| mako            | 9.10 ms                                                         | 9.97 ms: 1.09x slower                                           |
| genshi_xml      | 46.6 ms                                                         | 53.9 ms: 1.16x slower                                           |
| genshi_text     | 21.0 ms                                                         | 24.9 ms: 1.19x slower                                           |
| Geometric mean  | (ref)                                                           | 1.11x slower                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 114 us: 3.46x faster                                            |
| pidigits                 | 502 ms                                                          | 199 ms: 2.52x faster                                            |
| sqlglot_normalize        | 230 ms                                                          | 102 ms: 2.25x faster                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 553 ms: 1.67x faster                                            |
| pylint                   | 384 ms                                                          | 249 ms: 1.54x faster                                            |
| async_tree_io            | 940 ms                                                          | 683 ms: 1.38x faster                                            |
| async_tree_none          | 394 ms                                                          | 296 ms: 1.33x faster                                            |
| json_dumps               | 9.82 ms                                                         | 7.49 ms: 1.31x faster                                           |
| async_tree_memoization   | 467 ms                                                          | 358 ms: 1.30x faster                                            |
| thrift                   | 902 us                                                          | 773 us: 1.17x faster                                            |
| asyncio_tcp              | 744 ms                                                          | 646 ms: 1.15x faster                                            |
| crypto_pyaes             | 81.3 ms                                                         | 71.7 ms: 1.13x faster                                           |
| comprehensions           | 17.7 us                                                         | 15.7 us: 1.13x faster                                           |
| tornado_http             | 118 ms                                                          | 104 ms: 1.13x faster                                            |
| deltablue                | 4.04 ms                                                         | 3.61 ms: 1.12x faster                                           |
| aiohttp                  | 1.13 ms                                                         | 1.03 ms: 1.11x faster                                           |
| chaos                    | 74.4 ms                                                         | 68.1 ms: 1.09x faster                                           |
| sqlalchemy_imperative    | 13.2 ms                                                         | 12.1 ms: 1.09x faster                                           |
| json                     | 4.76 ms                                                         | 4.42 ms: 1.08x faster                                           |
| python_startup           | 22.9 ms                                                         | 21.3 ms: 1.08x faster                                           |
| go                       | 146 ms                                                          | 135 ms: 1.08x faster                                            |
| pycparser                | 1.04 sec                                                        | 970 ms: 1.07x faster                                            |
| sqlite_synth             | 2.29 us                                                         | 2.13 us: 1.07x faster                                           |
| create_gc_cycles         | 694 us                                                          | 648 us: 1.07x faster                                            |
| json_loads               | 22.4 us                                                         | 20.9 us: 1.07x faster                                           |
| dask                     | 341 ms                                                          | 322 ms: 1.06x faster                                            |
| sympy_sum                | 122 ms                                                          | 116 ms: 1.06x faster                                            |
| xml_etree_parse          | 120 ms                                                          | 113 ms: 1.06x faster                                            |
| sqlglot_parse            | 1.33 ms                                                         | 1.26 ms: 1.05x faster                                           |
| bench_thread_pool        | 1.12 ms                                                         | 1.08 ms: 1.04x faster                                           |
| richards_super           | 49.9 ms                                                         | 48.2 ms: 1.04x faster                                           |
| mypy2                    | 590 ms                                                          | 571 ms: 1.03x faster                                            |
| dulwich_log              | 58.5 ms                                                         | 56.7 ms: 1.03x faster                                           |
| unpickle                 | 9.82 us                                                         | 9.53 us: 1.03x faster                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.54 ms: 1.03x faster                                           |
| regex_v8                 | 15.8 ms                                                         | 15.3 ms: 1.03x faster                                           |
| sqlalchemy_declarative   | 104 ms                                                          | 102 ms: 1.02x faster                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.7 sec: 1.01x faster                                          |
| html5lib                 | 52.1 ms                                                         | 51.5 ms: 1.01x faster                                           |
| regex_dna                | 131 ms                                                          | 129 ms: 1.01x faster                                            |
| docutils                 | 1.95 sec                                                        | 1.94 sec: 1.00x faster                                          |
| mdp                      | 1.83 sec                                                        | 1.82 sec: 1.00x faster                                          |
| 2to3                     | 265 ms                                                          | 269 ms: 1.01x slower                                            |
| sympy_str                | 229 ms                                                          | 232 ms: 1.01x slower                                            |
| sympy_integrate          | 16.6 ms                                                         | 16.9 ms: 1.01x slower                                           |
| django_template          | 36.0 ms                                                         | 36.7 ms: 1.02x slower                                           |
| pyflate                  | 422 ms                                                          | 433 ms: 1.03x slower                                            |
| sympy_expand             | 391 ms                                                          | 402 ms: 1.03x slower                                            |
| pathlib                  | 81.2 ms                                                         | 85.6 ms: 1.05x slower                                           |
| meteor_contest           | 80.0 ms                                                         | 84.8 ms: 1.06x slower                                           |
| nqueens                  | 87.1 ms                                                         | 92.6 ms: 1.06x slower                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 47.6 ms: 1.06x slower                                           |
| pickle_pure_python       | 280 us                                                          | 299 us: 1.07x slower                                            |
| logging_silent           | 97.9 ns                                                         | 105 ns: 1.07x slower                                            |
| scimark_lu               | 89.8 ms                                                         | 96.6 ms: 1.08x slower                                           |
| richards                 | 40.3 ms                                                         | 43.5 ms: 1.08x slower                                           |
| telco                    | 4.83 ms                                                         | 5.22 ms: 1.08x slower                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 67.0 ms: 1.08x slower                                           |
| bench_mp_pool            | 66.4 ms                                                         | 71.9 ms: 1.08x slower                                           |
| coverage                 | 46.6 ms                                                         | 50.4 ms: 1.08x slower                                           |
| unpickle_list            | 2.98 us                                                         | 3.27 us: 1.09x slower                                           |
| mako                     | 9.10 ms                                                         | 9.97 ms: 1.09x slower                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 77.8 ms: 1.10x slower                                           |
| gc_traversal             | 1.28 ms                                                         | 1.41 ms: 1.10x slower                                           |
| float                    | 69.6 ms                                                         | 76.5 ms: 1.10x slower                                           |
| pickle_dict              | 18.2 us                                                         | 20.1 us: 1.10x slower                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.52 sec: 1.11x slower                                          |
| xml_etree_process        | 48.1 ms                                                         | 53.5 ms: 1.11x slower                                           |
| regex_compile            | 117 ms                                                          | 130 ms: 1.12x slower                                            |
| pprint_safe_repr         | 658 ms                                                          | 742 ms: 1.13x slower                                            |
| scimark_sor              | 115 ms                                                          | 130 ms: 1.13x slower                                            |
| hexiom                   | 6.13 ms                                                         | 6.93 ms: 1.13x slower                                           |
| deepcopy                 | 310 us                                                          | 353 us: 1.14x slower                                            |
| unpickle_pure_python     | 189 us                                                          | 217 us: 1.14x slower                                            |
| fannkuch                 | 317 ms                                                          | 363 ms: 1.14x slower                                            |
| tomli_loads              | 1.91 sec                                                        | 2.19 sec: 1.15x slower                                          |
| chameleon                | 6.42 ms                                                         | 7.39 ms: 1.15x slower                                           |
| genshi_xml               | 46.6 ms                                                         | 53.9 ms: 1.16x slower                                           |
| coroutines               | 17.9 ms                                                         | 20.9 ms: 1.17x slower                                           |
| deepcopy_reduce          | 2.68 us                                                         | 3.16 us: 1.18x slower                                           |
| genshi_text              | 21.0 ms                                                         | 24.9 ms: 1.19x slower                                           |
| xml_etree_generate       | 61.6 ms                                                         | 73.6 ms: 1.19x slower                                           |
| regex_effbot             | 1.66 ms                                                         | 2.00 ms: 1.21x slower                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.96 ms: 1.22x slower                                           |
| scimark_fft              | 216 ms                                                          | 271 ms: 1.26x slower                                            |
| generators               | 31.6 ms                                                         | 39.9 ms: 1.27x slower                                           |
| deepcopy_memo            | 29.6 us                                                         | 37.7 us: 1.28x slower                                           |
| async_generators         | 241 ms                                                          | 313 ms: 1.30x slower                                            |
| logging_format           | 7.91 us                                                         | 10.3 us: 1.30x slower                                           |
| logging_simple           | 7.29 us                                                         | 9.61 us: 1.32x slower                                           |
| spectral_norm            | 80.2 ms                                                         | 106 ms: 1.32x slower                                            |
| nbody                    | 79.1 ms                                                         | 125 ms: 1.57x slower                                            |
| Geometric mean           | (ref)                                                           | 1.01x faster                                                    |

Benchmark hidden because not significant (4): python_startup_no_site, pickle, raytrace, pickle_list
Ignored benchmarks (2) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, unpack_sequence
Ignored benchmarks (4) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 71.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown