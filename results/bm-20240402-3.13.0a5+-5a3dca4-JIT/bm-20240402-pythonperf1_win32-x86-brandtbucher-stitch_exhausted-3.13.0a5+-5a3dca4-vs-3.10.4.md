# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.04x faster
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| chameleon      | 6.42 ms                                                         | 6.24 ms: 1.03x faster                                                             |
| docutils       | 1.95 sec                                                        | 1.98 sec: 1.01x slower                                                            |
| html5lib       | 52.1 ms                                                         | 45.7 ms: 1.14x faster                                                             |
| tornado_http   | 118 ms                                                          | 97.6 ms: 1.20x faster                                                             |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                      |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 480 ms: 1.92x faster                                                              |
| async_tree_io           | 940 ms                                                          | 553 ms: 1.70x faster                                                              |
| async_tree_none         | 394 ms                                                          | 237 ms: 1.66x faster                                                              |
| async_tree_memoization  | 467 ms                                                          | 289 ms: 1.62x faster                                                              |
| Geometric mean          | (ref)                                                           | 1.72x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 198 ms: 2.54x faster                                                              |
| float          | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                             |
| nbody          | 79.1 ms                                                         | 98.7 ms: 1.25x slower                                                             |
| Geometric mean | (ref)                                                           | 1.38x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 122 ms: 1.07x faster                                                              |
| regex_compile  | 117 ms                                                          | 115 ms: 1.01x faster                                                              |
| regex_v8       | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                             |
| regex_effbot   | 1.66 ms                                                         | 1.89 ms: 1.14x slower                                                             |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.91 ms: 1.42x faster                                                             |
| pickle_pure_python   | 280 us                                                          | 224 us: 1.25x faster                                                              |
| json_loads           | 22.4 us                                                         | 19.8 us: 1.13x faster                                                             |
| tomli_loads          | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 110 ms: 1.09x faster                                                              |
| unpickle_list        | 2.98 us                                                         | 2.76 us: 1.08x faster                                                             |
| xml_etree_iterparse  | 70.8 ms                                                         | 66.6 ms: 1.06x faster                                                             |
| unpickle_pure_python | 189 us                                                          | 178 us: 1.06x faster                                                              |
| xml_etree_process    | 48.1 ms                                                         | 46.0 ms: 1.05x faster                                                             |
| unpickle             | 9.82 us                                                         | 9.89 us: 1.01x slower                                                             |
| pickle_list          | 3.22 us                                                         | 3.26 us: 1.01x slower                                                             |
| xml_etree_generate   | 61.6 ms                                                         | 64.4 ms: 1.04x slower                                                             |
| pickle               | 7.83 us                                                         | 8.24 us: 1.05x slower                                                             |
| pickle_dict          | 18.2 us                                                         | 20.1 us: 1.10x slower                                                             |
| Geometric mean       | (ref)                                                           | 1.07x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                             |
| python_startup_no_site | 18.1 ms                                                         | 22.0 ms: 1.22x slower                                                             |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.18 ms: 1.27x faster                                                             |
| django_template | 36.0 ms                                                         | 35.3 ms: 1.02x faster                                                             |
| genshi_xml      | 46.6 ms                                                         | 49.9 ms: 1.07x slower                                                             |
| genshi_text     | 21.0 ms                                                         | 23.3 ms: 1.11x slower                                                             |
| Geometric mean  | (ref)                                                           | 1.02x faster                                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 101 us: 3.91x faster                                                              |
| pidigits                 | 502 ms                                                          | 198 ms: 2.54x faster                                                              |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 480 ms: 1.92x faster                                                              |
| async_tree_io            | 940 ms                                                          | 553 ms: 1.70x faster                                                              |
| pylint                   | 384 ms                                                          | 228 ms: 1.68x faster                                                              |
| async_tree_none          | 394 ms                                                          | 237 ms: 1.66x faster                                                              |
| logging_silent           | 97.9 ns                                                         | 59.9 ns: 1.63x faster                                                             |
| async_tree_memoization   | 467 ms                                                          | 289 ms: 1.62x faster                                                              |
| deltablue                | 4.04 ms                                                         | 2.61 ms: 1.54x faster                                                             |
| json_dumps               | 9.82 ms                                                         | 6.91 ms: 1.42x faster                                                             |
| generators               | 31.6 ms                                                         | 22.4 ms: 1.41x faster                                                             |
| sqlglot_parse            | 1.33 ms                                                         | 1.00 ms: 1.32x faster                                                             |
| float                    | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                             |
| crypto_pyaes             | 81.3 ms                                                         | 62.7 ms: 1.30x faster                                                             |
| mako                     | 9.10 ms                                                         | 7.18 ms: 1.27x faster                                                             |
| sqlglot_transpile        | 1.58 ms                                                         | 1.26 ms: 1.26x faster                                                             |
| pickle_pure_python       | 280 us                                                          | 224 us: 1.25x faster                                                              |
| richards_super           | 49.9 ms                                                         | 40.4 ms: 1.24x faster                                                             |
| coroutines               | 17.9 ms                                                         | 14.5 ms: 1.23x faster                                                             |
| asyncio_tcp              | 744 ms                                                          | 608 ms: 1.22x faster                                                              |
| tornado_http             | 118 ms                                                          | 97.6 ms: 1.20x faster                                                             |
| pycparser                | 1.04 sec                                                        | 869 ms: 1.20x faster                                                              |
| chaos                    | 74.4 ms                                                         | 62.5 ms: 1.19x faster                                                             |
| sqlite_synth             | 2.29 us                                                         | 1.94 us: 1.18x faster                                                             |
| scimark_sor              | 115 ms                                                          | 97.9 ms: 1.18x faster                                                             |
| raytrace                 | 303 ms                                                          | 264 ms: 1.15x faster                                                              |
| json                     | 4.76 ms                                                         | 4.16 ms: 1.14x faster                                                             |
| html5lib                 | 52.1 ms                                                         | 45.7 ms: 1.14x faster                                                             |
| spectral_norm            | 80.2 ms                                                         | 70.5 ms: 1.14x faster                                                             |
| pyflate                  | 422 ms                                                          | 372 ms: 1.13x faster                                                              |
| json_loads               | 22.4 us                                                         | 19.8 us: 1.13x faster                                                             |
| go                       | 146 ms                                                          | 130 ms: 1.12x faster                                                              |
| richards                 | 40.3 ms                                                         | 36.0 ms: 1.12x faster                                                             |
| deepcopy_memo            | 29.6 us                                                         | 26.6 us: 1.11x faster                                                             |
| sympy_sum                | 122 ms                                                          | 112 ms: 1.09x faster                                                              |
| tomli_loads              | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                            |
| xml_etree_parse          | 120 ms                                                          | 110 ms: 1.09x faster                                                              |
| bench_thread_pool        | 1.12 ms                                                         | 1.03 ms: 1.09x faster                                                             |
| comprehensions           | 17.7 us                                                         | 16.3 us: 1.09x faster                                                             |
| unpickle_list            | 2.98 us                                                         | 2.76 us: 1.08x faster                                                             |
| regex_dna                | 131 ms                                                          | 122 ms: 1.07x faster                                                              |
| xml_etree_iterparse      | 70.8 ms                                                         | 66.6 ms: 1.06x faster                                                             |
| unpickle_pure_python     | 189 us                                                          | 178 us: 1.06x faster                                                              |
| xml_etree_process        | 48.1 ms                                                         | 46.0 ms: 1.05x faster                                                             |
| deepcopy_reduce          | 2.68 us                                                         | 2.57 us: 1.04x faster                                                             |
| mdp                      | 1.83 sec                                                        | 1.76 sec: 1.04x faster                                                            |
| sympy_str                | 229 ms                                                          | 222 ms: 1.03x faster                                                              |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.14 ms: 1.03x faster                                                             |
| chameleon                | 6.42 ms                                                         | 6.24 ms: 1.03x faster                                                             |
| deepcopy                 | 310 us                                                          | 302 us: 1.03x faster                                                              |
| django_template          | 36.0 ms                                                         | 35.3 ms: 1.02x faster                                                             |
| scimark_lu               | 89.8 ms                                                         | 88.2 ms: 1.02x faster                                                             |
| regex_compile            | 117 ms                                                          | 115 ms: 1.01x faster                                                              |
| sympy_expand             | 391 ms                                                          | 386 ms: 1.01x faster                                                              |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                            |
| unpickle                 | 9.82 us                                                         | 9.89 us: 1.01x slower                                                             |
| pickle_list              | 3.22 us                                                         | 3.26 us: 1.01x slower                                                             |
| sympy_integrate          | 16.6 ms                                                         | 16.9 ms: 1.01x slower                                                             |
| docutils                 | 1.95 sec                                                        | 1.98 sec: 1.01x slower                                                            |
| fannkuch                 | 317 ms                                                          | 324 ms: 1.02x slower                                                              |
| regex_v8                 | 15.8 ms                                                         | 16.3 ms: 1.03x slower                                                             |
| xml_etree_generate       | 61.6 ms                                                         | 64.4 ms: 1.04x slower                                                             |
| pickle                   | 7.83 us                                                         | 8.24 us: 1.05x slower                                                             |
| python_startup           | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                             |
| sqlglot_optimize         | 44.7 ms                                                         | 47.5 ms: 1.06x slower                                                             |
| create_gc_cycles         | 694 us                                                          | 737 us: 1.06x slower                                                              |
| pathlib                  | 81.2 ms                                                         | 86.4 ms: 1.06x slower                                                             |
| genshi_xml               | 46.6 ms                                                         | 49.9 ms: 1.07x slower                                                             |
| sqlglot_normalize        | 230 ms                                                          | 247 ms: 1.07x slower                                                              |
| hexiom                   | 6.13 ms                                                         | 6.65 ms: 1.08x slower                                                             |
| pprint_pformat           | 1.37 sec                                                        | 1.48 sec: 1.08x slower                                                            |
| meteor_contest           | 80.0 ms                                                         | 87.2 ms: 1.09x slower                                                             |
| bench_mp_pool            | 66.4 ms                                                         | 72.7 ms: 1.10x slower                                                             |
| pickle_dict              | 18.2 us                                                         | 20.1 us: 1.10x slower                                                             |
| nqueens                  | 87.1 ms                                                         | 96.7 ms: 1.11x slower                                                             |
| genshi_text              | 21.0 ms                                                         | 23.3 ms: 1.11x slower                                                             |
| pprint_safe_repr         | 658 ms                                                          | 732 ms: 1.11x slower                                                              |
| scimark_fft              | 216 ms                                                          | 240 ms: 1.11x slower                                                              |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.11x slower                                                             |
| unpack_sequence          | 40.0 ns                                                         | 45.5 ns: 1.14x slower                                                             |
| regex_effbot             | 1.66 ms                                                         | 1.89 ms: 1.14x slower                                                             |
| logging_format           | 7.91 us                                                         | 9.18 us: 1.16x slower                                                             |
| logging_simple           | 7.29 us                                                         | 8.60 us: 1.18x slower                                                             |
| python_startup_no_site   | 18.1 ms                                                         | 22.0 ms: 1.22x slower                                                             |
| async_generators         | 241 ms                                                          | 294 ms: 1.22x slower                                                              |
| nbody                    | 79.1 ms                                                         | 98.7 ms: 1.25x slower                                                             |
| telco                    | 4.83 ms                                                         | 6.32 ms: 1.31x slower                                                             |
| coverage                 | 46.6 ms                                                         | 490 ms: 10.53x slower                                                             |
| thrift                   | 902 us                                                          | 11.0 ms: 12.17x slower                                                            |
| Geometric mean           | (ref)                                                           | 1.04x faster                                                                      |

Benchmark hidden because not significant (2): 2to3, scimark_monte_carlo
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.57% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown