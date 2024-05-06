# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.06x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 252 ms: 1.05x faster                                                          |
| chameleon      | 6.42 ms                                                         | 6.20 ms: 1.04x faster                                                         |
| html5lib       | 52.1 ms                                                         | 45.5 ms: 1.14x faster                                                         |
| tornado_http   | 118 ms                                                          | 96.9 ms: 1.21x faster                                                         |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                  |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 473 ms: 1.95x faster                                                          |
| async_tree_io           | 940 ms                                                          | 548 ms: 1.72x faster                                                          |
| async_tree_none         | 394 ms                                                          | 234 ms: 1.68x faster                                                          |
| async_tree_memoization  | 467 ms                                                          | 285 ms: 1.64x faster                                                          |
| Geometric mean          | (ref)                                                           | 1.74x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 202 ms: 2.49x faster                                                          |
| float          | 69.6 ms                                                         | 53.6 ms: 1.30x faster                                                         |
| nbody          | 79.1 ms                                                         | 92.1 ms: 1.16x slower                                                         |
| Geometric mean | (ref)                                                           | 1.41x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 131 ms                                                          | 119 ms: 1.09x faster                                                          |
| regex_compile  | 117 ms                                                          | 115 ms: 1.01x faster                                                          |
| regex_v8       | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                         |
| regex_effbot   | 1.66 ms                                                         | 1.92 ms: 1.15x slower                                                         |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.70 ms: 1.47x faster                                                         |
| pickle_pure_python   | 280 us                                                          | 221 us: 1.27x faster                                                          |
| tomli_loads          | 1.91 sec                                                        | 1.67 sec: 1.14x faster                                                        |
| unpickle_pure_python | 189 us                                                          | 166 us: 1.14x faster                                                          |
| xml_etree_process    | 48.1 ms                                                         | 42.6 ms: 1.13x faster                                                         |
| xml_etree_parse      | 120 ms                                                          | 108 ms: 1.12x faster                                                          |
| json_loads           | 22.4 us                                                         | 20.1 us: 1.11x faster                                                         |
| xml_etree_iterparse  | 70.8 ms                                                         | 64.8 ms: 1.09x faster                                                         |
| unpickle_list        | 2.98 us                                                         | 2.90 us: 1.03x faster                                                         |
| xml_etree_generate   | 61.6 ms                                                         | 60.8 ms: 1.01x faster                                                         |
| pickle_list          | 3.22 us                                                         | 3.18 us: 1.01x faster                                                         |
| pickle               | 7.83 us                                                         | 8.04 us: 1.03x slower                                                         |
| pickle_dict          | 18.2 us                                                         | 19.6 us: 1.08x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.09x faster                                                                  |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                         |
| python_startup_no_site | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.05 ms: 1.29x faster                                                         |
| django_template | 36.0 ms                                                         | 33.0 ms: 1.09x faster                                                         |
| genshi_text     | 21.0 ms                                                         | 20.8 ms: 1.01x faster                                                         |
| genshi_xml      | 46.6 ms                                                         | 47.0 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                           | 1.09x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 95.3 us: 4.15x faster                                                         |
| pidigits                 | 502 ms                                                          | 202 ms: 2.49x faster                                                          |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 473 ms: 1.95x faster                                                          |
| pylint                   | 384 ms                                                          | 222 ms: 1.73x faster                                                          |
| async_tree_io            | 940 ms                                                          | 548 ms: 1.72x faster                                                          |
| async_tree_none          | 394 ms                                                          | 234 ms: 1.68x faster                                                          |
| async_tree_memoization   | 467 ms                                                          | 285 ms: 1.64x faster                                                          |
| logging_silent           | 97.9 ns                                                         | 60.7 ns: 1.61x faster                                                         |
| deltablue                | 4.04 ms                                                         | 2.55 ms: 1.58x faster                                                         |
| json_dumps               | 9.82 ms                                                         | 6.70 ms: 1.47x faster                                                         |
| generators               | 31.6 ms                                                         | 23.2 ms: 1.36x faster                                                         |
| sqlglot_parse            | 1.33 ms                                                         | 983 us: 1.35x faster                                                          |
| float                    | 69.6 ms                                                         | 53.6 ms: 1.30x faster                                                         |
| mako                     | 9.10 ms                                                         | 7.05 ms: 1.29x faster                                                         |
| crypto_pyaes             | 81.3 ms                                                         | 63.2 ms: 1.29x faster                                                         |
| sqlglot_transpile        | 1.58 ms                                                         | 1.24 ms: 1.28x faster                                                         |
| pickle_pure_python       | 280 us                                                          | 221 us: 1.27x faster                                                          |
| tornado_http             | 118 ms                                                          | 96.9 ms: 1.21x faster                                                         |
| go                       | 146 ms                                                          | 121 ms: 1.21x faster                                                          |
| chaos                    | 74.4 ms                                                         | 61.8 ms: 1.20x faster                                                         |
| pycparser                | 1.04 sec                                                        | 865 ms: 1.20x faster                                                          |
| coroutines               | 17.9 ms                                                         | 14.9 ms: 1.20x faster                                                         |
| scimark_sor              | 115 ms                                                          | 95.6 ms: 1.20x faster                                                         |
| asyncio_tcp              | 744 ms                                                          | 623 ms: 1.19x faster                                                          |
| sqlite_synth             | 2.29 us                                                         | 1.92 us: 1.19x faster                                                         |
| richards_super           | 49.9 ms                                                         | 42.1 ms: 1.18x faster                                                         |
| comprehensions           | 17.7 us                                                         | 15.1 us: 1.18x faster                                                         |
| deepcopy_memo            | 29.6 us                                                         | 25.5 us: 1.16x faster                                                         |
| pyflate                  | 422 ms                                                          | 364 ms: 1.16x faster                                                          |
| raytrace                 | 303 ms                                                          | 265 ms: 1.14x faster                                                          |
| html5lib                 | 52.1 ms                                                         | 45.5 ms: 1.14x faster                                                         |
| tomli_loads              | 1.91 sec                                                        | 1.67 sec: 1.14x faster                                                        |
| unpickle_pure_python     | 189 us                                                          | 166 us: 1.14x faster                                                          |
| spectral_norm            | 80.2 ms                                                         | 70.4 ms: 1.14x faster                                                         |
| json                     | 4.76 ms                                                         | 4.19 ms: 1.14x faster                                                         |
| xml_etree_process        | 48.1 ms                                                         | 42.6 ms: 1.13x faster                                                         |
| sympy_sum                | 122 ms                                                          | 109 ms: 1.12x faster                                                          |
| xml_etree_parse          | 120 ms                                                          | 108 ms: 1.12x faster                                                          |
| json_loads               | 22.4 us                                                         | 20.1 us: 1.11x faster                                                         |
| bench_thread_pool        | 1.12 ms                                                         | 1.01 ms: 1.11x faster                                                         |
| xml_etree_iterparse      | 70.8 ms                                                         | 64.8 ms: 1.09x faster                                                         |
| regex_dna                | 131 ms                                                          | 119 ms: 1.09x faster                                                          |
| django_template          | 36.0 ms                                                         | 33.0 ms: 1.09x faster                                                         |
| richards                 | 40.3 ms                                                         | 37.0 ms: 1.09x faster                                                         |
| sympy_str                | 229 ms                                                          | 216 ms: 1.06x faster                                                          |
| deepcopy                 | 310 us                                                          | 294 us: 1.06x faster                                                          |
| 2to3                     | 265 ms                                                          | 252 ms: 1.05x faster                                                          |
| scimark_lu               | 89.8 ms                                                         | 86.1 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.12 ms: 1.04x faster                                                         |
| mdp                      | 1.83 sec                                                        | 1.76 sec: 1.04x faster                                                        |
| sympy_expand             | 391 ms                                                          | 377 ms: 1.04x faster                                                          |
| chameleon                | 6.42 ms                                                         | 6.20 ms: 1.04x faster                                                         |
| unpickle_list            | 2.98 us                                                         | 2.90 us: 1.03x faster                                                         |
| sympy_integrate          | 16.6 ms                                                         | 16.2 ms: 1.03x faster                                                         |
| deepcopy_reduce          | 2.68 us                                                         | 2.62 us: 1.02x faster                                                         |
| xml_etree_generate       | 61.6 ms                                                         | 60.8 ms: 1.01x faster                                                         |
| regex_compile            | 117 ms                                                          | 115 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 16.8 sec: 1.01x faster                                                        |
| pickle_list              | 3.22 us                                                         | 3.18 us: 1.01x faster                                                         |
| genshi_text              | 21.0 ms                                                         | 20.8 ms: 1.01x faster                                                         |
| genshi_xml               | 46.6 ms                                                         | 47.0 ms: 1.01x slower                                                         |
| scimark_monte_carlo      | 61.9 ms                                                         | 62.5 ms: 1.01x slower                                                         |
| meteor_contest           | 80.0 ms                                                         | 81.6 ms: 1.02x slower                                                         |
| sqlglot_optimize         | 44.7 ms                                                         | 45.7 ms: 1.02x slower                                                         |
| pickle                   | 7.83 us                                                         | 8.04 us: 1.03x slower                                                         |
| regex_v8                 | 15.8 ms                                                         | 16.2 ms: 1.03x slower                                                         |
| sqlglot_normalize        | 230 ms                                                          | 238 ms: 1.03x slower                                                          |
| hexiom                   | 6.13 ms                                                         | 6.36 ms: 1.04x slower                                                         |
| nqueens                  | 87.1 ms                                                         | 90.5 ms: 1.04x slower                                                         |
| python_startup           | 22.9 ms                                                         | 24.2 ms: 1.06x slower                                                         |
| create_gc_cycles         | 694 us                                                          | 738 us: 1.06x slower                                                          |
| pathlib                  | 81.2 ms                                                         | 86.7 ms: 1.07x slower                                                         |
| pickle_dict              | 18.2 us                                                         | 19.6 us: 1.08x slower                                                         |
| pprint_pformat           | 1.37 sec                                                        | 1.48 sec: 1.08x slower                                                        |
| bench_mp_pool            | 66.4 ms                                                         | 72.1 ms: 1.09x slower                                                         |
| scimark_fft              | 216 ms                                                          | 236 ms: 1.09x slower                                                          |
| pprint_safe_repr         | 658 ms                                                          | 727 ms: 1.10x slower                                                          |
| gc_traversal             | 1.28 ms                                                         | 1.44 ms: 1.13x slower                                                         |
| logging_format           | 7.91 us                                                         | 8.92 us: 1.13x slower                                                         |
| logging_simple           | 7.29 us                                                         | 8.34 us: 1.14x slower                                                         |
| unpack_sequence          | 40.0 ns                                                         | 45.9 ns: 1.15x slower                                                         |
| regex_effbot             | 1.66 ms                                                         | 1.92 ms: 1.15x slower                                                         |
| nbody                    | 79.1 ms                                                         | 92.1 ms: 1.16x slower                                                         |
| python_startup_no_site   | 18.1 ms                                                         | 21.8 ms: 1.21x slower                                                         |
| async_generators         | 241 ms                                                          | 294 ms: 1.22x slower                                                          |
| telco                    | 4.83 ms                                                         | 6.41 ms: 1.33x slower                                                         |
| coverage                 | 46.6 ms                                                         | 477 ms: 10.25x slower                                                         |
| thrift                   | 902 us                                                          | 11.2 ms: 12.45x slower                                                        |
| Geometric mean           | (ref)                                                           | 1.06x faster                                                                  |

Benchmark hidden because not significant (3): docutils, unpickle, fannkuch
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown