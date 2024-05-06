# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.05x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 258 ms: 1.03x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.25 ms: 1.03x faster                                                           |
| html5lib       | 52.1 ms                                                         | 46.6 ms: 1.12x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.9 ms: 1.21x faster                                                           |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 490 ms: 1.88x faster                                                            |
| async_tree_io           | 940 ms                                                          | 556 ms: 1.69x faster                                                            |
| async_tree_none         | 394 ms                                                          | 241 ms: 1.63x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 290 ms: 1.61x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.70x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 198 ms: 2.53x faster                                                            |
| float          | 69.6 ms                                                         | 53.1 ms: 1.31x faster                                                           |
| nbody          | 79.1 ms                                                         | 94.8 ms: 1.20x slower                                                           |
| Geometric mean | (ref)                                                           | 1.40x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 121 ms: 1.08x faster                                                            |
| regex_compile  | 117 ms                                                          | 112 ms: 1.04x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 222 us: 1.26x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 106 ms: 1.13x faster                                                            |
| json_loads           | 22.4 us                                                         | 20.0 us: 1.12x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 172 us: 1.10x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.0 ms: 1.09x faster                                                           |
| xml_etree_process    | 48.1 ms                                                         | 44.2 ms: 1.09x faster                                                           |
| tomli_loads          | 1.91 sec                                                        | 1.80 sec: 1.06x faster                                                          |
| unpickle_list        | 2.98 us                                                         | 2.82 us: 1.06x faster                                                           |
| unpickle             | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.33 us: 1.03x slower                                                           |
| pickle               | 7.83 us                                                         | 8.13 us: 1.04x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.0 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 22.0 ms: 1.22x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 6.99 ms: 1.30x faster                                                           |
| genshi_xml     | 46.6 ms                                                         | 48.4 ms: 1.04x slower                                                           |
| genshi_text    | 21.0 ms                                                         | 22.8 ms: 1.09x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 101 us: 3.94x faster                                                            |
| pidigits                 | 502 ms                                                          | 198 ms: 2.53x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 490 ms: 1.88x faster                                                            |
| pylint                   | 384 ms                                                          | 224 ms: 1.72x faster                                                            |
| async_tree_io            | 940 ms                                                          | 556 ms: 1.69x faster                                                            |
| async_tree_none          | 394 ms                                                          | 241 ms: 1.63x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 290 ms: 1.61x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 61.0 ns: 1.60x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.74 ms: 1.47x faster                                                           |
| generators               | 31.6 ms                                                         | 22.0 ms: 1.43x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.87 ms: 1.43x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 997 us: 1.33x faster                                                            |
| raytrace                 | 303 ms                                                          | 231 ms: 1.31x faster                                                            |
| float                    | 69.6 ms                                                         | 53.1 ms: 1.31x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 62.4 ms: 1.30x faster                                                           |
| mako                     | 9.10 ms                                                         | 6.99 ms: 1.30x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.25 ms: 1.27x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 222 us: 1.26x faster                                                            |
| richards_super           | 49.9 ms                                                         | 39.5 ms: 1.26x faster                                                           |
| pycparser                | 1.04 sec                                                        | 850 ms: 1.23x faster                                                            |
| chaos                    | 74.4 ms                                                         | 61.2 ms: 1.22x faster                                                           |
| tornado_http             | 118 ms                                                          | 96.9 ms: 1.21x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 24.8 us: 1.19x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.1 ms: 1.19x faster                                                           |
| go                       | 146 ms                                                          | 124 ms: 1.17x faster                                                            |
| pyflate                  | 422 ms                                                          | 362 ms: 1.17x faster                                                            |
| asyncio_tcp              | 744 ms                                                          | 642 ms: 1.16x faster                                                            |
| sqlite_synth             | 2.29 us                                                         | 1.98 us: 1.15x faster                                                           |
| json                     | 4.76 ms                                                         | 4.13 ms: 1.15x faster                                                           |
| scimark_sor              | 115 ms                                                          | 101 ms: 1.14x faster                                                            |
| richards                 | 40.3 ms                                                         | 35.2 ms: 1.14x faster                                                           |
| comprehensions           | 17.7 us                                                         | 15.6 us: 1.14x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 106 ms: 1.13x faster                                                            |
| json_loads               | 22.4 us                                                         | 20.0 us: 1.12x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 1.00 ms: 1.12x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 46.6 ms: 1.12x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 172 us: 1.10x faster                                                            |
| sympy_sum                | 122 ms                                                          | 112 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.0 ms: 1.09x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 73.6 ms: 1.09x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 44.2 ms: 1.09x faster                                                           |
| regex_dna                | 131 ms                                                          | 121 ms: 1.08x faster                                                            |
| deepcopy                 | 310 us                                                          | 291 us: 1.07x faster                                                            |
| tomli_loads              | 1.91 sec                                                        | 1.80 sec: 1.06x faster                                                          |
| unpickle_list            | 2.98 us                                                         | 2.82 us: 1.06x faster                                                           |
| regex_compile            | 117 ms                                                          | 112 ms: 1.04x faster                                                            |
| scimark_lu               | 89.8 ms                                                         | 86.2 ms: 1.04x faster                                                           |
| sympy_str                | 229 ms                                                          | 221 ms: 1.04x faster                                                            |
| 2to3                     | 265 ms                                                          | 258 ms: 1.03x faster                                                            |
| chameleon                | 6.42 ms                                                         | 6.25 ms: 1.03x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.61 us: 1.03x faster                                                           |
| sympy_expand             | 391 ms                                                          | 382 ms: 1.02x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.80 sec: 1.01x faster                                                          |
| hexiom                   | 6.13 ms                                                         | 6.10 ms: 1.01x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 16.6 ms: 1.00x faster                                                           |
| fannkuch                 | 317 ms                                                          | 321 ms: 1.01x slower                                                            |
| sqlglot_normalize        | 230 ms                                                          | 233 ms: 1.01x slower                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 63.3 ms: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 46.2 ms: 1.03x slower                                                           |
| meteor_contest           | 80.0 ms                                                         | 82.6 ms: 1.03x slower                                                           |
| pickle_list              | 3.22 us                                                         | 3.33 us: 1.03x slower                                                           |
| pickle                   | 7.83 us                                                         | 8.13 us: 1.04x slower                                                           |
| genshi_xml               | 46.6 ms                                                         | 48.4 ms: 1.04x slower                                                           |
| python_startup           | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 87.1 ms: 1.07x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 745 us: 1.07x slower                                                            |
| nqueens                  | 87.1 ms                                                         | 94.2 ms: 1.08x slower                                                           |
| genshi_text              | 21.0 ms                                                         | 22.8 ms: 1.09x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.0 us: 1.10x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.76 us: 1.11x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 73.8 ms: 1.11x slower                                                           |
| logging_simple           | 7.29 us                                                         | 8.11 us: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.44 ms: 1.12x slower                                                           |
| scimark_fft              | 216 ms                                                          | 245 ms: 1.13x slower                                                            |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.58 sec: 1.15x slower                                                          |
| pprint_safe_repr         | 658 ms                                                          | 769 ms: 1.17x slower                                                            |
| async_generators         | 241 ms                                                          | 288 ms: 1.19x slower                                                            |
| nbody                    | 79.1 ms                                                         | 94.8 ms: 1.20x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 22.0 ms: 1.22x slower                                                           |
| telco                    | 4.83 ms                                                         | 6.43 ms: 1.33x slower                                                           |
| coverage                 | 46.6 ms                                                         | 531 ms: 11.40x slower                                                           |
| thrift                   | 902 us                                                          | 10.7 ms: 11.90x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.05x faster                                                                    |

Benchmark hidden because not significant (4): scimark_sparse_mat_mult, asyncio_tcp_ssl, xml_etree_generate, docutils
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown