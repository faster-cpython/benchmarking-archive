# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 302 ms: 1.16x faster                                                           |
| chameleon      | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                                          |
| docutils       | 3.41 sec                                                     | 3.12 sec: 1.10x faster                                                         |
| html5lib       | 94.6 ms                                                      | 74.9 ms: 1.26x faster                                                          |
| tornado_http   | 157 ms                                                       | 123 ms: 1.28x faster                                                           |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 854 ms: 1.87x faster                                                           |
| async_tree_memoization  | 819 ms                                                       | 446 ms: 1.84x faster                                                           |
| async_tree_none         | 692 ms                                                       | 380 ms: 1.82x faster                                                           |
| async_tree_cpu_io_mixed | 936 ms                                                       | 613 ms: 1.53x faster                                                           |
| Geometric mean          | (ref)                                                        | 1.76x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.9 ms: 1.46x faster                                                          |
| nbody          | 134 ms                                                       | 97.1 ms: 1.38x faster                                                          |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 145 ms: 1.31x faster                                                           |
| regex_dna      | 261 ms                                                       | 238 ms: 1.10x faster                                                           |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                          |
| regex_effbot   | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 307 us: 1.48x faster                                                           |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                                          |
| unpickle_pure_python | 312 us                                                       | 227 us: 1.37x faster                                                           |
| tomli_loads          | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 59.2 ms: 1.28x faster                                                          |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                          |
| xml_etree_parse      | 160 ms                                                       | 147 ms: 1.09x faster                                                           |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.09x faster                                                           |
| xml_etree_generate   | 92.3 ms                                                      | 85.8 ms: 1.08x faster                                                          |
| unpickle_list        | 4.65 us                                                      | 4.61 us: 1.01x faster                                                          |
| pickle_list          | 4.12 us                                                      | 4.43 us: 1.07x slower                                                          |
| pickle               | 9.89 us                                                      | 10.7 us: 1.09x slower                                                          |
| unpickle             | 13.5 us                                                      | 15.2 us: 1.13x slower                                                          |
| pickle_dict          | 29.5 us                                                      | 33.7 us: 1.14x slower                                                          |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                          |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 9.98 ms: 1.47x faster                                                          |
| genshi_text    | 31.4 ms                                                      | 27.2 ms: 1.15x faster                                                          |
| genshi_xml     | 63.3 ms                                                      | 59.5 ms: 1.06x faster                                                          |
| Geometric mean | (ref)                                                        | 1.22x faster                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 121 us: 4.44x faster                                                           |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.10x faster                                                           |
| deltablue                | 7.50 ms                                                      | 3.78 ms: 1.98x faster                                                          |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 854 ms: 1.87x faster                                                           |
| async_tree_memoization   | 819 ms                                                       | 446 ms: 1.84x faster                                                           |
| async_tree_none          | 692 ms                                                       | 380 ms: 1.82x faster                                                           |
| raytrace                 | 489 ms                                                       | 275 ms: 1.78x faster                                                           |
| richards_super           | 90.6 ms                                                      | 51.9 ms: 1.75x faster                                                          |
| generators               | 57.3 ms                                                      | 33.0 ms: 1.74x faster                                                          |
| logging_silent           | 167 ns                                                       | 98.2 ns: 1.70x faster                                                          |
| pylint                   | 566 ms                                                       | 341 ms: 1.66x faster                                                           |
| richards                 | 75.1 ms                                                      | 45.3 ms: 1.66x faster                                                          |
| chaos                    | 109 ms                                                       | 66.1 ms: 1.64x faster                                                          |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.59x faster                                                          |
| crypto_pyaes             | 119 ms                                                       | 77.6 ms: 1.54x faster                                                          |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 613 ms: 1.53x faster                                                           |
| go                       | 262 ms                                                       | 172 ms: 1.52x faster                                                           |
| pyflate                  | 733 ms                                                       | 486 ms: 1.51x faster                                                           |
| spectral_norm            | 139 ms                                                       | 92.8 ms: 1.50x faster                                                          |
| scimark_monte_carlo      | 107 ms                                                       | 72.1 ms: 1.49x faster                                                          |
| pickle_pure_python       | 455 us                                                       | 307 us: 1.48x faster                                                           |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.48x faster                                                          |
| mako                     | 14.7 ms                                                      | 9.98 ms: 1.47x faster                                                          |
| float                    | 111 ms                                                       | 75.9 ms: 1.46x faster                                                          |
| scimark_lu               | 167 ms                                                       | 115 ms: 1.45x faster                                                           |
| nbody                    | 134 ms                                                       | 97.1 ms: 1.38x faster                                                          |
| logging_simple           | 8.88 us                                                      | 6.43 us: 1.38x faster                                                          |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                                          |
| unpickle_pure_python     | 312 us                                                       | 227 us: 1.37x faster                                                           |
| tomli_loads              | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                         |
| coroutines               | 30.3 ms                                                      | 22.2 ms: 1.36x faster                                                          |
| comprehensions           | 26.7 us                                                      | 19.7 us: 1.36x faster                                                          |
| logging_format           | 9.64 us                                                      | 7.12 us: 1.35x faster                                                          |
| bench_mp_pool            | 6.37 ms                                                      | 4.71 ms: 1.35x faster                                                          |
| deepcopy_memo            | 49.8 us                                                      | 37.0 us: 1.34x faster                                                          |
| pycparser                | 1.67 sec                                                     | 1.24 sec: 1.34x faster                                                         |
| regex_compile            | 190 ms                                                       | 145 ms: 1.31x faster                                                           |
| thrift                   | 1.18 ms                                                      | 897 us: 1.31x faster                                                           |
| hexiom                   | 9.42 ms                                                      | 7.30 ms: 1.29x faster                                                          |
| xml_etree_process        | 75.9 ms                                                      | 59.2 ms: 1.28x faster                                                          |
| tornado_http             | 157 ms                                                       | 123 ms: 1.28x faster                                                           |
| chameleon                | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                                          |
| fannkuch                 | 483 ms                                                       | 381 ms: 1.27x faster                                                           |
| html5lib                 | 94.6 ms                                                      | 74.9 ms: 1.26x faster                                                          |
| pprint_pformat           | 2.15 sec                                                     | 1.72 sec: 1.25x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 841 ms: 1.25x faster                                                           |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.18 ms: 1.21x faster                                                          |
| scimark_sor              | 180 ms                                                       | 150 ms: 1.20x faster                                                           |
| deepcopy                 | 468 us                                                       | 390 us: 1.20x faster                                                           |
| bench_thread_pool        | 1.14 ms                                                      | 952 us: 1.20x faster                                                           |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                          |
| dulwich_log              | 81.1 ms                                                      | 68.2 ms: 1.19x faster                                                          |
| sympy_sum                | 193 ms                                                       | 165 ms: 1.17x faster                                                           |
| deepcopy_reduce          | 4.01 us                                                      | 3.45 us: 1.16x faster                                                          |
| dask                     | 472 ms                                                       | 407 ms: 1.16x faster                                                           |
| 2to3                     | 350 ms                                                       | 302 ms: 1.16x faster                                                           |
| sympy_str                | 360 ms                                                       | 311 ms: 1.16x faster                                                           |
| genshi_text              | 31.4 ms                                                      | 27.2 ms: 1.15x faster                                                          |
| sympy_expand             | 600 ms                                                       | 522 ms: 1.15x faster                                                           |
| mdp                      | 3.01 sec                                                     | 2.63 sec: 1.14x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 126 ms: 1.14x faster                                                           |
| nqueens                  | 115 ms                                                       | 101 ms: 1.14x faster                                                           |
| scimark_fft              | 361 ms                                                       | 322 ms: 1.12x faster                                                           |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.11x faster                                                          |
| async_generators         | 421 ms                                                       | 379 ms: 1.11x faster                                                           |
| regex_dna                | 261 ms                                                       | 238 ms: 1.10x faster                                                           |
| mypy2                    | 933 ms                                                       | 849 ms: 1.10x faster                                                           |
| sympy_integrate          | 28.2 ms                                                      | 25.7 ms: 1.10x faster                                                          |
| docutils                 | 3.41 sec                                                     | 3.12 sec: 1.10x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 147 ms: 1.09x faster                                                           |
| sqlglot_optimize         | 70.1 ms                                                      | 64.5 ms: 1.09x faster                                                          |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.09x faster                                                           |
| json                     | 5.86 ms                                                      | 5.41 ms: 1.08x faster                                                          |
| pathlib                  | 21.4 ms                                                      | 19.7 ms: 1.08x faster                                                          |
| xml_etree_generate       | 92.3 ms                                                      | 85.8 ms: 1.08x faster                                                          |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                          |
| genshi_xml               | 63.3 ms                                                      | 59.5 ms: 1.06x faster                                                          |
| gunicorn                 | 1.16 ms                                                      | 1.11 ms: 1.04x faster                                                          |
| aiohttp                  | 1.19 ms                                                      | 1.14 ms: 1.04x faster                                                          |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                           |
| meteor_contest           | 138 ms                                                       | 136 ms: 1.02x faster                                                           |
| unpickle_list            | 4.65 us                                                      | 4.61 us: 1.01x faster                                                          |
| create_gc_cycles         | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                          |
| pickle_list              | 4.12 us                                                      | 4.43 us: 1.07x slower                                                          |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.09x slower                                                          |
| unpickle                 | 13.5 us                                                      | 15.2 us: 1.13x slower                                                          |
| regex_effbot             | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                          |
| pickle_dict              | 29.5 us                                                      | 33.7 us: 1.14x slower                                                          |
| telco                    | 7.23 ms                                                      | 8.32 ms: 1.15x slower                                                          |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                          |
| gc_traversal             | 3.42 ms                                                      | 4.66 ms: 1.36x slower                                                          |
| coverage                 | 63.3 ms                                                      | 86.4 ms: 1.37x slower                                                          |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                          |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                   |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.20x