# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 226 ms: 1.17x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.65 ms: 1.14x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.79 sec: 1.09x faster                                                          |
| html5lib       | 52.1 ms                                                         | 41.7 ms: 1.25x faster                                                           |
| tornado_http   | 118 ms                                                          | 92.5 ms: 1.27x faster                                                           |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 464 ms: 1.99x faster                                                            |
| async_tree_io           | 940 ms                                                          | 519 ms: 1.81x faster                                                            |
| async_tree_none         | 394 ms                                                          | 222 ms: 1.77x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 265 ms: 1.76x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.83x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| float          | 69.6 ms                                                         | 53.4 ms: 1.30x faster                                                           |
| Geometric mean | (ref)                                                           | 1.50x faster                                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 95.9 ms: 1.22x faster                                                           |
| regex_dna      | 131 ms                                                          | 117 ms: 1.12x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.0 ms: 1.01x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.88 ms: 1.13x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.60 ms: 1.49x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 137 us: 1.39x faster                                                            |
| pickle_pure_python   | 280 us                                                          | 203 us: 1.38x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.58 sec: 1.21x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 42.6 ms: 1.13x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.9 ms: 1.08x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.78 us: 1.07x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 62.0 ms: 1.01x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.24 us: 1.01x slower                                                           |
| pickle               | 7.83 us                                                         | 8.02 us: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.9 ms                                                         | 21.9 ms: 1.05x faster                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 6.74 ms: 1.35x faster                                                           |
| genshi_text    | 21.0 ms                                                         | 18.5 ms: 1.13x faster                                                           |
| genshi_xml     | 46.6 ms                                                         | 41.8 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                           | 1.19x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 93.0 us: 4.25x faster                                                           |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 464 ms: 1.99x faster                                                            |
| deltablue                | 4.04 ms                                                         | 2.12 ms: 1.91x faster                                                           |
| pylint                   | 384 ms                                                          | 206 ms: 1.86x faster                                                            |
| async_tree_io            | 940 ms                                                          | 519 ms: 1.81x faster                                                            |
| async_tree_none          | 394 ms                                                          | 222 ms: 1.77x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 265 ms: 1.76x faster                                                            |
| raytrace                 | 303 ms                                                          | 180 ms: 1.68x faster                                                            |
| chaos                    | 74.4 ms                                                         | 45.3 ms: 1.64x faster                                                           |
| logging_silent           | 97.9 ns                                                         | 61.7 ns: 1.59x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 862 us: 1.54x faster                                                            |
| richards_super           | 49.9 ms                                                         | 32.8 ms: 1.52x faster                                                           |
| comprehensions           | 17.7 us                                                         | 11.7 us: 1.51x faster                                                           |
| go                       | 146 ms                                                          | 96.6 ms: 1.51x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.60 ms: 1.49x faster                                                           |
| scimark_sor              | 115 ms                                                          | 77.9 ms: 1.48x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 55.1 ms: 1.47x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 4.19 ms: 1.46x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.09 ms: 1.45x faster                                                           |
| scimark_lu               | 89.8 ms                                                         | 61.9 ms: 1.45x faster                                                           |
| generators               | 31.6 ms                                                         | 22.2 ms: 1.42x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 137 us: 1.39x faster                                                            |
| richards                 | 40.3 ms                                                         | 29.0 ms: 1.39x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 203 us: 1.38x faster                                                            |
| pycparser                | 1.04 sec                                                        | 760 ms: 1.37x faster                                                            |
| pyflate                  | 422 ms                                                          | 309 ms: 1.36x faster                                                            |
| mako                     | 9.10 ms                                                         | 6.74 ms: 1.35x faster                                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 46.0 ms: 1.35x faster                                                           |
| float                    | 69.6 ms                                                         | 53.4 ms: 1.30x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 22.7 us: 1.30x faster                                                           |
| tornado_http             | 118 ms                                                          | 92.5 ms: 1.27x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 69.3 ms: 1.26x faster                                                           |
| coroutines               | 17.9 ms                                                         | 14.3 ms: 1.26x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 41.7 ms: 1.25x faster                                                           |
| regex_compile            | 117 ms                                                          | 95.9 ms: 1.22x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.58 sec: 1.21x faster                                                          |
| sympy_sum                | 122 ms                                                          | 101 ms: 1.21x faster                                                            |
| pprint_pformat           | 1.37 sec                                                        | 1.14 sec: 1.20x faster                                                          |
| sqlite_synth             | 2.29 us                                                         | 1.91 us: 1.20x faster                                                           |
| fannkuch                 | 317 ms                                                          | 266 ms: 1.19x faster                                                            |
| pprint_safe_repr         | 658 ms                                                          | 558 ms: 1.18x faster                                                            |
| json                     | 4.76 ms                                                         | 4.04 ms: 1.18x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 14.2 ms: 1.17x faster                                                           |
| 2to3                     | 265 ms                                                          | 226 ms: 1.17x faster                                                            |
| spectral_norm            | 80.2 ms                                                         | 68.5 ms: 1.17x faster                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 38.4 ms: 1.17x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 639 ms: 1.16x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.57 sec: 1.16x faster                                                          |
| sqlglot_normalize        | 230 ms                                                          | 200 ms: 1.15x faster                                                            |
| sympy_str                | 229 ms                                                          | 199 ms: 1.15x faster                                                            |
| deepcopy                 | 310 us                                                          | 269 us: 1.15x faster                                                            |
| chameleon                | 6.42 ms                                                         | 5.65 ms: 1.14x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 986 us: 1.14x faster                                                            |
| genshi_text              | 21.0 ms                                                         | 18.5 ms: 1.13x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 42.6 ms: 1.13x faster                                                           |
| sympy_expand             | 391 ms                                                          | 349 ms: 1.12x faster                                                            |
| regex_dna                | 131 ms                                                          | 117 ms: 1.12x faster                                                            |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| genshi_xml               | 46.6 ms                                                         | 41.8 ms: 1.11x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| docutils                 | 1.95 sec                                                        | 1.79 sec: 1.09x faster                                                          |
| deepcopy_reduce          | 2.68 us                                                         | 2.48 us: 1.08x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.9 ms: 1.08x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.78 us: 1.07x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.07 ms: 1.06x faster                                                           |
| python_startup           | 22.9 ms                                                         | 21.9 ms: 1.05x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 76.7 ms: 1.04x faster                                                           |
| scimark_fft              | 216 ms                                                          | 211 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| xml_etree_generate       | 61.6 ms                                                         | 62.0 ms: 1.01x slower                                                           |
| pickle_list              | 3.22 us                                                         | 3.24 us: 1.01x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.0 ms: 1.01x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.04 us: 1.02x slower                                                           |
| pickle                   | 7.83 us                                                         | 8.02 us: 1.02x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 67.9 ms: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 83.4 ms: 1.03x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.49 us: 1.03x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 723 us: 1.04x slower                                                            |
| pickle_dict              | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.88 ms: 1.13x slower                                                           |
| async_generators         | 241 ms                                                          | 287 ms: 1.19x slower                                                            |
| telco                    | 4.83 ms                                                         | 5.93 ms: 1.23x slower                                                           |
| thrift                   | 902 us                                                          | 9.72 ms: 10.77x slower                                                          |
| coverage                 | 46.6 ms                                                         | 503 ms: 10.80x slower                                                           |
| Geometric mean           | (ref)                                                           | 1.17x faster                                                                    |

Benchmark hidden because not significant (2): nbody, python_startup_no_site
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: unknown