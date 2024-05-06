# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 245 ms: 1.08x faster                                                            |
| chameleon      | 6.42 ms                                                         | 5.70 ms: 1.13x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| html5lib       | 52.1 ms                                                         | 44.8 ms: 1.16x faster                                                           |
| tornado_http   | 118 ms                                                          | 97.7 ms: 1.20x faster                                                           |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 472 ms: 1.95x faster                                                            |
| async_tree_io           | 940 ms                                                          | 531 ms: 1.77x faster                                                            |
| async_tree_none         | 394 ms                                                          | 226 ms: 1.74x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 274 ms: 1.71x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.79x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| float          | 69.6 ms                                                         | 61.1 ms: 1.14x faster                                                           |
| nbody          | 79.1 ms                                                         | 82.9 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 123 ms: 1.06x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.02x slower                                                           |
| regex_compile  | 117 ms                                                          | 125 ms: 1.07x slower                                                            |
| regex_effbot   | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.64 ms: 1.48x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 211 us: 1.33x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 42.8 ms: 1.12x faster                                                           |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| unpickle_pure_python | 189 us                                                          | 176 us: 1.08x faster                                                            |
| unpickle_list        | 2.98 us                                                         | 2.79 us: 1.07x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 67.9 ms: 1.04x faster                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 61.0 ms: 1.01x faster                                                           |
| pickle               | 7.83 us                                                         | 7.78 us: 1.01x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.29 us: 1.02x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 22.6 ms: 1.02x faster                                                           |
| python_startup_no_site | 18.1 ms                                                         | 18.8 ms: 1.04x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 7.60 ms: 1.20x faster                                                           |
| genshi_text    | 21.0 ms                                                         | 19.6 ms: 1.07x faster                                                           |
| genshi_xml     | 46.6 ms                                                         | 45.0 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 94.5 us: 4.19x faster                                                           |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 472 ms: 1.95x faster                                                            |
| async_tree_io            | 940 ms                                                          | 531 ms: 1.77x faster                                                            |
| pylint                   | 384 ms                                                          | 219 ms: 1.75x faster                                                            |
| async_tree_none          | 394 ms                                                          | 226 ms: 1.74x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 274 ms: 1.71x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 60.5 ns: 1.62x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.67 ms: 1.51x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.64 ms: 1.48x faster                                                           |
| richards_super           | 49.9 ms                                                         | 34.4 ms: 1.45x faster                                                           |
| raytrace                 | 303 ms                                                          | 215 ms: 1.41x faster                                                            |
| chaos                    | 74.4 ms                                                         | 53.4 ms: 1.39x faster                                                           |
| generators               | 31.6 ms                                                         | 22.8 ms: 1.38x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 965 us: 1.38x faster                                                            |
| crypto_pyaes             | 81.3 ms                                                         | 59.0 ms: 1.38x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 211 us: 1.33x faster                                                            |
| sqlglot_transpile        | 1.58 ms                                                         | 1.20 ms: 1.32x faster                                                           |
| richards                 | 40.3 ms                                                         | 30.7 ms: 1.31x faster                                                           |
| pycparser                | 1.04 sec                                                        | 827 ms: 1.26x faster                                                            |
| coroutines               | 17.9 ms                                                         | 14.5 ms: 1.24x faster                                                           |
| comprehensions           | 17.7 us                                                         | 14.5 us: 1.22x faster                                                           |
| scimark_sor              | 115 ms                                                          | 94.4 ms: 1.22x faster                                                           |
| go                       | 146 ms                                                          | 120 ms: 1.22x faster                                                            |
| tornado_http             | 118 ms                                                          | 97.7 ms: 1.20x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.60 ms: 1.20x faster                                                           |
| pyflate                  | 422 ms                                                          | 355 ms: 1.19x faster                                                            |
| asyncio_tcp              | 744 ms                                                          | 628 ms: 1.18x faster                                                            |
| sqlite_synth             | 2.29 us                                                         | 1.94 us: 1.18x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| html5lib                 | 52.1 ms                                                         | 44.8 ms: 1.16x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 25.6 us: 1.16x faster                                                           |
| json                     | 4.76 ms                                                         | 4.12 ms: 1.15x faster                                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 53.8 ms: 1.15x faster                                                           |
| deepcopy                 | 310 us                                                          | 269 us: 1.15x faster                                                            |
| float                    | 69.6 ms                                                         | 61.1 ms: 1.14x faster                                                           |
| chameleon                | 6.42 ms                                                         | 5.70 ms: 1.13x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 42.8 ms: 1.12x faster                                                           |
| bench_thread_pool        | 1.12 ms                                                         | 1.00 ms: 1.12x faster                                                           |
| mdp                      | 1.83 sec                                                        | 1.63 sec: 1.12x faster                                                          |
| deepcopy_reduce          | 2.68 us                                                         | 2.41 us: 1.12x faster                                                           |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| nqueens                  | 87.1 ms                                                         | 78.2 ms: 1.11x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| sympy_sum                | 122 ms                                                          | 113 ms: 1.09x faster                                                            |
| 2to3                     | 265 ms                                                          | 245 ms: 1.08x faster                                                            |
| unpickle_pure_python     | 189 us                                                          | 176 us: 1.08x faster                                                            |
| fannkuch                 | 317 ms                                                          | 295 ms: 1.07x faster                                                            |
| genshi_text              | 21.0 ms                                                         | 19.6 ms: 1.07x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.79 us: 1.07x faster                                                           |
| regex_dna                | 131 ms                                                          | 123 ms: 1.06x faster                                                            |
| scimark_lu               | 89.8 ms                                                         | 85.1 ms: 1.05x faster                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.31 sec: 1.05x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 16.0 ms: 1.04x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 67.9 ms: 1.04x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 5.89 ms: 1.04x faster                                                           |
| pprint_safe_repr         | 658 ms                                                          | 635 ms: 1.04x faster                                                            |
| genshi_xml               | 46.6 ms                                                         | 45.0 ms: 1.03x faster                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 43.3 ms: 1.03x faster                                                           |
| sympy_str                | 229 ms                                                          | 224 ms: 1.02x faster                                                            |
| sqlglot_normalize        | 230 ms                                                          | 225 ms: 1.02x faster                                                            |
| docutils                 | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| python_startup           | 22.9 ms                                                         | 22.6 ms: 1.02x faster                                                           |
| meteor_contest           | 80.0 ms                                                         | 79.2 ms: 1.01x faster                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 61.0 ms: 1.01x faster                                                           |
| pickle                   | 7.83 us                                                         | 7.78 us: 1.01x faster                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| pickle_list              | 3.22 us                                                         | 3.29 us: 1.02x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.02x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 83.6 ms: 1.03x slower                                                           |
| scimark_fft              | 216 ms                                                          | 223 ms: 1.03x slower                                                            |
| python_startup_no_site   | 18.1 ms                                                         | 18.8 ms: 1.04x slower                                                           |
| nbody                    | 79.1 ms                                                         | 82.9 ms: 1.05x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 735 us: 1.06x slower                                                            |
| logging_format           | 7.91 us                                                         | 8.40 us: 1.06x slower                                                           |
| logging_simple           | 7.29 us                                                         | 7.75 us: 1.06x slower                                                           |
| regex_compile            | 117 ms                                                          | 125 ms: 1.07x slower                                                            |
| bench_mp_pool            | 66.4 ms                                                         | 71.6 ms: 1.08x slower                                                           |
| spectral_norm            | 80.2 ms                                                         | 86.7 ms: 1.08x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.12x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.90 ms: 1.14x slower                                                           |
| async_generators         | 241 ms                                                          | 301 ms: 1.25x slower                                                            |
| telco                    | 4.83 ms                                                         | 6.34 ms: 1.31x slower                                                           |
| coverage                 | 46.6 ms                                                         | 507 ms: 10.89x slower                                                           |
| thrift                   | 902 us                                                          | 11.3 ms: 12.50x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (3): scimark_sparse_mat_mult, sympy_expand, unpickle
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown