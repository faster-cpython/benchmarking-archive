# Results vs. 3.10.4

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 302 ms: 1.16x faster                                                       |
| chameleon      | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                                      |
| docutils       | 3.41 sec                                                     | 3.09 sec: 1.11x faster                                                     |
| html5lib       | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                      |
| tornado_http   | 157 ms                                                       | 122 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                        | 1.22x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 371 ms: 1.86x faster                                                       |
| async_tree_io           | 1.60 sec                                                     | 883 ms: 1.81x faster                                                       |
| async_tree_memoization  | 819 ms                                                       | 464 ms: 1.77x faster                                                       |
| async_tree_cpu_io_mixed | 936 ms                                                       | 614 ms: 1.52x faster                                                       |
| Geometric mean          | (ref)                                                        | 1.74x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.0 ms: 1.46x faster                                                      |
| nbody          | 134 ms                                                       | 98.9 ms: 1.36x faster                                                      |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                        | 1.27x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                       |
| regex_dna      | 261 ms                                                       | 238 ms: 1.10x faster                                                       |
| regex_v8       | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                      |
| regex_effbot   | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                        | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 312 us                                                       | 214 us: 1.46x faster                                                       |
| pickle_pure_python   | 455 us                                                       | 317 us: 1.44x faster                                                       |
| tomli_loads          | 2.92 sec                                                     | 2.09 sec: 1.40x faster                                                     |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.37x faster                                                      |
| xml_etree_process    | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                      |
| json_loads           | 30.3 us                                                      | 24.6 us: 1.23x faster                                                      |
| xml_etree_parse      | 160 ms                                                       | 142 ms: 1.13x faster                                                       |
| xml_etree_generate   | 92.3 ms                                                      | 83.0 ms: 1.11x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                       | 100 ms: 1.10x faster                                                       |
| unpickle_list        | 4.65 us                                                      | 4.73 us: 1.02x slower                                                      |
| pickle_dict          | 29.5 us                                                      | 30.5 us: 1.03x slower                                                      |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                      |
| pickle_list          | 4.12 us                                                      | 4.50 us: 1.09x slower                                                      |
| unpickle             | 13.5 us                                                      | 15.6 us: 1.16x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.14x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                      |
| python_startup_no_site | 7.33 ms                                                      | 9.43 ms: 1.29x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.65 ms: 1.52x faster                                                      |
| django_template | 50.2 ms                                                      | 40.4 ms: 1.24x faster                                                      |
| genshi_text     | 31.4 ms                                                      | 29.1 ms: 1.08x faster                                                      |
| genshi_xml      | 63.3 ms                                                      | 62.3 ms: 1.02x faster                                                      |
| Geometric mean  | (ref)                                                        | 1.20x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 185 us: 2.91x faster                                                       |
| asyncio_tcp              | 779 ms                                                       | 374 ms: 2.08x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.80 ms: 1.97x faster                                                      |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                     |
| async_tree_none          | 692 ms                                                       | 371 ms: 1.86x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 883 ms: 1.81x faster                                                       |
| richards_super           | 90.6 ms                                                      | 51.2 ms: 1.77x faster                                                      |
| async_tree_memoization   | 819 ms                                                       | 464 ms: 1.77x faster                                                       |
| logging_silent           | 167 ns                                                       | 95.4 ns: 1.75x faster                                                      |
| raytrace                 | 489 ms                                                       | 281 ms: 1.74x faster                                                       |
| generators               | 57.3 ms                                                      | 34.4 ms: 1.67x faster                                                      |
| chaos                    | 109 ms                                                       | 65.7 ms: 1.65x faster                                                      |
| richards                 | 75.1 ms                                                      | 45.8 ms: 1.64x faster                                                      |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.57x faster                                                      |
| crypto_pyaes             | 119 ms                                                       | 76.3 ms: 1.56x faster                                                      |
| scimark_monte_carlo      | 107 ms                                                       | 69.1 ms: 1.55x faster                                                      |
| pylint                   | 566 ms                                                       | 370 ms: 1.53x faster                                                       |
| spectral_norm            | 139 ms                                                       | 90.9 ms: 1.53x faster                                                      |
| mako                     | 14.7 ms                                                      | 9.65 ms: 1.52x faster                                                      |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 614 ms: 1.52x faster                                                       |
| go                       | 262 ms                                                       | 173 ms: 1.52x faster                                                       |
| pyflate                  | 733 ms                                                       | 494 ms: 1.48x faster                                                       |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.47x faster                                                      |
| float                    | 111 ms                                                       | 76.0 ms: 1.46x faster                                                      |
| unpickle_pure_python     | 312 us                                                       | 214 us: 1.46x faster                                                       |
| pickle_pure_python       | 455 us                                                       | 317 us: 1.44x faster                                                       |
| coroutines               | 30.3 ms                                                      | 21.6 ms: 1.40x faster                                                      |
| scimark_lu               | 167 ms                                                       | 119 ms: 1.40x faster                                                       |
| tomli_loads              | 2.92 sec                                                     | 2.09 sec: 1.40x faster                                                     |
| comprehensions           | 26.7 us                                                      | 19.3 us: 1.38x faster                                                      |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.37x faster                                                      |
| logging_simple           | 8.88 us                                                      | 6.52 us: 1.36x faster                                                      |
| nbody                    | 134 ms                                                       | 98.9 ms: 1.36x faster                                                      |
| logging_format           | 9.64 us                                                      | 7.15 us: 1.35x faster                                                      |
| hexiom                   | 9.42 ms                                                      | 7.02 ms: 1.34x faster                                                      |
| thrift                   | 1.18 ms                                                      | 877 us: 1.34x faster                                                       |
| deepcopy_memo            | 49.8 us                                                      | 37.4 us: 1.33x faster                                                      |
| bench_mp_pool            | 6.37 ms                                                      | 4.80 ms: 1.33x faster                                                      |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                       |
| xml_etree_process        | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                      |
| pycparser                | 1.67 sec                                                     | 1.29 sec: 1.29x faster                                                     |
| tornado_http             | 157 ms                                                       | 122 ms: 1.29x faster                                                       |
| fannkuch                 | 483 ms                                                       | 376 ms: 1.28x faster                                                       |
| pprint_pformat           | 2.15 sec                                                     | 1.68 sec: 1.28x faster                                                     |
| html5lib                 | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                      |
| chameleon                | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                                      |
| pprint_safe_repr         | 1.05 sec                                                     | 839 ms: 1.25x faster                                                       |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.06 ms: 1.25x faster                                                      |
| django_template          | 50.2 ms                                                      | 40.4 ms: 1.24x faster                                                      |
| json_loads               | 30.3 us                                                      | 24.6 us: 1.23x faster                                                      |
| pathlib                  | 21.4 ms                                                      | 17.6 ms: 1.22x faster                                                      |
| bench_thread_pool        | 1.14 ms                                                      | 941 us: 1.21x faster                                                       |
| dulwich_log              | 81.1 ms                                                      | 67.4 ms: 1.20x faster                                                      |
| scimark_sor              | 180 ms                                                       | 151 ms: 1.19x faster                                                       |
| deepcopy                 | 468 us                                                       | 393 us: 1.19x faster                                                       |
| dask                     | 472 ms                                                       | 402 ms: 1.18x faster                                                       |
| sympy_sum                | 193 ms                                                       | 165 ms: 1.17x faster                                                       |
| sympy_expand             | 600 ms                                                       | 513 ms: 1.17x faster                                                       |
| mdp                      | 3.01 sec                                                     | 2.57 sec: 1.17x faster                                                     |
| sympy_str                | 360 ms                                                       | 308 ms: 1.17x faster                                                       |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.44 us: 1.16x faster                                                      |
| 2to3                     | 350 ms                                                       | 302 ms: 1.16x faster                                                       |
| nqueens                  | 115 ms                                                       | 100 ms: 1.15x faster                                                       |
| scimark_fft              | 361 ms                                                       | 318 ms: 1.14x faster                                                       |
| xml_etree_parse          | 160 ms                                                       | 142 ms: 1.13x faster                                                       |
| sqlglot_optimize         | 70.1 ms                                                      | 63.1 ms: 1.11x faster                                                      |
| xml_etree_generate       | 92.3 ms                                                      | 83.0 ms: 1.11x faster                                                      |
| mypy2                    | 933 ms                                                       | 843 ms: 1.11x faster                                                       |
| docutils                 | 3.41 sec                                                     | 3.09 sec: 1.11x faster                                                     |
| xml_etree_iterparse      | 110 ms                                                       | 100 ms: 1.10x faster                                                       |
| json                     | 5.86 ms                                                      | 5.31 ms: 1.10x faster                                                      |
| sqlite_synth             | 2.99 us                                                      | 2.71 us: 1.10x faster                                                      |
| sympy_integrate          | 28.2 ms                                                      | 25.6 ms: 1.10x faster                                                      |
| regex_dna                | 261 ms                                                       | 238 ms: 1.10x faster                                                       |
| async_generators         | 421 ms                                                       | 389 ms: 1.08x faster                                                       |
| genshi_text              | 31.4 ms                                                      | 29.1 ms: 1.08x faster                                                      |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.05x faster                                                      |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                      |
| regex_v8                 | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                      |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                       |
| meteor_contest           | 138 ms                                                       | 135 ms: 1.02x faster                                                       |
| genshi_xml               | 63.3 ms                                                      | 62.3 ms: 1.02x faster                                                      |
| unpickle_list            | 4.65 us                                                      | 4.73 us: 1.02x slower                                                      |
| pickle_dict              | 29.5 us                                                      | 30.5 us: 1.03x slower                                                      |
| pickle                   | 9.89 us                                                      | 10.3 us: 1.04x slower                                                      |
| create_gc_cycles         | 1.76 ms                                                      | 1.89 ms: 1.07x slower                                                      |
| pickle_list              | 4.12 us                                                      | 4.50 us: 1.09x slower                                                      |
| telco                    | 7.23 ms                                                      | 8.05 ms: 1.11x slower                                                      |
| regex_effbot             | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                      |
| unpickle                 | 13.5 us                                                      | 15.6 us: 1.16x slower                                                      |
| python_startup           | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                      |
| coverage                 | 63.3 ms                                                      | 79.6 ms: 1.26x slower                                                      |
| python_startup_no_site   | 7.33 ms                                                      | 9.43 ms: 1.29x slower                                                      |
| gc_traversal             | 3.42 ms                                                      | 4.43 ms: 1.30x slower                                                      |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                               |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-8d9855f-JIT/bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.21x