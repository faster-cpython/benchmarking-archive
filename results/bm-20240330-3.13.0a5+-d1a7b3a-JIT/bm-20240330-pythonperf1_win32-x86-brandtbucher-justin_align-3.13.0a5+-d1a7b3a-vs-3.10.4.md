# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.06x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 254 ms: 1.04x faster                                                          |
| chameleon      | 6.42 ms                                                         | 6.36 ms: 1.01x faster                                                         |
| docutils       | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                        |
| html5lib       | 52.1 ms                                                         | 45.4 ms: 1.15x faster                                                         |
| tornado_http   | 118 ms                                                          | 96.1 ms: 1.22x faster                                                         |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 474 ms: 1.95x faster                                                          |
| async_tree_io           | 940 ms                                                          | 545 ms: 1.73x faster                                                          |
| async_tree_none         | 394 ms                                                          | 231 ms: 1.70x faster                                                          |
| async_tree_memoization  | 467 ms                                                          | 284 ms: 1.64x faster                                                          |
| Geometric mean          | (ref)                                                           | 1.75x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 197 ms: 2.56x faster                                                          |
| float          | 69.6 ms                                                         | 54.0 ms: 1.29x faster                                                         |
| nbody          | 79.1 ms                                                         | 96.5 ms: 1.22x slower                                                         |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 121 ms: 1.07x faster                                                          |
| regex_compile  | 117 ms                                                          | 113 ms: 1.03x faster                                                          |
| regex_v8       | 15.8 ms                                                         | 16.3 ms: 1.04x slower                                                         |
| regex_effbot   | 1.66 ms                                                         | 1.90 ms: 1.15x slower                                                         |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.93 ms: 1.42x faster                                                         |
| pickle_pure_python   | 280 us                                                          | 223 us: 1.26x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 107 ms: 1.12x faster                                                          |
| unpickle_pure_python | 189 us                                                          | 171 us: 1.11x faster                                                          |
| json_loads           | 22.4 us                                                         | 20.2 us: 1.11x faster                                                         |
| tomli_loads          | 1.91 sec                                                        | 1.74 sec: 1.10x faster                                                        |
| xml_etree_process    | 48.1 ms                                                         | 43.8 ms: 1.10x faster                                                         |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                         |
| unpickle_list        | 2.98 us                                                         | 2.80 us: 1.07x faster                                                         |
| pickle_list          | 3.22 us                                                         | 3.23 us: 1.00x slower                                                         |
| xml_etree_generate   | 61.6 ms                                                         | 62.0 ms: 1.01x slower                                                         |
| pickle               | 7.83 us                                                         | 7.90 us: 1.01x slower                                                         |
| unpickle             | 9.82 us                                                         | 10.0 us: 1.02x slower                                                         |
| pickle_dict          | 18.2 us                                                         | 19.8 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.08x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                         |
| python_startup_no_site | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.07 ms: 1.29x faster                                                         |
| django_template | 36.0 ms                                                         | 33.6 ms: 1.07x faster                                                         |
| genshi_text     | 21.0 ms                                                         | 20.7 ms: 1.01x faster                                                         |
| genshi_xml      | 46.6 ms                                                         | 48.8 ms: 1.05x slower                                                         |
| Geometric mean  | (ref)                                                           | 1.07x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 94.1 us: 4.21x faster                                                         |
| pidigits                 | 502 ms                                                          | 197 ms: 2.56x faster                                                          |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 474 ms: 1.95x faster                                                          |
| pylint                   | 384 ms                                                          | 221 ms: 1.74x faster                                                          |
| async_tree_io            | 940 ms                                                          | 545 ms: 1.73x faster                                                          |
| async_tree_none          | 394 ms                                                          | 231 ms: 1.70x faster                                                          |
| async_tree_memoization   | 467 ms                                                          | 284 ms: 1.64x faster                                                          |
| logging_silent           | 97.9 ns                                                         | 61.3 ns: 1.60x faster                                                         |
| deltablue                | 4.04 ms                                                         | 2.61 ms: 1.55x faster                                                         |
| json_dumps               | 9.82 ms                                                         | 6.93 ms: 1.42x faster                                                         |
| generators               | 31.6 ms                                                         | 23.1 ms: 1.36x faster                                                         |
| sqlglot_parse            | 1.33 ms                                                         | 1.00 ms: 1.33x faster                                                         |
| float                    | 69.6 ms                                                         | 54.0 ms: 1.29x faster                                                         |
| mako                     | 9.10 ms                                                         | 7.07 ms: 1.29x faster                                                         |
| crypto_pyaes             | 81.3 ms                                                         | 63.7 ms: 1.28x faster                                                         |
| sqlglot_transpile        | 1.58 ms                                                         | 1.25 ms: 1.26x faster                                                         |
| pickle_pure_python       | 280 us                                                          | 223 us: 1.26x faster                                                          |
| chaos                    | 74.4 ms                                                         | 60.7 ms: 1.23x faster                                                         |
| tornado_http             | 118 ms                                                          | 96.1 ms: 1.22x faster                                                         |
| richards_super           | 49.9 ms                                                         | 40.8 ms: 1.22x faster                                                         |
| pycparser                | 1.04 sec                                                        | 857 ms: 1.22x faster                                                          |
| coroutines               | 17.9 ms                                                         | 14.9 ms: 1.20x faster                                                         |
| sqlite_synth             | 2.29 us                                                         | 1.92 us: 1.20x faster                                                         |
| asyncio_tcp              | 744 ms                                                          | 627 ms: 1.19x faster                                                          |
| go                       | 146 ms                                                          | 123 ms: 1.19x faster                                                          |
| raytrace                 | 303 ms                                                          | 262 ms: 1.16x faster                                                          |
| pyflate                  | 422 ms                                                          | 365 ms: 1.16x faster                                                          |
| comprehensions           | 17.7 us                                                         | 15.4 us: 1.15x faster                                                         |
| scimark_sor              | 115 ms                                                          | 99.9 ms: 1.15x faster                                                         |
| html5lib                 | 52.1 ms                                                         | 45.4 ms: 1.15x faster                                                         |
| sympy_sum                | 122 ms                                                          | 108 ms: 1.13x faster                                                          |
| deepcopy_memo            | 29.6 us                                                         | 26.1 us: 1.13x faster                                                         |
| xml_etree_parse          | 120 ms                                                          | 107 ms: 1.12x faster                                                          |
| json                     | 4.76 ms                                                         | 4.26 ms: 1.12x faster                                                         |
| spectral_norm            | 80.2 ms                                                         | 72.1 ms: 1.11x faster                                                         |
| richards                 | 40.3 ms                                                         | 36.2 ms: 1.11x faster                                                         |
| unpickle_pure_python     | 189 us                                                          | 171 us: 1.11x faster                                                          |
| json_loads               | 22.4 us                                                         | 20.2 us: 1.11x faster                                                         |
| tomli_loads              | 1.91 sec                                                        | 1.74 sec: 1.10x faster                                                        |
| xml_etree_process        | 48.1 ms                                                         | 43.8 ms: 1.10x faster                                                         |
| bench_thread_pool        | 1.12 ms                                                         | 1.03 ms: 1.09x faster                                                         |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.4 ms: 1.08x faster                                                         |
| sympy_str                | 229 ms                                                          | 213 ms: 1.08x faster                                                          |
| regex_dna                | 131 ms                                                          | 121 ms: 1.07x faster                                                          |
| django_template          | 36.0 ms                                                         | 33.6 ms: 1.07x faster                                                         |
| deepcopy_reduce          | 2.68 us                                                         | 2.51 us: 1.07x faster                                                         |
| unpickle_list            | 2.98 us                                                         | 2.80 us: 1.07x faster                                                         |
| deepcopy                 | 310 us                                                          | 291 us: 1.06x faster                                                          |
| sympy_expand             | 391 ms                                                          | 371 ms: 1.05x faster                                                          |
| mdp                      | 1.83 sec                                                        | 1.74 sec: 1.05x faster                                                        |
| 2to3                     | 265 ms                                                          | 254 ms: 1.04x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 16.0 ms: 1.04x faster                                                         |
| regex_compile            | 117 ms                                                          | 113 ms: 1.03x faster                                                          |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.15 ms: 1.03x faster                                                         |
| docutils                 | 1.95 sec                                                        | 1.91 sec: 1.02x faster                                                        |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.7 sec: 1.01x faster                                                        |
| genshi_text              | 21.0 ms                                                         | 20.7 ms: 1.01x faster                                                         |
| chameleon                | 6.42 ms                                                         | 6.36 ms: 1.01x faster                                                         |
| pickle_list              | 3.22 us                                                         | 3.23 us: 1.00x slower                                                         |
| xml_etree_generate       | 61.6 ms                                                         | 62.0 ms: 1.01x slower                                                         |
| pickle                   | 7.83 us                                                         | 7.90 us: 1.01x slower                                                         |
| fannkuch                 | 317 ms                                                          | 323 ms: 1.02x slower                                                          |
| sqlglot_optimize         | 44.7 ms                                                         | 45.6 ms: 1.02x slower                                                         |
| unpickle                 | 9.82 us                                                         | 10.0 us: 1.02x slower                                                         |
| meteor_contest           | 80.0 ms                                                         | 82.0 ms: 1.03x slower                                                         |
| hexiom                   | 6.13 ms                                                         | 6.30 ms: 1.03x slower                                                         |
| regex_v8                 | 15.8 ms                                                         | 16.3 ms: 1.04x slower                                                         |
| sqlglot_normalize        | 230 ms                                                          | 241 ms: 1.05x slower                                                          |
| genshi_xml               | 46.6 ms                                                         | 48.8 ms: 1.05x slower                                                         |
| scimark_lu               | 89.8 ms                                                         | 94.8 ms: 1.06x slower                                                         |
| pathlib                  | 81.2 ms                                                         | 86.3 ms: 1.06x slower                                                         |
| create_gc_cycles         | 694 us                                                          | 738 us: 1.06x slower                                                          |
| python_startup           | 22.9 ms                                                         | 24.4 ms: 1.06x slower                                                         |
| nqueens                  | 87.1 ms                                                         | 93.5 ms: 1.07x slower                                                         |
| pickle_dict              | 18.2 us                                                         | 19.8 us: 1.09x slower                                                         |
| pprint_pformat           | 1.37 sec                                                        | 1.49 sec: 1.09x slower                                                        |
| bench_mp_pool            | 66.4 ms                                                         | 72.3 ms: 1.09x slower                                                         |
| scimark_fft              | 216 ms                                                          | 238 ms: 1.10x slower                                                          |
| gc_traversal             | 1.28 ms                                                         | 1.43 ms: 1.11x slower                                                         |
| pprint_safe_repr         | 658 ms                                                          | 735 ms: 1.12x slower                                                          |
| unpack_sequence          | 40.0 ns                                                         | 45.7 ns: 1.14x slower                                                         |
| regex_effbot             | 1.66 ms                                                         | 1.90 ms: 1.15x slower                                                         |
| logging_format           | 7.91 us                                                         | 9.11 us: 1.15x slower                                                         |
| logging_simple           | 7.29 us                                                         | 8.55 us: 1.17x slower                                                         |
| async_generators         | 241 ms                                                          | 286 ms: 1.19x slower                                                          |
| python_startup_no_site   | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| nbody                    | 79.1 ms                                                         | 96.5 ms: 1.22x slower                                                         |
| telco                    | 4.83 ms                                                         | 6.58 ms: 1.36x slower                                                         |
| coverage                 | 46.6 ms                                                         | 489 ms: 10.50x slower                                                         |
| thrift                   | 902 us                                                          | 11.1 ms: 12.31x slower                                                        |
| Geometric mean           | (ref)                                                           | 1.06x faster                                                                  |

Benchmark hidden because not significant (1): scimark_monte_carlo
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown