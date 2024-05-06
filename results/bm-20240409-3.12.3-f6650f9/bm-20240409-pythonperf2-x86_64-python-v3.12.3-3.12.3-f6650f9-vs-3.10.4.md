# Results vs. 3.10.4

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 279 ms: 1.25x faster                                         |
| chameleon      | 9.44 ms                                                      | 7.22 ms: 1.31x faster                                        |
| docutils       | 3.41 sec                                                     | 2.85 sec: 1.20x faster                                       |
| html5lib       | 94.6 ms                                                      | 69.7 ms: 1.36x faster                                        |
| tornado_http   | 157 ms                                                       | 120 ms: 1.31x faster                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 451 ms: 1.53x faster                                         |
| async_tree_io           | 1.60 sec                                                     | 1.04 sec: 1.53x faster                                       |
| async_tree_memoization  | 819 ms                                                       | 545 ms: 1.50x faster                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 693 ms: 1.35x faster                                         |
| Geometric mean          | (ref)                                                        | 1.48x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 86.3 ms: 1.55x faster                                        |
| float          | 111 ms                                                       | 77.7 ms: 1.43x faster                                        |
| pidigits       | 271 ms                                                       | 264 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                        | 1.32x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 144 ms: 1.32x faster                                         |
| regex_v8       | 27.2 ms                                                      | 23.8 ms: 1.14x faster                                        |
| regex_dna      | 261 ms                                                       | 237 ms: 1.10x faster                                         |
| regex_effbot   | 3.09 ms                                                      | 3.45 ms: 1.12x slower                                        |
| Geometric mean | (ref)                                                        | 1.10x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_pure_python | 312 us                                                       | 205 us: 1.52x faster                                         |
| pickle_pure_python   | 455 us                                                       | 312 us: 1.46x faster                                         |
| json_dumps           | 14.5 ms                                                      | 10.3 ms: 1.41x faster                                        |
| tomli_loads          | 2.92 sec                                                     | 2.17 sec: 1.34x faster                                       |
| xml_etree_process    | 75.9 ms                                                      | 58.1 ms: 1.31x faster                                        |
| json_loads           | 30.3 us                                                      | 28.2 us: 1.08x faster                                        |
| xml_etree_parse      | 160 ms                                                       | 149 ms: 1.07x faster                                         |
| xml_etree_generate   | 92.3 ms                                                      | 86.8 ms: 1.06x faster                                        |
| xml_etree_iterparse  | 110 ms                                                       | 105 ms: 1.05x faster                                         |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                        |
| unpickle_list        | 4.65 us                                                      | 4.78 us: 1.03x slower                                        |
| pickle_dict          | 29.5 us                                                      | 30.6 us: 1.04x slower                                        |
| pickle_list          | 4.12 us                                                      | 4.41 us: 1.07x slower                                        |
| unpickle             | 13.5 us                                                      | 14.7 us: 1.09x slower                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 11.6 ms: 1.01x slower                                        |
| python_startup_no_site | 7.33 ms                                                      | 8.57 ms: 1.17x slower                                        |
| Geometric mean         | (ref)                                                        | 1.09x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                        |
| django_template | 50.2 ms                                                      | 38.0 ms: 1.32x faster                                        |
| genshi_text     | 31.4 ms                                                      | 24.7 ms: 1.27x faster                                        |
| genshi_xml      | 63.3 ms                                                      | 53.0 ms: 1.19x faster                                        |
| Geometric mean  | (ref)                                                        | 1.31x faster                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 125 us: 4.31x faster                                         |
| deltablue                | 7.50 ms                                                      | 3.23 ms: 2.32x faster                                        |
| asyncio_tcp              | 779 ms                                                       | 378 ms: 2.06x faster                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.56 sec: 1.98x faster                                       |
| richards_super           | 90.6 ms                                                      | 49.6 ms: 1.83x faster                                        |
| logging_silent           | 167 ns                                                       | 93.1 ns: 1.80x faster                                        |
| go                       | 262 ms                                                       | 146 ms: 1.79x faster                                         |
| chaos                    | 109 ms                                                       | 62.3 ms: 1.74x faster                                        |
| richards                 | 75.1 ms                                                      | 43.8 ms: 1.71x faster                                        |
| pyflate                  | 733 ms                                                       | 432 ms: 1.70x faster                                         |
| scimark_lu               | 167 ms                                                       | 99.0 ms: 1.69x faster                                        |
| scimark_sor              | 180 ms                                                       | 108 ms: 1.66x faster                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.38 ms: 1.63x faster                                        |
| pylint                   | 566 ms                                                       | 349 ms: 1.62x faster                                         |
| raytrace                 | 489 ms                                                       | 302 ms: 1.62x faster                                         |
| hexiom                   | 9.42 ms                                                      | 5.84 ms: 1.61x faster                                        |
| comprehensions           | 26.7 us                                                      | 16.6 us: 1.61x faster                                        |
| scimark_monte_carlo      | 107 ms                                                       | 67.8 ms: 1.58x faster                                        |
| nbody                    | 134 ms                                                       | 86.3 ms: 1.55x faster                                        |
| generators               | 57.3 ms                                                      | 36.9 ms: 1.55x faster                                        |
| async_tree_none          | 692 ms                                                       | 451 ms: 1.53x faster                                         |
| async_tree_io            | 1.60 sec                                                     | 1.04 sec: 1.53x faster                                       |
| unpickle_pure_python     | 312 us                                                       | 205 us: 1.52x faster                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.77 ms: 1.51x faster                                        |
| crypto_pyaes             | 119 ms                                                       | 79.1 ms: 1.51x faster                                        |
| async_tree_memoization   | 819 ms                                                       | 545 ms: 1.50x faster                                         |
| mako                     | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                        |
| spectral_norm            | 139 ms                                                       | 94.6 ms: 1.47x faster                                        |
| pickle_pure_python       | 455 us                                                       | 312 us: 1.46x faster                                         |
| fannkuch                 | 483 ms                                                       | 333 ms: 1.45x faster                                         |
| bench_mp_pool            | 6.37 ms                                                      | 4.41 ms: 1.44x faster                                        |
| float                    | 111 ms                                                       | 77.7 ms: 1.43x faster                                        |
| json_dumps               | 14.5 ms                                                      | 10.3 ms: 1.41x faster                                        |
| deepcopy_memo            | 49.8 us                                                      | 35.6 us: 1.40x faster                                        |
| html5lib                 | 94.6 ms                                                      | 69.7 ms: 1.36x faster                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 693 ms: 1.35x faster                                         |
| tomli_loads              | 2.92 sec                                                     | 2.17 sec: 1.34x faster                                       |
| logging_simple           | 8.88 us                                                      | 6.65 us: 1.33x faster                                        |
| logging_format           | 9.64 us                                                      | 7.26 us: 1.33x faster                                        |
| coroutines               | 30.3 ms                                                      | 22.9 ms: 1.32x faster                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.63 sec: 1.32x faster                                       |
| django_template          | 50.2 ms                                                      | 38.0 ms: 1.32x faster                                        |
| thrift                   | 1.18 ms                                                      | 890 us: 1.32x faster                                         |
| regex_compile            | 190 ms                                                       | 144 ms: 1.32x faster                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 797 ms: 1.32x faster                                         |
| tornado_http             | 157 ms                                                       | 120 ms: 1.31x faster                                         |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                       |
| nqueens                  | 115 ms                                                       | 87.7 ms: 1.31x faster                                        |
| chameleon                | 9.44 ms                                                      | 7.22 ms: 1.31x faster                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.1 ms: 1.31x faster                                        |
| deepcopy                 | 468 us                                                       | 363 us: 1.29x faster                                         |
| genshi_text              | 31.4 ms                                                      | 24.7 ms: 1.27x faster                                        |
| mypy2                    | 933 ms                                                       | 734 ms: 1.27x faster                                         |
| sympy_sum                | 193 ms                                                       | 152 ms: 1.27x faster                                         |
| sympy_str                | 360 ms                                                       | 287 ms: 1.25x faster                                         |
| 2to3                     | 350 ms                                                       | 279 ms: 1.25x faster                                         |
| dulwich_log              | 81.1 ms                                                      | 64.8 ms: 1.25x faster                                        |
| sqlglot_normalize        | 144 ms                                                       | 116 ms: 1.24x faster                                         |
| sympy_expand             | 600 ms                                                       | 483 ms: 1.24x faster                                         |
| sqlalchemy_imperative    | 22.7 ms                                                      | 18.5 ms: 1.23x faster                                        |
| sympy_integrate          | 28.2 ms                                                      | 23.0 ms: 1.23x faster                                        |
| scimark_fft              | 361 ms                                                       | 297 ms: 1.22x faster                                         |
| dask                     | 472 ms                                                       | 390 ms: 1.21x faster                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 58.0 ms: 1.21x faster                                        |
| deepcopy_reduce          | 4.01 us                                                      | 3.32 us: 1.21x faster                                        |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                       |
| docutils                 | 3.41 sec                                                     | 2.85 sec: 1.20x faster                                       |
| genshi_xml               | 63.3 ms                                                      | 53.0 ms: 1.19x faster                                        |
| bench_thread_pool        | 1.14 ms                                                      | 958 us: 1.19x faster                                         |
| sqlalchemy_declarative   | 190 ms                                                       | 160 ms: 1.19x faster                                         |
| aiohttp                  | 1.19 ms                                                      | 1.02 ms: 1.16x faster                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.37 ms: 1.16x faster                                        |
| gunicorn                 | 1.16 ms                                                      | 1.00 ms: 1.16x faster                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.53 ms: 1.15x faster                                        |
| regex_v8                 | 27.2 ms                                                      | 23.8 ms: 1.14x faster                                        |
| pathlib                  | 21.4 ms                                                      | 18.7 ms: 1.14x faster                                        |
| regex_dna                | 261 ms                                                       | 237 ms: 1.10x faster                                         |
| async_generators         | 421 ms                                                       | 381 ms: 1.10x faster                                         |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                        |
| meteor_contest           | 138 ms                                                       | 127 ms: 1.09x faster                                         |
| json_loads               | 30.3 us                                                      | 28.2 us: 1.08x faster                                        |
| xml_etree_parse          | 160 ms                                                       | 149 ms: 1.07x faster                                         |
| xml_etree_generate       | 92.3 ms                                                      | 86.8 ms: 1.06x faster                                        |
| json                     | 5.86 ms                                                      | 5.56 ms: 1.05x faster                                        |
| xml_etree_iterparse      | 110 ms                                                       | 105 ms: 1.05x faster                                         |
| telco                    | 7.23 ms                                                      | 6.95 ms: 1.04x faster                                        |
| pidigits                 | 271 ms                                                       | 264 ms: 1.03x faster                                         |
| python_startup           | 11.5 ms                                                      | 11.6 ms: 1.01x slower                                        |
| pickle                   | 9.89 us                                                      | 10.2 us: 1.03x slower                                        |
| unpickle_list            | 4.65 us                                                      | 4.78 us: 1.03x slower                                        |
| pickle_dict              | 29.5 us                                                      | 30.6 us: 1.04x slower                                        |
| coverage                 | 63.3 ms                                                      | 66.5 ms: 1.05x slower                                        |
| pickle_list              | 4.12 us                                                      | 4.41 us: 1.07x slower                                        |
| gc_traversal             | 3.42 ms                                                      | 3.72 ms: 1.09x slower                                        |
| unpickle                 | 13.5 us                                                      | 14.7 us: 1.09x slower                                        |
| regex_effbot             | 3.09 ms                                                      | 3.45 ms: 1.12x slower                                        |
| python_startup_no_site   | 7.33 ms                                                      | 8.57 ms: 1.17x slower                                        |
| Geometric mean           | (ref)                                                        | 1.32x faster                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (2) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, unpack_sequence
Ignored benchmarks (4) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x