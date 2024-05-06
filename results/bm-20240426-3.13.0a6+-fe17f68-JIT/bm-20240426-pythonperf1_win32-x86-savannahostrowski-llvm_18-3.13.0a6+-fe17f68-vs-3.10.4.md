# Results vs. 3.10.4

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-x86
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 97.82%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 265 ms                                                          | 270 ms: 1.02x slower                                                          |
| chameleon      | 6.42 ms                                                         | 6.48 ms: 1.01x slower                                                         |
| docutils       | 1.95 sec                                                        | 1.99 sec: 1.02x slower                                                        |
| html5lib       | 52.1 ms                                                         | 46.1 ms: 1.13x faster                                                         |
| tornado_http   | 118 ms                                                          | 107 ms: 1.10x faster                                                          |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 922 ms                                                          | 502 ms: 1.84x faster                                                          |
| async_tree_io           | 940 ms                                                          | 562 ms: 1.67x faster                                                          |
| async_tree_none         | 394 ms                                                          | 248 ms: 1.59x faster                                                          |
| async_tree_memoization  | 467 ms                                                          | 301 ms: 1.55x faster                                                          |
| Geometric mean          | (ref)                                                           | 1.66x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 502 ms                                                          | 199 ms: 2.53x faster                                                          |
| float          | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                         |
| nbody          | 79.1 ms                                                         | 96.2 ms: 1.22x slower                                                         |
| Geometric mean | (ref)                                                           | 1.39x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 117 ms                                                          | 109 ms: 1.07x faster                                                          |
| regex_dna      | 131 ms                                                          | 128 ms: 1.02x faster                                                          |
| regex_v8       | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                         |
| regex_effbot   | 1.66 ms                                                         | 2.00 ms: 1.20x slower                                                         |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.82 ms                                                         | 6.90 ms: 1.42x faster                                                         |
| pickle_pure_python   | 280 us                                                          | 224 us: 1.25x faster                                                          |
| xml_etree_parse      | 120 ms                                                          | 104 ms: 1.15x faster                                                          |
| unpickle_pure_python | 189 us                                                          | 165 us: 1.15x faster                                                          |
| json_loads           | 22.4 us                                                         | 20.5 us: 1.09x faster                                                         |
| tomli_loads          | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                        |
| xml_etree_iterparse  | 70.8 ms                                                         | 65.7 ms: 1.08x faster                                                         |
| unpickle_list        | 2.98 us                                                         | 2.80 us: 1.07x faster                                                         |
| xml_etree_process    | 48.1 ms                                                         | 45.4 ms: 1.06x faster                                                         |
| pickle_list          | 3.22 us                                                         | 3.28 us: 1.02x slower                                                         |
| xml_etree_generate   | 61.6 ms                                                         | 62.9 ms: 1.02x slower                                                         |
| pickle               | 7.83 us                                                         | 8.09 us: 1.03x slower                                                         |
| unpickle             | 9.82 us                                                         | 10.2 us: 1.04x slower                                                         |
| pickle_dict          | 18.2 us                                                         | 20.3 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.07x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.9 ms                                                         | 24.6 ms: 1.07x slower                                                         |
| python_startup_no_site | 18.1 ms                                                         | 20.6 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.10 ms                                                         | 7.09 ms: 1.28x faster                                                         |
| django_template | 36.0 ms                                                         | 33.8 ms: 1.06x faster                                                         |
| genshi_xml      | 46.6 ms                                                         | 52.1 ms: 1.12x slower                                                         |
| genshi_text     | 21.0 ms                                                         | 24.3 ms: 1.16x slower                                                         |
| Geometric mean  | (ref)                                                           | 1.01x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 396 us                                                          | 154 us: 2.57x faster                                                          |
| pidigits                 | 502 ms                                                          | 199 ms: 2.53x faster                                                          |
| sqlglot_normalize        | 230 ms                                                          | 101 ms: 2.27x faster                                                          |
| async_tree_cpu_io_mixed  | 922 ms                                                          | 502 ms: 1.84x faster                                                          |
| async_tree_io            | 940 ms                                                          | 562 ms: 1.67x faster                                                          |
| logging_silent           | 97.9 ns                                                         | 60.8 ns: 1.61x faster                                                         |
| async_tree_none          | 394 ms                                                          | 248 ms: 1.59x faster                                                          |
| pylint                   | 384 ms                                                          | 243 ms: 1.58x faster                                                          |
| async_tree_memoization   | 467 ms                                                          | 301 ms: 1.55x faster                                                          |
| deltablue                | 4.04 ms                                                         | 2.79 ms: 1.45x faster                                                         |
| json_dumps               | 9.82 ms                                                         | 6.90 ms: 1.42x faster                                                         |
| generators               | 31.6 ms                                                         | 23.0 ms: 1.37x faster                                                         |
| raytrace                 | 303 ms                                                          | 223 ms: 1.36x faster                                                          |
| crypto_pyaes             | 81.3 ms                                                         | 62.2 ms: 1.31x faster                                                         |
| float                    | 69.6 ms                                                         | 53.7 ms: 1.30x faster                                                         |
| sqlglot_parse            | 1.33 ms                                                         | 1.03 ms: 1.29x faster                                                         |
| mako                     | 9.10 ms                                                         | 7.09 ms: 1.28x faster                                                         |
| richards_super           | 49.9 ms                                                         | 38.9 ms: 1.28x faster                                                         |
| pickle_pure_python       | 280 us                                                          | 224 us: 1.25x faster                                                          |
| pycparser                | 1.04 sec                                                        | 851 ms: 1.22x faster                                                          |
| chaos                    | 74.4 ms                                                         | 60.9 ms: 1.22x faster                                                         |
| sqlglot_transpile        | 1.58 ms                                                         | 1.30 ms: 1.22x faster                                                         |
| richards                 | 40.3 ms                                                         | 34.0 ms: 1.18x faster                                                         |
| spectral_norm            | 80.2 ms                                                         | 68.0 ms: 1.18x faster                                                         |
| deepcopy_memo            | 29.6 us                                                         | 25.1 us: 1.18x faster                                                         |
| go                       | 146 ms                                                          | 124 ms: 1.17x faster                                                          |
| pyflate                  | 422 ms                                                          | 362 ms: 1.17x faster                                                          |
| scimark_sor              | 115 ms                                                          | 99.3 ms: 1.16x faster                                                         |
| sqlite_synth             | 2.29 us                                                         | 1.98 us: 1.15x faster                                                         |
| xml_etree_parse          | 120 ms                                                          | 104 ms: 1.15x faster                                                          |
| unpickle_pure_python     | 189 us                                                          | 165 us: 1.15x faster                                                          |
| html5lib                 | 52.1 ms                                                         | 46.1 ms: 1.13x faster                                                         |
| json                     | 4.76 ms                                                         | 4.22 ms: 1.13x faster                                                         |
| comprehensions           | 17.7 us                                                         | 16.1 us: 1.10x faster                                                         |
| tornado_http             | 118 ms                                                          | 107 ms: 1.10x faster                                                          |
| bench_thread_pool        | 1.12 ms                                                         | 1.02 ms: 1.10x faster                                                         |
| coroutines               | 17.9 ms                                                         | 16.4 ms: 1.10x faster                                                         |
| json_loads               | 22.4 us                                                         | 20.5 us: 1.09x faster                                                         |
| tomli_loads              | 1.91 sec                                                        | 1.75 sec: 1.09x faster                                                        |
| sympy_sum                | 122 ms                                                          | 113 ms: 1.08x faster                                                          |
| xml_etree_iterparse      | 70.8 ms                                                         | 65.7 ms: 1.08x faster                                                         |
| regex_compile            | 117 ms                                                          | 109 ms: 1.07x faster                                                          |
| unpickle_list            | 2.98 us                                                         | 2.80 us: 1.07x faster                                                         |
| django_template          | 36.0 ms                                                         | 33.8 ms: 1.06x faster                                                         |
| xml_etree_process        | 48.1 ms                                                         | 45.4 ms: 1.06x faster                                                         |
| scimark_monte_carlo      | 61.9 ms                                                         | 59.3 ms: 1.04x faster                                                         |
| sympy_str                | 229 ms                                                          | 223 ms: 1.03x faster                                                          |
| scimark_sparse_mat_mult  | 3.24 ms                                                         | 3.17 ms: 1.02x faster                                                         |
| deepcopy_reduce          | 2.68 us                                                         | 2.64 us: 1.02x faster                                                         |
| regex_dna                | 131 ms                                                          | 128 ms: 1.02x faster                                                          |
| deepcopy                 | 310 us                                                          | 305 us: 1.02x faster                                                          |
| sympy_expand             | 391 ms                                                          | 385 ms: 1.01x faster                                                          |
| fannkuch                 | 317 ms                                                          | 314 ms: 1.01x faster                                                          |
| sympy_integrate          | 16.6 ms                                                         | 16.7 ms: 1.01x slower                                                         |
| chameleon                | 6.42 ms                                                         | 6.48 ms: 1.01x slower                                                         |
| asyncio_tcp_ssl          | 17.0 sec                                                        | 17.1 sec: 1.01x slower                                                        |
| 2to3                     | 265 ms                                                          | 270 ms: 1.02x slower                                                          |
| pickle_list              | 3.22 us                                                         | 3.28 us: 1.02x slower                                                         |
| xml_etree_generate       | 61.6 ms                                                         | 62.9 ms: 1.02x slower                                                         |
| docutils                 | 1.95 sec                                                        | 1.99 sec: 1.02x slower                                                        |
| regex_v8                 | 15.8 ms                                                         | 16.1 ms: 1.02x slower                                                         |
| hexiom                   | 6.13 ms                                                         | 6.30 ms: 1.03x slower                                                         |
| asyncio_tcp              | 744 ms                                                          | 764 ms: 1.03x slower                                                          |
| pickle                   | 7.83 us                                                         | 8.09 us: 1.03x slower                                                         |
| unpickle                 | 9.82 us                                                         | 10.2 us: 1.04x slower                                                         |
| create_gc_cycles         | 694 us                                                          | 737 us: 1.06x slower                                                          |
| nqueens                  | 87.1 ms                                                         | 93.2 ms: 1.07x slower                                                         |
| python_startup           | 22.9 ms                                                         | 24.6 ms: 1.07x slower                                                         |
| meteor_contest           | 80.0 ms                                                         | 86.0 ms: 1.07x slower                                                         |
| sqlglot_optimize         | 44.7 ms                                                         | 48.2 ms: 1.08x slower                                                         |
| scimark_fft              | 216 ms                                                          | 235 ms: 1.09x slower                                                          |
| pprint_pformat           | 1.37 sec                                                        | 1.49 sec: 1.09x slower                                                        |
| pathlib                  | 81.2 ms                                                         | 88.8 ms: 1.09x slower                                                         |
| logging_format           | 7.91 us                                                         | 8.72 us: 1.10x slower                                                         |
| pprint_safe_repr         | 658 ms                                                          | 727 ms: 1.10x slower                                                          |
| pickle_dict              | 18.2 us                                                         | 20.3 us: 1.11x slower                                                         |
| logging_simple           | 7.29 us                                                         | 8.11 us: 1.11x slower                                                         |
| bench_mp_pool            | 66.4 ms                                                         | 74.1 ms: 1.12x slower                                                         |
| genshi_xml               | 46.6 ms                                                         | 52.1 ms: 1.12x slower                                                         |
| python_startup_no_site   | 18.1 ms                                                         | 20.6 ms: 1.14x slower                                                         |
| gc_traversal             | 1.28 ms                                                         | 1.47 ms: 1.15x slower                                                         |
| genshi_text              | 21.0 ms                                                         | 24.3 ms: 1.16x slower                                                         |
| regex_effbot             | 1.66 ms                                                         | 2.00 ms: 1.20x slower                                                         |
| nbody                    | 79.1 ms                                                         | 96.2 ms: 1.22x slower                                                         |
| async_generators         | 241 ms                                                          | 302 ms: 1.25x slower                                                          |
| telco                    | 4.83 ms                                                         | 6.41 ms: 1.33x slower                                                         |
| coverage                 | 46.6 ms                                                         | 420 ms: 9.01x slower                                                          |
| thrift                   | 902 us                                                          | 10.8 ms: 12.00x slower                                                        |
| Geometric mean           | (ref)                                                           | 1.05x faster                                                                  |

Benchmark hidden because not significant (2): mdp, scimark_lu
Ignored benchmarks (8) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1_win32-x86-python-v3.10.4-3.10.4-9d38120.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-fe17f68-JIT/bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 97.82% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown