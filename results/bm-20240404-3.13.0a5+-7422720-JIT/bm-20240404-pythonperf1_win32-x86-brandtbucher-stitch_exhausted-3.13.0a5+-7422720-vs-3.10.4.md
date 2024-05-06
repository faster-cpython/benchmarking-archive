# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 99.20%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| chameleon      | 6.42 ms                                                         | 6.35 ms: 1.01x faster                                                             |
| docutils       | 1.95 sec                                                        | 1.97 sec: 1.01x slower                                                            |
| html5lib       | 52.1 ms                                                         | 46.1 ms: 1.13x faster                                                             |
| tornado_http   | 118 ms                                                          | 97.5 ms: 1.21x faster                                                             |
| Geometric mean | (ref)                                                           | 1.06x faster                                                                      |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 491 ms: 1.88x faster                                                              |
| async_tree_io           | 940 ms                                                          | 549 ms: 1.71x faster                                                              |
| async_tree_none         | 394 ms                                                          | 244 ms: 1.62x faster                                                              |
| async_tree_memoization  | 467 ms                                                          | 294 ms: 1.59x faster                                                              |
| Geometric mean          | (ref)                                                           | 1.69x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                              |
| float          | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                             |
| nbody          | 79.1 ms                                                         | 96.6 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 116 ms: 1.12x faster                                                              |
| regex_compile  | 117 ms                                                          | 110 ms: 1.06x faster                                                              |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                             |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                             |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.96 ms: 1.41x faster                                                             |
| pickle_pure_python   | 280 us                                                          | 226 us: 1.24x faster                                                              |
| tomli_loads          | 1.91 sec                                                        | 1.70 sec: 1.12x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.12x faster                                                              |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                             |
| unpickle_pure_python | 189 us                                                          | 172 us: 1.10x faster                                                              |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.2 ms: 1.09x faster                                                             |
| xml_etree_process    | 48.1 ms                                                         | 44.9 ms: 1.07x faster                                                             |
| unpickle_list        | 2.98 us                                                         | 2.82 us: 1.06x faster                                                             |
| pickle_list          | 3.22 us                                                         | 3.19 us: 1.01x faster                                                             |
| pickle               | 7.83 us                                                         | 7.90 us: 1.01x slower                                                             |
| unpickle             | 9.82 us                                                         | 9.93 us: 1.01x slower                                                             |
| xml_etree_generate   | 61.6 ms                                                         | 62.3 ms: 1.01x slower                                                             |
| pickle_dict          | 18.2 us                                                         | 19.8 us: 1.09x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                             |
| python_startup_no_site | 18.1 ms                                                         | 22.1 ms: 1.22x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 7.00 ms: 1.30x faster                                                             |
| genshi_xml     | 46.6 ms                                                         | 48.5 ms: 1.04x slower                                                             |
| genshi_text    | 21.0 ms                                                         | 23.8 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 105 us: 3.75x faster                                                              |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                              |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 491 ms: 1.88x faster                                                              |
| async_tree_io            | 940 ms                                                          | 549 ms: 1.71x faster                                                              |
| pylint                   | 384 ms                                                          | 228 ms: 1.69x faster                                                              |
| async_tree_none          | 394 ms                                                          | 244 ms: 1.62x faster                                                              |
| logging_silent           | 97.9 ns                                                         | 61.2 ns: 1.60x faster                                                             |
| async_tree_memoization   | 467 ms                                                          | 294 ms: 1.59x faster                                                              |
| deltablue                | 4.04 ms                                                         | 2.80 ms: 1.44x faster                                                             |
| generators               | 31.6 ms                                                         | 21.9 ms: 1.44x faster                                                             |
| json_dumps               | 9.82 ms                                                         | 6.96 ms: 1.41x faster                                                             |
| raytrace                 | 303 ms                                                          | 222 ms: 1.36x faster                                                              |
| sqlglot_parse            | 1.33 ms                                                         | 1.02 ms: 1.31x faster                                                             |
| mako                     | 9.10 ms                                                         | 7.00 ms: 1.30x faster                                                             |
| float                    | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                             |
| crypto_pyaes             | 81.3 ms                                                         | 63.0 ms: 1.29x faster                                                             |
| go                       | 146 ms                                                          | 114 ms: 1.28x faster                                                              |
| richards_super           | 49.9 ms                                                         | 39.6 ms: 1.26x faster                                                             |
| pycparser                | 1.04 sec                                                        | 837 ms: 1.24x faster                                                              |
| pickle_pure_python       | 280 us                                                          | 226 us: 1.24x faster                                                              |
| sqlglot_transpile        | 1.58 ms                                                         | 1.28 ms: 1.23x faster                                                             |
| chaos                    | 74.4 ms                                                         | 61.0 ms: 1.22x faster                                                             |
| asyncio_tcp              | 744 ms                                                          | 616 ms: 1.21x faster                                                              |
| tornado_http             | 118 ms                                                          | 97.5 ms: 1.21x faster                                                             |
| coroutines               | 17.9 ms                                                         | 14.9 ms: 1.21x faster                                                             |
| scimark_sor              | 115 ms                                                          | 97.2 ms: 1.18x faster                                                             |
| sqlite_synth             | 2.29 us                                                         | 1.95 us: 1.17x faster                                                             |
| pyflate                  | 422 ms                                                          | 362 ms: 1.16x faster                                                              |
| richards                 | 40.3 ms                                                         | 34.9 ms: 1.15x faster                                                             |
| deepcopy_memo            | 29.6 us                                                         | 25.8 us: 1.15x faster                                                             |
| spectral_norm            | 80.2 ms                                                         | 70.5 ms: 1.14x faster                                                             |
| html5lib                 | 52.1 ms                                                         | 46.1 ms: 1.13x faster                                                             |
| bench_thread_pool        | 1.12 ms                                                         | 994 us: 1.13x faster                                                              |
| tomli_loads              | 1.91 sec                                                        | 1.70 sec: 1.12x faster                                                            |
| regex_dna                | 131 ms                                                          | 116 ms: 1.12x faster                                                              |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.12x faster                                                              |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                             |
| json                     | 4.76 ms                                                         | 4.32 ms: 1.10x faster                                                             |
| unpickle_pure_python     | 189 us                                                          | 172 us: 1.10x faster                                                              |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.2 ms: 1.09x faster                                                             |
| sympy_sum                | 122 ms                                                          | 114 ms: 1.08x faster                                                              |
| comprehensions           | 17.7 us                                                         | 16.5 us: 1.07x faster                                                             |
| xml_etree_process        | 48.1 ms                                                         | 44.9 ms: 1.07x faster                                                             |
| regex_compile            | 117 ms                                                          | 110 ms: 1.06x faster                                                              |
| unpickle_list            | 2.98 us                                                         | 2.82 us: 1.06x faster                                                             |
| scimark_lu               | 89.8 ms                                                         | 87.3 ms: 1.03x faster                                                             |
| deepcopy                 | 310 us                                                          | 302 us: 1.03x faster                                                              |
| sympy_str                | 229 ms                                                          | 224 ms: 1.02x faster                                                              |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.20 ms: 1.01x faster                                                             |
| chameleon                | 6.42 ms                                                         | 6.35 ms: 1.01x faster                                                             |
| sympy_expand             | 391 ms                                                          | 387 ms: 1.01x faster                                                              |
| mdp                      | 1.83 sec                                                        | 1.81 sec: 1.01x faster                                                            |
| pickle_list              | 3.22 us                                                         | 3.19 us: 1.01x faster                                                             |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.9 sec: 1.01x faster                                                            |
| pickle                   | 7.83 us                                                         | 7.90 us: 1.01x slower                                                             |
| unpickle                 | 9.82 us                                                         | 9.93 us: 1.01x slower                                                             |
| xml_etree_generate       | 61.6 ms                                                         | 62.3 ms: 1.01x slower                                                             |
| docutils                 | 1.95 sec                                                        | 1.97 sec: 1.01x slower                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 62.7 ms: 1.01x slower                                                             |
| deepcopy_reduce          | 2.68 us                                                         | 2.72 us: 1.01x slower                                                             |
| fannkuch                 | 317 ms                                                          | 324 ms: 1.02x slower                                                              |
| sympy_integrate          | 16.6 ms                                                         | 17.1 ms: 1.03x slower                                                             |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                             |
| genshi_xml               | 46.6 ms                                                         | 48.5 ms: 1.04x slower                                                             |
| meteor_contest           | 80.0 ms                                                         | 83.4 ms: 1.04x slower                                                             |
| python_startup           | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                             |
| pathlib                  | 81.2 ms                                                         | 86.6 ms: 1.07x slower                                                             |
| sqlglot_optimize         | 44.7 ms                                                         | 48.1 ms: 1.08x slower                                                             |
| hexiom                   | 6.13 ms                                                         | 6.60 ms: 1.08x slower                                                             |
| create_gc_cycles         | 694 us                                                          | 748 us: 1.08x slower                                                              |
| sqlglot_normalize        | 230 ms                                                          | 250 ms: 1.08x slower                                                              |
| pickle_dict              | 18.2 us                                                         | 19.8 us: 1.09x slower                                                             |
| nqueens                  | 87.1 ms                                                         | 95.1 ms: 1.09x slower                                                             |
| bench_mp_pool            | 66.4 ms                                                         | 72.8 ms: 1.10x slower                                                             |
| logging_format           | 7.91 us                                                         | 8.72 us: 1.10x slower                                                             |
| pprint_pformat           | 1.37 sec                                                        | 1.52 sec: 1.11x slower                                                            |
| logging_simple           | 7.29 us                                                         | 8.13 us: 1.12x slower                                                             |
| scimark_fft              | 216 ms                                                          | 241 ms: 1.12x slower                                                              |
| pprint_safe_repr         | 658 ms                                                          | 735 ms: 1.12x slower                                                              |
| gc_traversal             | 1.28 ms                                                         | 1.44 ms: 1.12x slower                                                             |
| genshi_text              | 21.0 ms                                                         | 23.8 ms: 1.13x slower                                                             |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                             |
| async_generators         | 241 ms                                                          | 280 ms: 1.16x slower                                                              |
| nbody                    | 79.1 ms                                                         | 96.6 ms: 1.22x slower                                                             |
| python_startup_no_site   | 18.1 ms                                                         | 22.1 ms: 1.22x slower                                                             |
| telco                    | 4.83 ms                                                         | 6.40 ms: 1.33x slower                                                             |
| coverage                 | 46.6 ms                                                         | 503 ms: 10.80x slower                                                             |
| thrift                   | 902 us                                                          | 10.7 ms: 11.87x slower                                                            |
| Geometric mean           | (ref)                                                           | 1.05x faster                                                                      |

Benchmark hidden because not significant (1): 2to3
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.20% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown