# Results vs. 3.10.4

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.07x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 254 ms: 1.05x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.22 ms: 1.03x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| html5lib       | 52.1 ms                                                         | 45.0 ms: 1.16x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.2 ms: 1.25x faster                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 481 ms: 1.92x faster                                                            |
| async_tree_io           | 940 ms                                                          | 537 ms: 1.75x faster                                                            |
| async_tree_none         | 394 ms                                                          | 232 ms: 1.70x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 282 ms: 1.65x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.75x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| float          | 69.6 ms                                                         | 53.3 ms: 1.31x faster                                                           |
| nbody          | 79.1 ms                                                         | 97.3 ms: 1.23x slower                                                           |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| regex_compile  | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.4 ms: 1.04x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.62 ms: 1.48x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 220 us: 1.27x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.66 sec: 1.15x faster                                                          |
| unpickle_pure_python | 189 us                                                          | 166 us: 1.14x faster                                                            |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| xml_etree_process    | 48.1 ms                                                         | 44.3 ms: 1.09x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 111 ms: 1.08x faster                                                            |
| xml_etree_iterparse  | 70.8 ms                                                         | 66.9 ms: 1.06x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.83 us: 1.06x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.19 us: 1.01x faster                                                           |
| pickle               | 7.83 us                                                         | 8.01 us: 1.02x slower                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 63.2 ms: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 20.1 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 23.7 ms: 1.04x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 20.1 ms: 1.11x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 9.10 ms                                                         | 7.03 ms: 1.30x faster                                                           |
| genshi_xml     | 46.6 ms                                                         | 48.4 ms: 1.04x slower                                                           |
| genshi_text    | 21.0 ms                                                         | 22.5 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 93.8 us: 4.22x faster                                                           |
| pidigits                 | 502 ms                                                          | 197 ms: 2.55x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 481 ms: 1.92x faster                                                            |
| async_tree_io            | 940 ms                                                          | 537 ms: 1.75x faster                                                            |
| pylint                   | 384 ms                                                          | 220 ms: 1.74x faster                                                            |
| async_tree_none          | 394 ms                                                          | 232 ms: 1.70x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 282 ms: 1.65x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 60.3 ns: 1.62x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.68 ms: 1.51x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.62 ms: 1.48x faster                                                           |
| generators               | 31.6 ms                                                         | 22.1 ms: 1.43x faster                                                           |
| raytrace                 | 303 ms                                                          | 221 ms: 1.37x faster                                                            |
| sqlglot_parse            | 1.33 ms                                                         | 990 us: 1.34x faster                                                            |
| float                    | 69.6 ms                                                         | 53.3 ms: 1.31x faster                                                           |
| richards_super           | 49.9 ms                                                         | 38.3 ms: 1.30x faster                                                           |
| chaos                    | 74.4 ms                                                         | 57.3 ms: 1.30x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.03 ms: 1.30x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 63.5 ms: 1.28x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.24 ms: 1.27x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 220 us: 1.27x faster                                                            |
| tornado_http             | 118 ms                                                          | 94.2 ms: 1.25x faster                                                           |
| scimark_sor              | 115 ms                                                          | 93.7 ms: 1.23x faster                                                           |
| go                       | 146 ms                                                          | 120 ms: 1.21x faster                                                            |
| pycparser                | 1.04 sec                                                        | 859 ms: 1.21x faster                                                            |
| coroutines               | 17.9 ms                                                         | 14.9 ms: 1.21x faster                                                           |
| richards                 | 40.3 ms                                                         | 33.8 ms: 1.19x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 626 ms: 1.19x faster                                                            |
| pyflate                  | 422 ms                                                          | 361 ms: 1.17x faster                                                            |
| sqlite_synth             | 2.29 us                                                         | 1.97 us: 1.16x faster                                                           |
| comprehensions           | 17.7 us                                                         | 15.3 us: 1.16x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 25.5 us: 1.16x faster                                                           |
| html5lib                 | 52.1 ms                                                         | 45.0 ms: 1.16x faster                                                           |
| json                     | 4.76 ms                                                         | 4.13 ms: 1.15x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.66 sec: 1.15x faster                                                          |
| spectral_norm            | 80.2 ms                                                         | 70.0 ms: 1.15x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 166 us: 1.14x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 991 us: 1.13x faster                                                            |
| sympy_sum                | 122 ms                                                          | 109 ms: 1.13x faster                                                            |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                           |
| xml_etree_process        | 48.1 ms                                                         | 44.3 ms: 1.09x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 111 ms: 1.08x faster                                                            |
| regex_dna                | 131 ms                                                          | 122 ms: 1.07x faster                                                            |
| scimark_lu               | 89.8 ms                                                         | 84.2 ms: 1.07x faster                                                           |
| sympy_str                | 229 ms                                                          | 215 ms: 1.06x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 66.9 ms: 1.06x faster                                                           |
| regex_compile            | 117 ms                                                          | 110 ms: 1.06x faster                                                            |
| unpickle_list            | 2.98 us                                                         | 2.83 us: 1.06x faster                                                           |
| sympy_expand             | 391 ms                                                          | 371 ms: 1.05x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.74 sec: 1.05x faster                                                          |
| 2to3                     | 265 ms                                                          | 254 ms: 1.05x faster                                                            |
| scimark_monte_carlo      | 61.9 ms                                                         | 59.4 ms: 1.04x faster                                                           |
| sympy_integrate          | 16.6 ms                                                         | 16.1 ms: 1.03x faster                                                           |
| chameleon                | 6.42 ms                                                         | 6.22 ms: 1.03x faster                                                           |
| hexiom                   | 6.13 ms                                                         | 5.98 ms: 1.03x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                          |
| deepcopy                 | 310 us                                                          | 305 us: 1.02x faster                                                            |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.20 ms: 1.01x faster                                                           |
| sqlglot_normalize        | 230 ms                                                          | 228 ms: 1.01x faster                                                            |
| pickle_list              | 3.22 us                                                         | 3.19 us: 1.01x faster                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| sqlglot_optimize         | 44.7 ms                                                         | 44.9 ms: 1.00x slower                                                           |
| fannkuch                 | 317 ms                                                          | 319 ms: 1.01x slower                                                            |
| deepcopy_reduce          | 2.68 us                                                         | 2.71 us: 1.01x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 83.1 ms: 1.02x slower                                                           |
| pickle                   | 7.83 us                                                         | 8.01 us: 1.02x slower                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 63.2 ms: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.1 us: 1.03x slower                                                           |
| python_startup           | 22.9 ms                                                         | 23.7 ms: 1.04x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.4 ms: 1.04x slower                                                           |
| genshi_xml               | 46.6 ms                                                         | 48.4 ms: 1.04x slower                                                           |
| nqueens                  | 87.1 ms                                                         | 90.8 ms: 1.04x slower                                                           |
| meteor_contest           | 80.0 ms                                                         | 83.5 ms: 1.04x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 733 us: 1.06x slower                                                            |
| genshi_text              | 21.0 ms                                                         | 22.5 ms: 1.07x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 71.8 ms: 1.08x slower                                                           |
| logging_format           | 7.91 us                                                         | 8.58 us: 1.08x slower                                                           |
| scimark_fft              | 216 ms                                                          | 236 ms: 1.09x slower                                                            |
| logging_simple           | 7.29 us                                                         | 7.98 us: 1.10x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 20.1 us: 1.10x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.51 sec: 1.10x slower                                                          |
| python_startup_no_site   | 18.1 ms                                                         | 20.1 ms: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                           |
| pprint_safe_repr         | 658 ms                                                          | 736 ms: 1.12x slower                                                            |
| regex_effbot             | 1.66 ms                                                         | 1.91 ms: 1.15x slower                                                           |
| async_generators         | 241 ms                                                          | 291 ms: 1.21x slower                                                            |
| nbody                    | 79.1 ms                                                         | 97.3 ms: 1.23x slower                                                           |
| telco                    | 4.83 ms                                                         | 6.42 ms: 1.33x slower                                                           |
| coverage                 | 46.6 ms                                                         | 504 ms: 10.82x slower                                                           |
| thrift                   | 902 us                                                          | 10.6 ms: 11.77x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.07x faster                                                                    |
Ignored benchmarks (9) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240414-3.13.0a6+-a74f117-JIT/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown