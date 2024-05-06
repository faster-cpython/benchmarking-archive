# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 306 ms: 1.15x faster                                                           |
| chameleon      | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                          |
| docutils       | 3.41 sec                                                     | 3.13 sec: 1.09x faster                                                         |
| html5lib       | 94.6 ms                                                      | 74.3 ms: 1.27x faster                                                          |
| tornado_http   | 157 ms                                                       | 124 ms: 1.27x faster                                                           |
| Geometric mean | (ref)                                                        | 1.20x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 362 ms: 1.91x faster                                                           |
| async_tree_memoization  | 819 ms                                                       | 445 ms: 1.84x faster                                                           |
| async_tree_io           | 1.60 sec                                                     | 891 ms: 1.79x faster                                                           |
| async_tree_cpu_io_mixed | 936 ms                                                       | 601 ms: 1.56x faster                                                           |
| Geometric mean          | (ref)                                                        | 1.77x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 79.0 ms: 1.41x faster                                                          |
| nbody          | 134 ms                                                       | 96.8 ms: 1.39x faster                                                          |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                        | 1.26x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 146 ms: 1.30x faster                                                           |
| regex_dna      | 261 ms                                                       | 240 ms: 1.09x faster                                                           |
| regex_v8       | 27.2 ms                                                      | 25.7 ms: 1.05x faster                                                          |
| regex_effbot   | 3.09 ms                                                      | 3.60 ms: 1.17x slower                                                          |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 308 us: 1.48x faster                                                           |
| unpickle_pure_python | 312 us                                                       | 230 us: 1.36x faster                                                           |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.35x faster                                                          |
| tomli_loads          | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                                          |
| json_loads           | 30.3 us                                                      | 25.4 us: 1.19x faster                                                          |
| xml_etree_parse      | 160 ms                                                       | 142 ms: 1.13x faster                                                           |
| xml_etree_generate   | 92.3 ms                                                      | 82.7 ms: 1.12x faster                                                          |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.09x faster                                                           |
| unpickle_list        | 4.65 us                                                      | 4.61 us: 1.01x faster                                                          |
| pickle_list          | 4.12 us                                                      | 4.50 us: 1.09x slower                                                          |
| pickle               | 9.89 us                                                      | 11.0 us: 1.12x slower                                                          |
| pickle_dict          | 29.5 us                                                      | 33.0 us: 1.12x slower                                                          |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                          |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                          |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.90 ms: 1.49x faster                                                          |
| django_template | 50.2 ms                                                      | 40.9 ms: 1.23x faster                                                          |
| genshi_text     | 31.4 ms                                                      | 28.0 ms: 1.12x faster                                                          |
| genshi_xml      | 63.3 ms                                                      | 59.9 ms: 1.06x faster                                                          |
| Geometric mean  | (ref)                                                        | 1.21x faster                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 123 us: 4.38x faster                                                           |
| asyncio_tcp              | 779 ms                                                       | 375 ms: 2.08x faster                                                           |
| deltablue                | 7.50 ms                                                      | 3.79 ms: 1.98x faster                                                          |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                         |
| async_tree_none          | 692 ms                                                       | 362 ms: 1.91x faster                                                           |
| async_tree_memoization   | 819 ms                                                       | 445 ms: 1.84x faster                                                           |
| async_tree_io            | 1.60 sec                                                     | 891 ms: 1.79x faster                                                           |
| logging_silent           | 167 ns                                                       | 97.7 ns: 1.71x faster                                                          |
| generators               | 57.3 ms                                                      | 33.5 ms: 1.71x faster                                                          |
| pylint                   | 566 ms                                                       | 345 ms: 1.64x faster                                                           |
| chaos                    | 109 ms                                                       | 69.0 ms: 1.57x faster                                                          |
| richards_super           | 90.6 ms                                                      | 57.6 ms: 1.57x faster                                                          |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.57x faster                                                          |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 601 ms: 1.56x faster                                                           |
| raytrace                 | 489 ms                                                       | 316 ms: 1.55x faster                                                           |
| crypto_pyaes             | 119 ms                                                       | 79.1 ms: 1.51x faster                                                          |
| richards                 | 75.1 ms                                                      | 50.5 ms: 1.49x faster                                                          |
| mako                     | 14.7 ms                                                      | 9.90 ms: 1.49x faster                                                          |
| spectral_norm            | 139 ms                                                       | 94.0 ms: 1.48x faster                                                          |
| pickle_pure_python       | 455 us                                                       | 308 us: 1.48x faster                                                           |
| go                       | 262 ms                                                       | 177 ms: 1.48x faster                                                           |
| sqlglot_transpile        | 2.68 ms                                                      | 1.84 ms: 1.46x faster                                                          |
| scimark_monte_carlo      | 107 ms                                                       | 75.9 ms: 1.41x faster                                                          |
| float                    | 111 ms                                                       | 79.0 ms: 1.41x faster                                                          |
| scimark_lu               | 167 ms                                                       | 119 ms: 1.40x faster                                                           |
| pyflate                  | 733 ms                                                       | 528 ms: 1.39x faster                                                           |
| nbody                    | 134 ms                                                       | 96.8 ms: 1.39x faster                                                          |
| coroutines               | 30.3 ms                                                      | 22.2 ms: 1.37x faster                                                          |
| unpickle_pure_python     | 312 us                                                       | 230 us: 1.36x faster                                                           |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.35x faster                                                          |
| tomli_loads              | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                         |
| thrift                   | 1.18 ms                                                      | 878 us: 1.34x faster                                                           |
| logging_simple           | 8.88 us                                                      | 6.63 us: 1.34x faster                                                          |
| comprehensions           | 26.7 us                                                      | 20.2 us: 1.32x faster                                                          |
| logging_format           | 9.64 us                                                      | 7.32 us: 1.32x faster                                                          |
| regex_compile            | 190 ms                                                       | 146 ms: 1.30x faster                                                           |
| xml_etree_process        | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                                          |
| deepcopy_memo            | 49.8 us                                                      | 38.4 us: 1.30x faster                                                          |
| pycparser                | 1.67 sec                                                     | 1.29 sec: 1.29x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 74.3 ms: 1.27x faster                                                          |
| bench_mp_pool            | 6.37 ms                                                      | 5.01 ms: 1.27x faster                                                          |
| tornado_http             | 157 ms                                                       | 124 ms: 1.27x faster                                                           |
| fannkuch                 | 483 ms                                                       | 383 ms: 1.26x faster                                                           |
| pprint_safe_repr         | 1.05 sec                                                     | 836 ms: 1.26x faster                                                           |
| chameleon                | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                          |
| pprint_pformat           | 2.15 sec                                                     | 1.73 sec: 1.25x faster                                                         |
| django_template          | 50.2 ms                                                      | 40.9 ms: 1.23x faster                                                          |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.14 ms: 1.23x faster                                                          |
| hexiom                   | 9.42 ms                                                      | 7.73 ms: 1.22x faster                                                          |
| json_loads               | 30.3 us                                                      | 25.4 us: 1.19x faster                                                          |
| dulwich_log              | 81.1 ms                                                      | 68.9 ms: 1.18x faster                                                          |
| sympy_sum                | 193 ms                                                       | 165 ms: 1.17x faster                                                           |
| deepcopy                 | 468 us                                                       | 401 us: 1.17x faster                                                           |
| sympy_str                | 360 ms                                                       | 310 ms: 1.16x faster                                                           |
| dask                     | 472 ms                                                       | 407 ms: 1.16x faster                                                           |
| scimark_sor              | 180 ms                                                       | 156 ms: 1.16x faster                                                           |
| 2to3                     | 350 ms                                                       | 306 ms: 1.15x faster                                                           |
| scimark_fft              | 361 ms                                                       | 317 ms: 1.14x faster                                                           |
| sympy_expand             | 600 ms                                                       | 526 ms: 1.14x faster                                                           |
| deepcopy_reduce          | 4.01 us                                                      | 3.52 us: 1.14x faster                                                          |
| mdp                      | 3.01 sec                                                     | 2.65 sec: 1.13x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 127 ms: 1.13x faster                                                           |
| xml_etree_parse          | 160 ms                                                       | 142 ms: 1.13x faster                                                           |
| genshi_text              | 31.4 ms                                                      | 28.0 ms: 1.12x faster                                                          |
| xml_etree_generate       | 92.3 ms                                                      | 82.7 ms: 1.12x faster                                                          |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                                          |
| mypy2                    | 933 ms                                                       | 852 ms: 1.10x faster                                                           |
| docutils                 | 3.41 sec                                                     | 3.13 sec: 1.09x faster                                                         |
| regex_dna                | 261 ms                                                       | 240 ms: 1.09x faster                                                           |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.09x faster                                                           |
| nqueens                  | 115 ms                                                       | 106 ms: 1.08x faster                                                           |
| sqlglot_optimize         | 70.1 ms                                                      | 64.7 ms: 1.08x faster                                                          |
| sympy_integrate          | 28.2 ms                                                      | 26.1 ms: 1.08x faster                                                          |
| pathlib                  | 21.4 ms                                                      | 19.8 ms: 1.08x faster                                                          |
| async_generators         | 421 ms                                                       | 393 ms: 1.07x faster                                                           |
| json                     | 5.86 ms                                                      | 5.51 ms: 1.06x faster                                                          |
| genshi_xml               | 63.3 ms                                                      | 59.9 ms: 1.06x faster                                                          |
| regex_v8                 | 27.2 ms                                                      | 25.7 ms: 1.05x faster                                                          |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                           |
| aiohttp                  | 1.19 ms                                                      | 1.15 ms: 1.04x faster                                                          |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.03x faster                                                          |
| meteor_contest           | 138 ms                                                       | 135 ms: 1.03x faster                                                           |
| asyncio_websockets       | 390 ms                                                       | 384 ms: 1.02x faster                                                           |
| unpickle_list            | 4.65 us                                                      | 4.61 us: 1.01x faster                                                          |
| unpack_sequence          | 59.9 ns                                                      | 59.5 ns: 1.01x faster                                                          |
| create_gc_cycles         | 1.76 ms                                                      | 1.81 ms: 1.03x slower                                                          |
| pickle_list              | 4.12 us                                                      | 4.50 us: 1.09x slower                                                          |
| pickle                   | 9.89 us                                                      | 11.0 us: 1.12x slower                                                          |
| pickle_dict              | 29.5 us                                                      | 33.0 us: 1.12x slower                                                          |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                          |
| telco                    | 7.23 ms                                                      | 8.11 ms: 1.12x slower                                                          |
| regex_effbot             | 3.09 ms                                                      | 3.60 ms: 1.17x slower                                                          |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                          |
| gc_traversal             | 3.42 ms                                                      | 4.35 ms: 1.27x slower                                                          |
| coverage                 | 63.3 ms                                                      | 84.3 ms: 1.33x slower                                                          |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                          |
| Geometric mean           | (ref)                                                        | 1.24x faster                                                                   |

Benchmark hidden because not significant (1): bench_thread_pool
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.21x