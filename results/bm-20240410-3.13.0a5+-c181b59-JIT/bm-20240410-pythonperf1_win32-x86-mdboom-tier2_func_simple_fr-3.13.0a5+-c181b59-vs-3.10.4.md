# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.07x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 255 ms: 1.04x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.27 ms: 1.02x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.93 sec: 1.01x faster                                                          |
| html5lib       | 52.1 ms                                                         | 45.4 ms: 1.15x faster                                                           |
| tornado_http   | 118 ms                                                          | 95.5 ms: 1.23x faster                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 491 ms: 1.88x faster                                                            |
| async_tree_io           | 940 ms                                                          | 553 ms: 1.70x faster                                                            |
| async_tree_none         | 394 ms                                                          | 238 ms: 1.65x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 287 ms: 1.63x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.71x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| float          | 69.6 ms                                                         | 53.2 ms: 1.31x faster                                                           |
| nbody          | 79.1 ms                                                         | 96.9 ms: 1.22x slower                                                           |
| Geometric mean | (ref)                                                           | 1.40x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| regex_compile  | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.84 ms: 1.44x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 216 us: 1.29x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.71 sec: 1.12x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 43.0 ms: 1.12x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.12x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 174 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.7 ms: 1.08x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.82 us: 1.06x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.17 us: 1.01x faster                                                           |
| pickle               | 7.83 us                                                         | 7.94 us: 1.01x slower                                                           |
| unpickle             | 9.82 us                                                         | 10.2 us: 1.03x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 19.8 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 23.9 ms: 1.04x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 7.13 ms: 1.28x faster                                                           |
| genshi_text    | 21.0 ms                                                         | 20.7 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 96.1 us: 4.12x faster                                                           |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 491 ms: 1.88x faster                                                            |
| pylint                   | 384 ms                                                          | 220 ms: 1.74x faster                                                            |
| async_tree_io            | 940 ms                                                          | 553 ms: 1.70x faster                                                            |
| async_tree_none          | 394 ms                                                          | 238 ms: 1.65x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 59.4 ns: 1.65x faster                                                           |
| async_tree_memoization   | 467 ms                                                          | 287 ms: 1.63x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.72 ms: 1.48x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.84 ms: 1.44x faster                                                           |
| generators               | 31.6 ms                                                         | 22.3 ms: 1.41x faster                                                           |
| raytrace                 | 303 ms                                                          | 220 ms: 1.38x faster                                                            |
| sqlglot_parse            | 1.33 ms                                                         | 988 us: 1.35x faster                                                            |
| float                    | 69.6 ms                                                         | 53.2 ms: 1.31x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 216 us: 1.29x faster                                                            |
| crypto_pyaes             | 81.3 ms                                                         | 63.5 ms: 1.28x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.13 ms: 1.28x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.24 ms: 1.28x faster                                                           |
| richards_super           | 49.9 ms                                                         | 39.5 ms: 1.26x faster                                                           |
| pycparser                | 1.04 sec                                                        | 841 ms: 1.24x faster                                                            |
| tornado_http             | 118 ms                                                          | 95.5 ms: 1.23x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 607 ms: 1.23x faster                                                            |
| chaos                    | 74.4 ms                                                         | 61.9 ms: 1.20x faster                                                           |
| coroutines               | 17.9 ms                                                         | 15.1 ms: 1.19x faster                                                           |
| go                       | 146 ms                                                          | 123 ms: 1.18x faster                                                            |
| scimark_sor              | 115 ms                                                          | 97.4 ms: 1.18x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.95 us: 1.18x faster                                                           |
| pyflate                  | 422 ms                                                          | 361 ms: 1.17x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 25.3 us: 1.17x faster                                                           |
| richards                 | 40.3 ms                                                         | 34.8 ms: 1.16x faster                                                           |
| json                     | 4.76 ms                                                         | 4.12 ms: 1.16x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 45.4 ms: 1.15x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 981 us: 1.14x faster                                                            |
| comprehensions           | 17.7 us                                                         | 15.6 us: 1.13x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 71.0 ms: 1.13x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.71 sec: 1.12x faster                                                          |
| xml_etree_process        | 48.1 ms                                                         | 43.0 ms: 1.12x faster                                                           |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.12x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| sympy_sum                | 122 ms                                                          | 110 ms: 1.11x faster                                                            |
| unpickle_pure_python     | 189 us                                                          | 174 us: 1.09x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.7 ms: 1.08x faster                                                           |
| regex_dna                | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| unpickle_list            | 2.98 us                                                         | 2.82 us: 1.06x faster                                                           |
| sympy_str                | 229 ms                                                          | 217 ms: 1.06x faster                                                            |
| regex_compile            | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.73 sec: 1.06x faster                                                          |
| deepcopy                 | 310 us                                                          | 294 us: 1.06x faster                                                            |
| sympy_expand             | 391 ms                                                          | 373 ms: 1.05x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 59.4 ms: 1.04x faster                                                           |
| 2to3                     | 265 ms                                                          | 255 ms: 1.04x faster                                                            |
| scimark_lu               | 89.8 ms                                                         | 87.5 ms: 1.03x faster                                                           |
| chameleon                | 6.42 ms                                                         | 6.27 ms: 1.02x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 16.4 ms: 1.02x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 60.7 ms: 1.02x faster                                                           |
| genshi_text              | 21.0 ms                                                         | 20.7 ms: 1.01x faster                                                           |
| pickle_list              | 3.22 us                                                         | 3.17 us: 1.01x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.93 sec: 1.01x faster                                                          |
| sqlglot_normalize        | 230 ms                                                          | 232 ms: 1.01x slower                                                            |
| pickle                   | 7.83 us                                                         | 7.94 us: 1.01x slower                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 45.4 ms: 1.02x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                           |
| meteor_contest           | 80.0 ms                                                         | 82.0 ms: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.2 us: 1.03x slower                                                           |
| fannkuch                 | 317 ms                                                          | 329 ms: 1.04x slower                                                            |
| pathlib                  | 81.2 ms                                                         | 84.6 ms: 1.04x slower                                                           |
| python_startup           | 22.9 ms                                                         | 23.9 ms: 1.04x slower                                                           |
| nqueens                  | 87.1 ms                                                         | 92.9 ms: 1.07x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.53 us: 1.08x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 749 us: 1.08x slower                                                            |
| bench_mp_pool            | 66.4 ms                                                         | 71.8 ms: 1.08x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 19.8 us: 1.09x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.93 us: 1.09x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.53 sec: 1.12x slower                                                          |
| gc_traversal             | 1.28 ms                                                         | 1.45 ms: 1.13x slower                                                           |
| scimark_fft              | 216 ms                                                          | 245 ms: 1.13x slower                                                            |
| pprint_safe_repr         | 658 ms                                                          | 749 ms: 1.14x slower                                                            |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| async_generators         | 241 ms                                                          | 286 ms: 1.19x slower                                                            |
| python_startup_no_site   | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                           |
| nbody                    | 79.1 ms                                                         | 96.9 ms: 1.22x slower                                                           |
| telco                    | 4.83 ms                                                         | 6.84 ms: 1.42x slower                                                           |
| coverage                 | 46.6 ms                                                         | 499 ms: 10.71x slower                                                           |
| thrift                   | 902 us                                                          | 10.5 ms: 11.69x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.07x faster                                                                    |

Benchmark hidden because not significant (5): asyncio_tcp_ssl, scimark_sparse_mat_mult, hexiom, genshi_xml, deepcopy_reduce
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown