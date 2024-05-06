# Results vs. 3.10.4

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-x86
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.05x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 257 ms: 1.03x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.17 ms: 1.04x faster                                                           |
| docutils       | 1.95 sec                                                        | 1.93 sec: 1.01x faster                                                          |
| html5lib       | 52.1 ms                                                         | 46.5 ms: 1.12x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.1 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 472 ms: 1.95x faster                                                            |
| async_tree_io           | 940 ms                                                          | 547 ms: 1.72x faster                                                            |
| async_tree_none         | 394 ms                                                          | 232 ms: 1.70x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 286 ms: 1.63x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.75x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 199 ms: 2.52x faster                                                            |
| float          | 69.6 ms                                                         | 53.6 ms: 1.30x faster                                                           |
| nbody          | 79.1 ms                                                         | 95.8 ms: 1.21x slower                                                           |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 120 ms: 1.09x faster                                                            |
| regex_compile  | 117 ms                                                          | 114 ms: 1.03x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.92 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.93 ms: 1.42x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 220 us: 1.27x faster                                                            |
| json_loads           | 22.4 us                                                         | 19.9 us: 1.12x faster                                                           |
| xml_etree_parse      | 120 ms                                                          | 107 ms: 1.12x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.73 sec: 1.11x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 43.7 ms: 1.10x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 180 us: 1.06x faster                                                            |
| unpickle_list        | 2.98 us                                                         | 2.85 us: 1.05x faster                                                           |
| pickle_list          | 3.22 us                                                         | 3.25 us: 1.01x slower                                                           |
| xml_etree_generate   | 61.6 ms                                                         | 62.4 ms: 1.01x slower                                                           |
| pickle               | 7.83 us                                                         | 7.98 us: 1.02x slower                                                           |
| unpickle             | 9.82 us                                                         | 10.0 us: 1.02x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 21.9 ms: 1.22x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.10 ms: 1.28x faster                                                           |
| django_template | 36.0 ms                                                         | 33.4 ms: 1.08x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 21.2 ms: 1.01x slower                                                           |
| genshi_xml      | 46.6 ms                                                         | 48.6 ms: 1.04x slower                                                           |
| Geometric mean  | (ref)                                                           | 1.07x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 96.5 us: 4.10x faster                                                           |
| pidigits                 | 502 ms                                                          | 199 ms: 2.52x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 472 ms: 1.95x faster                                                            |
| pylint                   | 384 ms                                                          | 222 ms: 1.73x faster                                                            |
| async_tree_io            | 940 ms                                                          | 547 ms: 1.72x faster                                                            |
| async_tree_none          | 394 ms                                                          | 232 ms: 1.70x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 286 ms: 1.63x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 60.3 ns: 1.62x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.62 ms: 1.54x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.93 ms: 1.42x faster                                                           |
| generators               | 31.6 ms                                                         | 23.1 ms: 1.36x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 1.01 ms: 1.32x faster                                                           |
| crypto_pyaes             | 81.3 ms                                                         | 61.8 ms: 1.31x faster                                                           |
| float                    | 69.6 ms                                                         | 53.6 ms: 1.30x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.10 ms: 1.28x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 220 us: 1.27x faster                                                            |
| sqlglot_transpile        | 1.58 ms                                                         | 1.26 ms: 1.25x faster                                                           |
| richards_super           | 49.9 ms                                                         | 40.2 ms: 1.24x faster                                                           |
| asyncio_tcp              | 744 ms                                                          | 604 ms: 1.23x faster                                                            |
| tornado_http             | 118 ms                                                          | 96.1 ms: 1.22x faster                                                           |
| coroutines               | 17.9 ms                                                         | 14.7 ms: 1.22x faster                                                           |
| pycparser                | 1.04 sec                                                        | 872 ms: 1.19x faster                                                            |
| go                       | 146 ms                                                          | 123 ms: 1.18x faster                                                            |
| chaos                    | 74.4 ms                                                         | 63.1 ms: 1.18x faster                                                           |
| sqlite_synth             | 2.29 us                                                         | 1.94 us: 1.18x faster                                                           |
| scimark_sor              | 115 ms                                                          | 100.0 ms: 1.15x faster                                                          |
| pyflate                  | 422 ms                                                          | 370 ms: 1.14x faster                                                            |
| comprehensions           | 17.7 us                                                         | 15.6 us: 1.14x faster                                                           |
| richards                 | 40.3 ms                                                         | 35.6 ms: 1.13x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 71.2 ms: 1.13x faster                                                           |
| deepcopy_memo            | 29.6 us                                                         | 26.3 us: 1.12x faster                                                           |
| json_loads               | 22.4 us                                                         | 19.9 us: 1.12x faster                                                           |
| xml_etree_parse          | 120 ms                                                          | 107 ms: 1.12x faster                                                            |
| html5lib                 | 52.1 ms                                                         | 46.5 ms: 1.12x faster                                                           |
| sympy_sum                | 122 ms                                                          | 110 ms: 1.11x faster                                                            |
| raytrace                 | 303 ms                                                          | 273 ms: 1.11x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 1.01 ms: 1.11x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.73 sec: 1.11x faster                                                          |
| xml_etree_process        | 48.1 ms                                                         | 43.7 ms: 1.10x faster                                                           |
| regex_dna                | 131 ms                                                          | 120 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| django_template          | 36.0 ms                                                         | 33.4 ms: 1.08x faster                                                           |
| json                     | 4.76 ms                                                         | 4.45 ms: 1.07x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 180 us: 1.06x faster                                                            |
| sympy_str                | 229 ms                                                          | 218 ms: 1.05x faster                                                            |
| unpickle_list            | 2.98 us                                                         | 2.85 us: 1.05x faster                                                           |
| chameleon                | 6.42 ms                                                         | 6.17 ms: 1.04x faster                                                           |
| deepcopy                 | 310 us                                                          | 300 us: 1.03x faster                                                            |
| 2to3                     | 265 ms                                                          | 257 ms: 1.03x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.78 sec: 1.03x faster                                                          |
| regex_compile            | 117 ms                                                          | 114 ms: 1.03x faster                                                            |
| sympy_expand             | 391 ms                                                          | 381 ms: 1.02x faster                                                            |
| sympy_integrate          | 16.6 ms                                                         | 16.4 ms: 1.02x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.64 us: 1.02x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.19 ms: 1.02x faster                                                           |
| docutils                 | 1.95 sec                                                        | 1.93 sec: 1.01x faster                                                          |
| scimark_monte_carlo      | 61.9 ms                                                         | 61.5 ms: 1.01x faster                                                           |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| fannkuch                 | 317 ms                                                          | 319 ms: 1.01x slower                                                            |
| pickle_list              | 3.22 us                                                         | 3.25 us: 1.01x slower                                                           |
| genshi_text              | 21.0 ms                                                         | 21.2 ms: 1.01x slower                                                           |
| xml_etree_generate       | 61.6 ms                                                         | 62.4 ms: 1.01x slower                                                           |
| pickle                   | 7.83 us                                                         | 7.98 us: 1.02x slower                                                           |
| unpickle                 | 9.82 us                                                         | 10.0 us: 1.02x slower                                                           |
| hexiom                   | 6.13 ms                                                         | 6.28 ms: 1.02x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| scimark_lu               | 89.8 ms                                                         | 93.0 ms: 1.04x slower                                                           |
| sqlglot_optimize         | 44.7 ms                                                         | 46.5 ms: 1.04x slower                                                           |
| genshi_xml               | 46.6 ms                                                         | 48.6 ms: 1.04x slower                                                           |
| sqlglot_normalize        | 230 ms                                                          | 241 ms: 1.05x slower                                                            |
| meteor_contest           | 80.0 ms                                                         | 83.9 ms: 1.05x slower                                                           |
| nqueens                  | 87.1 ms                                                         | 92.1 ms: 1.06x slower                                                           |
| python_startup           | 22.9 ms                                                         | 24.3 ms: 1.06x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 86.3 ms: 1.06x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 737 us: 1.06x slower                                                            |
| pickle_dict              | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 72.2 ms: 1.09x slower                                                           |
| scimark_fft              | 216 ms                                                          | 237 ms: 1.10x slower                                                            |
| pprint_pformat           | 1.37 sec                                                        | 1.51 sec: 1.10x slower                                                          |
| logging_format           | 7.91 us                                                         | 8.81 us: 1.11x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.12x slower                                                           |
| pprint_safe_repr         | 658 ms                                                          | 742 ms: 1.13x slower                                                            |
| logging_simple           | 7.29 us                                                         | 8.24 us: 1.13x slower                                                           |
| regex_effbot             | 1.66 ms                                                         | 1.92 ms: 1.16x slower                                                           |
| unpack_sequence          | 40.0 ns                                                         | 46.6 ns: 1.16x slower                                                           |
| async_generators         | 241 ms                                                          | 285 ms: 1.18x slower                                                            |
| nbody                    | 79.1 ms                                                         | 95.8 ms: 1.21x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 21.9 ms: 1.22x slower                                                           |
| telco                    | 4.83 ms                                                         | 6.50 ms: 1.35x slower                                                           |
| coverage                 | 46.6 ms                                                         | 487 ms: 10.46x slower                                                           |
| thrift                   | 902 us                                                          | 10.9 ms: 12.12x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.05x faster                                                                    |
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-05e0b67-JIT/bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown