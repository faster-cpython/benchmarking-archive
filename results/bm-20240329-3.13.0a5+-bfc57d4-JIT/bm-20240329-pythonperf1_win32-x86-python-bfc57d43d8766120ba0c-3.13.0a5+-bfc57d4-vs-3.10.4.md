# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.05x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 255 ms: 1.04x faster                                                            |
| chameleon      | 6.42 ms                                                         | 6.13 ms: 1.05x faster                                                           |
| html5lib       | 52.1 ms                                                         | 46.0 ms: 1.13x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.4 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 481 ms: 1.92x faster                                                            |
| async_tree_io           | 940 ms                                                          | 544 ms: 1.73x faster                                                            |
| async_tree_none         | 394 ms                                                          | 231 ms: 1.71x faster                                                            |
| async_tree_memoization  | 467 ms                                                          | 282 ms: 1.66x faster                                                            |
| Geometric mean          | (ref)                                                           | 1.75x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| float          | 69.6 ms                                                         | 53.3 ms: 1.31x faster                                                           |
| nbody          | 79.1 ms                                                         | 98.8 ms: 1.25x slower                                                           |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 125 ms: 1.05x faster                                                            |
| regex_compile  | 117 ms                                                          | 113 ms: 1.03x faster                                                            |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| regex_effbot   | 1.66 ms                                                         | 1.93 ms: 1.16x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.78 ms: 1.45x faster                                                           |
| pickle_pure_python   | 280 us                                                          | 227 us: 1.23x faster                                                            |
| tomli_loads          | 1.91 sec                                                        | 1.72 sec: 1.11x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 43.4 ms: 1.11x faster                                                           |
| unpickle_pure_python | 189 us                                                          | 171 us: 1.11x faster                                                            |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| json_loads           | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| unpickle_list        | 2.98 us                                                         | 2.80 us: 1.06x faster                                                           |
| unpickle             | 9.82 us                                                         | 9.88 us: 1.01x slower                                                           |
| pickle_list          | 3.22 us                                                         | 3.25 us: 1.01x slower                                                           |
| pickle               | 7.83 us                                                         | 8.18 us: 1.04x slower                                                           |
| pickle_dict          | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                           |
| python_startup_no_site | 18.1 ms                                                         | 21.9 ms: 1.21x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.24 ms: 1.26x faster                                                           |
| django_template | 36.0 ms                                                         | 33.2 ms: 1.09x faster                                                           |
| genshi_text     | 21.0 ms                                                         | 20.1 ms: 1.04x faster                                                           |
| genshi_xml      | 46.6 ms                                                         | 47.7 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                           | 1.09x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 98.2 us: 4.03x faster                                                           |
| pidigits                 | 502 ms                                                          | 198 ms: 2.54x faster                                                            |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 481 ms: 1.92x faster                                                            |
| async_tree_io            | 940 ms                                                          | 544 ms: 1.73x faster                                                            |
| pylint                   | 384 ms                                                          | 223 ms: 1.72x faster                                                            |
| async_tree_none          | 394 ms                                                          | 231 ms: 1.71x faster                                                            |
| async_tree_memoization   | 467 ms                                                          | 282 ms: 1.66x faster                                                            |
| logging_silent           | 97.9 ns                                                         | 60.7 ns: 1.61x faster                                                           |
| deltablue                | 4.04 ms                                                         | 2.59 ms: 1.56x faster                                                           |
| json_dumps               | 9.82 ms                                                         | 6.78 ms: 1.45x faster                                                           |
| generators               | 31.6 ms                                                         | 23.0 ms: 1.37x faster                                                           |
| sqlglot_parse            | 1.33 ms                                                         | 996 us: 1.33x faster                                                            |
| crypto_pyaes             | 81.3 ms                                                         | 62.0 ms: 1.31x faster                                                           |
| float                    | 69.6 ms                                                         | 53.3 ms: 1.31x faster                                                           |
| mako                     | 9.10 ms                                                         | 7.24 ms: 1.26x faster                                                           |
| sqlglot_transpile        | 1.58 ms                                                         | 1.26 ms: 1.25x faster                                                           |
| pickle_pure_python       | 280 us                                                          | 227 us: 1.23x faster                                                            |
| richards_super           | 49.9 ms                                                         | 40.6 ms: 1.23x faster                                                           |
| tornado_http             | 118 ms                                                          | 96.4 ms: 1.22x faster                                                           |
| coroutines               | 17.9 ms                                                         | 14.8 ms: 1.21x faster                                                           |
| chaos                    | 74.4 ms                                                         | 61.8 ms: 1.21x faster                                                           |
| pycparser                | 1.04 sec                                                        | 871 ms: 1.20x faster                                                            |
| go                       | 146 ms                                                          | 122 ms: 1.19x faster                                                            |
| asyncio_tcp              | 744 ms                                                          | 632 ms: 1.18x faster                                                            |
| sqlite_synth             | 2.29 us                                                         | 1.95 us: 1.18x faster                                                           |
| raytrace                 | 303 ms                                                          | 260 ms: 1.16x faster                                                            |
| scimark_sor              | 115 ms                                                          | 99.1 ms: 1.16x faster                                                           |
| comprehensions           | 17.7 us                                                         | 15.3 us: 1.16x faster                                                           |
| pyflate                  | 422 ms                                                          | 369 ms: 1.14x faster                                                            |
| html5lib                 | 52.1 ms                                                         | 46.0 ms: 1.13x faster                                                           |
| spectral_norm            | 80.2 ms                                                         | 71.3 ms: 1.12x faster                                                           |
| sympy_sum                | 122 ms                                                          | 109 ms: 1.12x faster                                                            |
| deepcopy_memo            | 29.6 us                                                         | 26.5 us: 1.12x faster                                                           |
| richards                 | 40.3 ms                                                         | 36.1 ms: 1.11x faster                                                           |
| tomli_loads              | 1.91 sec                                                        | 1.72 sec: 1.11x faster                                                          |
| xml_etree_process        | 48.1 ms                                                         | 43.4 ms: 1.11x faster                                                           |
| unpickle_pure_python     | 189 us                                                          | 171 us: 1.11x faster                                                            |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.11x faster                                                            |
| bench_thread_pool        | 1.12 ms                                                         | 1.01 ms: 1.11x faster                                                           |
| json_loads               | 22.4 us                                                         | 20.3 us: 1.10x faster                                                           |
| django_template          | 36.0 ms                                                         | 33.2 ms: 1.09x faster                                                           |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                           |
| unpickle_list            | 2.98 us                                                         | 2.80 us: 1.06x faster                                                           |
| sympy_str                | 229 ms                                                          | 217 ms: 1.06x faster                                                            |
| deepcopy                 | 310 us                                                          | 295 us: 1.05x faster                                                            |
| chameleon                | 6.42 ms                                                         | 6.13 ms: 1.05x faster                                                           |
| regex_dna                | 131 ms                                                          | 125 ms: 1.05x faster                                                            |
| genshi_text              | 21.0 ms                                                         | 20.1 ms: 1.04x faster                                                           |
| 2to3                     | 265 ms                                                          | 255 ms: 1.04x faster                                                            |
| sympy_expand             | 391 ms                                                          | 378 ms: 1.03x faster                                                            |
| regex_compile            | 117 ms                                                          | 113 ms: 1.03x faster                                                            |
| mdp                      | 1.83 sec                                                        | 1.78 sec: 1.03x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 16.3 ms: 1.02x faster                                                           |
| deepcopy_reduce          | 2.68 us                                                         | 2.63 us: 1.02x faster                                                           |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.18 ms: 1.02x faster                                                           |
| fannkuch                 | 317 ms                                                          | 313 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| unpickle                 | 9.82 us                                                         | 9.88 us: 1.01x slower                                                           |
| scimark_monte_carlo      | 61.9 ms                                                         | 62.4 ms: 1.01x slower                                                           |
| pickle_list              | 3.22 us                                                         | 3.25 us: 1.01x slower                                                           |
| meteor_contest           | 80.0 ms                                                         | 81.2 ms: 1.01x slower                                                           |
| hexiom                   | 6.13 ms                                                         | 6.24 ms: 1.02x slower                                                           |
| genshi_xml               | 46.6 ms                                                         | 47.7 ms: 1.02x slower                                                           |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                           |
| sqlglot_normalize        | 230 ms                                                          | 238 ms: 1.03x slower                                                            |
| sqlglot_optimize         | 44.7 ms                                                         | 46.3 ms: 1.03x slower                                                           |
| pickle                   | 7.83 us                                                         | 8.18 us: 1.04x slower                                                           |
| pathlib                  | 81.2 ms                                                         | 86.0 ms: 1.06x slower                                                           |
| python_startup           | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                           |
| create_gc_cycles         | 694 us                                                          | 740 us: 1.07x slower                                                            |
| nqueens                  | 87.1 ms                                                         | 93.0 ms: 1.07x slower                                                           |
| scimark_lu               | 89.8 ms                                                         | 96.7 ms: 1.08x slower                                                           |
| pickle_dict              | 18.2 us                                                         | 19.9 us: 1.09x slower                                                           |
| bench_mp_pool            | 66.4 ms                                                         | 72.3 ms: 1.09x slower                                                           |
| pprint_pformat           | 1.37 sec                                                        | 1.49 sec: 1.09x slower                                                          |
| unpack_sequence          | 40.0 ns                                                         | 44.0 ns: 1.10x slower                                                           |
| gc_traversal             | 1.28 ms                                                         | 1.42 ms: 1.11x slower                                                           |
| pprint_safe_repr         | 658 ms                                                          | 741 ms: 1.13x slower                                                            |
| logging_format           | 7.91 us                                                         | 9.05 us: 1.14x slower                                                           |
| scimark_fft              | 216 ms                                                          | 247 ms: 1.14x slower                                                            |
| regex_effbot             | 1.66 ms                                                         | 1.93 ms: 1.16x slower                                                           |
| logging_simple           | 7.29 us                                                         | 8.50 us: 1.17x slower                                                           |
| python_startup_no_site   | 18.1 ms                                                         | 21.9 ms: 1.21x slower                                                           |
| async_generators         | 241 ms                                                          | 295 ms: 1.22x slower                                                            |
| nbody                    | 79.1 ms                                                         | 98.8 ms: 1.25x slower                                                           |
| telco                    | 4.83 ms                                                         | 6.33 ms: 1.31x slower                                                           |
| coverage                 | 46.6 ms                                                         | 482 ms: 10.35x slower                                                           |
| thrift                   | 902 us                                                          | 11.0 ms: 12.16x slower                                                          |
| Geometric mean           | (ref)                                                           | 1.05x faster                                                                    |

Benchmark hidden because not significant (3): json, docutils, xml_etree_generate
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown