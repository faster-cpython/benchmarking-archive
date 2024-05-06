# Results vs. 3.10.4

- fork: mdboom
- ref: all_above_200
- machine: linux-x86_64
- commit hash: d42ae28
- commit date: 2024-04-03
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 302 ms: 1.16x faster                                                  |
| chameleon      | 9.44 ms                                                      | 7.31 ms: 1.29x faster                                                 |
| docutils       | 3.41 sec                                                     | 3.06 sec: 1.11x faster                                                |
| html5lib       | 94.6 ms                                                      | 72.5 ms: 1.31x faster                                                 |
| tornado_http   | 157 ms                                                       | 124 ms: 1.27x faster                                                  |
| Geometric mean | (ref)                                                        | 1.23x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 377 ms: 1.83x faster                                                  |
| async_tree_memoization  | 819 ms                                                       | 452 ms: 1.81x faster                                                  |
| async_tree_io           | 1.60 sec                                                     | 906 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed | 936 ms                                                       | 602 ms: 1.55x faster                                                  |
| Geometric mean          | (ref)                                                        | 1.74x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 111 ms                                                       | 77.7 ms: 1.43x faster                                                 |
| nbody          | 134 ms                                                       | 94.7 ms: 1.42x faster                                                 |
| pidigits       | 271 ms                                                       | 264 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 150 ms: 1.27x faster                                                  |
| regex_dna      | 261 ms                                                       | 247 ms: 1.06x faster                                                  |
| regex_v8       | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                 |
| regex_effbot   | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 310 us: 1.47x faster                                                  |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                 |
| tomli_loads          | 2.92 sec                                                     | 2.21 sec: 1.32x faster                                                |
| unpickle_pure_python | 312 us                                                       | 241 us: 1.30x faster                                                  |
| xml_etree_process    | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                 |
| json_loads           | 30.3 us                                                      | 25.8 us: 1.18x faster                                                 |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.10x faster                                                  |
| xml_etree_generate   | 92.3 ms                                                      | 85.5 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.06x faster                                                  |
| unpickle_list        | 4.65 us                                                      | 4.60 us: 1.01x faster                                                 |
| pickle_list          | 4.12 us                                                      | 4.45 us: 1.08x slower                                                 |
| unpickle             | 13.5 us                                                      | 14.6 us: 1.08x slower                                                 |
| pickle_dict          | 29.5 us                                                      | 33.1 us: 1.12x slower                                                 |
| pickle               | 9.89 us                                                      | 11.1 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.6 ms: 1.18x slower                                                 |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.84 ms: 1.49x faster                                                 |
| django_template | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                                 |
| genshi_text     | 31.4 ms                                                      | 27.7 ms: 1.13x faster                                                 |
| genshi_xml      | 63.3 ms                                                      | 62.7 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.21x faster                                                          |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 123 us: 4.37x faster                                                  |
| asyncio_tcp              | 779 ms                                                       | 369 ms: 2.11x faster                                                  |
| deltablue                | 7.50 ms                                                      | 3.77 ms: 1.99x faster                                                 |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                |
| async_tree_none          | 692 ms                                                       | 377 ms: 1.83x faster                                                  |
| async_tree_memoization   | 819 ms                                                       | 452 ms: 1.81x faster                                                  |
| async_tree_io            | 1.60 sec                                                     | 906 ms: 1.76x faster                                                  |
| logging_silent           | 167 ns                                                       | 97.3 ns: 1.72x faster                                                 |
| generators               | 57.3 ms                                                      | 34.4 ms: 1.67x faster                                                 |
| chaos                    | 109 ms                                                       | 67.7 ms: 1.60x faster                                                 |
| raytrace                 | 489 ms                                                       | 309 ms: 1.58x faster                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.58x faster                                                 |
| pylint                   | 566 ms                                                       | 364 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 602 ms: 1.55x faster                                                  |
| richards_super           | 90.6 ms                                                      | 58.9 ms: 1.54x faster                                                 |
| crypto_pyaes             | 119 ms                                                       | 77.9 ms: 1.53x faster                                                 |
| mako                     | 14.7 ms                                                      | 9.84 ms: 1.49x faster                                                 |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.48x faster                                                 |
| go                       | 262 ms                                                       | 178 ms: 1.47x faster                                                  |
| pickle_pure_python       | 455 us                                                       | 310 us: 1.47x faster                                                  |
| richards                 | 75.1 ms                                                      | 51.2 ms: 1.47x faster                                                 |
| scimark_monte_carlo      | 107 ms                                                       | 73.7 ms: 1.46x faster                                                 |
| pyflate                  | 733 ms                                                       | 506 ms: 1.45x faster                                                  |
| spectral_norm            | 139 ms                                                       | 96.2 ms: 1.45x faster                                                 |
| float                    | 111 ms                                                       | 77.7 ms: 1.43x faster                                                 |
| nbody                    | 134 ms                                                       | 94.7 ms: 1.42x faster                                                 |
| scimark_lu               | 167 ms                                                       | 120 ms: 1.39x faster                                                  |
| thrift                   | 1.18 ms                                                      | 845 us: 1.39x faster                                                  |
| comprehensions           | 26.7 us                                                      | 19.5 us: 1.37x faster                                                 |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                 |
| coroutines               | 30.3 ms                                                      | 22.5 ms: 1.35x faster                                                 |
| logging_simple           | 8.88 us                                                      | 6.73 us: 1.32x faster                                                 |
| logging_format           | 9.64 us                                                      | 7.31 us: 1.32x faster                                                 |
| tomli_loads              | 2.92 sec                                                     | 2.21 sec: 1.32x faster                                                |
| html5lib                 | 94.6 ms                                                      | 72.5 ms: 1.31x faster                                                 |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                                |
| unpickle_pure_python     | 312 us                                                       | 241 us: 1.30x faster                                                  |
| chameleon                | 9.44 ms                                                      | 7.31 ms: 1.29x faster                                                 |
| xml_etree_process        | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                 |
| bench_mp_pool            | 6.37 ms                                                      | 4.98 ms: 1.28x faster                                                 |
| regex_compile            | 190 ms                                                       | 150 ms: 1.27x faster                                                  |
| tornado_http             | 157 ms                                                       | 124 ms: 1.27x faster                                                  |
| pprint_safe_repr         | 1.05 sec                                                     | 828 ms: 1.27x faster                                                  |
| pprint_pformat           | 2.15 sec                                                     | 1.70 sec: 1.27x faster                                                |
| deepcopy_memo            | 49.8 us                                                      | 39.6 us: 1.26x faster                                                 |
| django_template          | 50.2 ms                                                      | 40.1 ms: 1.25x faster                                                 |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.14 ms: 1.23x faster                                                 |
| hexiom                   | 9.42 ms                                                      | 7.70 ms: 1.22x faster                                                 |
| fannkuch                 | 483 ms                                                       | 396 ms: 1.22x faster                                                  |
| deepcopy                 | 468 us                                                       | 391 us: 1.20x faster                                                  |
| sympy_sum                | 193 ms                                                       | 161 ms: 1.19x faster                                                  |
| sympy_str                | 360 ms                                                       | 304 ms: 1.19x faster                                                  |
| scimark_sor              | 180 ms                                                       | 153 ms: 1.18x faster                                                  |
| deepcopy_reduce          | 4.01 us                                                      | 3.41 us: 1.18x faster                                                 |
| json_loads               | 30.3 us                                                      | 25.8 us: 1.18x faster                                                 |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                  |
| sympy_expand             | 600 ms                                                       | 512 ms: 1.17x faster                                                  |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                  |
| dulwich_log              | 81.1 ms                                                      | 69.9 ms: 1.16x faster                                                 |
| 2to3                     | 350 ms                                                       | 302 ms: 1.16x faster                                                  |
| scimark_fft              | 361 ms                                                       | 314 ms: 1.15x faster                                                  |
| mdp                      | 3.01 sec                                                     | 2.63 sec: 1.14x faster                                                |
| genshi_text              | 31.4 ms                                                      | 27.7 ms: 1.13x faster                                                 |
| mypy2                    | 933 ms                                                       | 826 ms: 1.13x faster                                                  |
| sympy_integrate          | 28.2 ms                                                      | 25.1 ms: 1.12x faster                                                 |
| docutils                 | 3.41 sec                                                     | 3.06 sec: 1.11x faster                                                |
| sqlglot_optimize         | 70.1 ms                                                      | 62.9 ms: 1.11x faster                                                 |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                                 |
| pathlib                  | 21.4 ms                                                      | 19.3 ms: 1.10x faster                                                 |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.10x faster                                                  |
| nqueens                  | 115 ms                                                       | 105 ms: 1.09x faster                                                  |
| json                     | 5.86 ms                                                      | 5.42 ms: 1.08x faster                                                 |
| xml_etree_generate       | 92.3 ms                                                      | 85.5 ms: 1.08x faster                                                 |
| aiohttp                  | 1.19 ms                                                      | 1.11 ms: 1.07x faster                                                 |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.06x faster                                                  |
| regex_dna                | 261 ms                                                       | 247 ms: 1.06x faster                                                  |
| async_generators         | 421 ms                                                       | 398 ms: 1.06x faster                                                  |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.06x faster                                                 |
| regex_v8                 | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                 |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                  |
| pidigits                 | 271 ms                                                       | 264 ms: 1.03x faster                                                  |
| bench_thread_pool        | 1.14 ms                                                      | 1.12 ms: 1.02x faster                                                 |
| unpickle_list            | 4.65 us                                                      | 4.60 us: 1.01x faster                                                 |
| genshi_xml               | 63.3 ms                                                      | 62.7 ms: 1.01x faster                                                 |
| asyncio_websockets       | 390 ms                                                       | 387 ms: 1.01x faster                                                  |
| create_gc_cycles         | 1.76 ms                                                      | 1.81 ms: 1.03x slower                                                 |
| pickle_list              | 4.12 us                                                      | 4.45 us: 1.08x slower                                                 |
| unpickle                 | 13.5 us                                                      | 14.6 us: 1.08x slower                                                 |
| pickle_dict              | 29.5 us                                                      | 33.1 us: 1.12x slower                                                 |
| pickle                   | 9.89 us                                                      | 11.1 us: 1.12x slower                                                 |
| telco                    | 7.23 ms                                                      | 8.19 ms: 1.13x slower                                                 |
| regex_effbot             | 3.09 ms                                                      | 3.50 ms: 1.13x slower                                                 |
| python_startup           | 11.5 ms                                                      | 13.6 ms: 1.18x slower                                                 |
| coverage                 | 63.3 ms                                                      | 81.6 ms: 1.29x slower                                                 |
| gc_traversal             | 3.42 ms                                                      | 4.85 ms: 1.42x slower                                                 |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.24x faster                                                          |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-d42ae28-JIT/bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x