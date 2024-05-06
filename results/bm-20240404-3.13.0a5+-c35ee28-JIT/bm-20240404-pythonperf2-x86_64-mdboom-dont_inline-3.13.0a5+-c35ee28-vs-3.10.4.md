# Results vs. 3.10.4

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 298 ms: 1.17x faster                                                |
| chameleon      | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                               |
| docutils       | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                              |
| html5lib       | 94.6 ms                                                      | 72.5 ms: 1.31x faster                                               |
| tornado_http   | 157 ms                                                       | 122 ms: 1.29x faster                                                |
| Geometric mean | (ref)                                                        | 1.23x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|-------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 856 ms: 1.87x faster                                                |
| async_tree_memoization  | 819 ms                                                       | 447 ms: 1.83x faster                                                |
| async_tree_none         | 692 ms                                                       | 379 ms: 1.82x faster                                                |
| async_tree_cpu_io_mixed | 936 ms                                                       | 610 ms: 1.53x faster                                                |
| Geometric mean          | (ref)                                                        | 1.76x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.0 ms: 1.48x faster                                               |
| nbody          | 134 ms                                                       | 95.1 ms: 1.41x faster                                               |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| Geometric mean | (ref)                                                        | 1.29x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.28x faster                                                |
| regex_dna      | 261 ms                                                       | 241 ms: 1.09x faster                                                |
| regex_v8       | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                               |
| regex_effbot   | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                               |
| Geometric mean | (ref)                                                        | 1.06x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 309 us: 1.47x faster                                                |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                               |
| tomli_loads          | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                              |
| unpickle_pure_python | 312 us                                                       | 234 us: 1.33x faster                                                |
| xml_etree_process    | 75.9 ms                                                      | 57.9 ms: 1.31x faster                                               |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                               |
| xml_etree_generate   | 92.3 ms                                                      | 83.4 ms: 1.11x faster                                               |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.09x faster                                                |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.07x faster                                                |
| unpickle_list        | 4.65 us                                                      | 4.54 us: 1.02x faster                                               |
| pickle_list          | 4.12 us                                                      | 4.43 us: 1.07x slower                                               |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                               |
| pickle_dict          | 29.5 us                                                      | 32.7 us: 1.11x slower                                               |
| unpickle             | 13.5 us                                                      | 15.2 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                               |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                               |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 9.85 ms: 1.49x faster                                               |
| genshi_text    | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                               |
| genshi_xml     | 63.3 ms                                                      | 58.0 ms: 1.09x faster                                               |
| Geometric mean | (ref)                                                        | 1.25x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 120 us: 4.47x faster                                                |
| asyncio_tcp              | 779 ms                                                       | 370 ms: 2.10x faster                                                |
| deltablue                | 7.50 ms                                                      | 3.61 ms: 2.08x faster                                               |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                              |
| async_tree_io            | 1.60 sec                                                     | 856 ms: 1.87x faster                                                |
| async_tree_memoization   | 819 ms                                                       | 447 ms: 1.83x faster                                                |
| async_tree_none          | 692 ms                                                       | 379 ms: 1.82x faster                                                |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.72x faster                                               |
| logging_silent           | 167 ns                                                       | 97.8 ns: 1.71x faster                                               |
| chaos                    | 109 ms                                                       | 63.8 ms: 1.70x faster                                               |
| raytrace                 | 489 ms                                                       | 291 ms: 1.68x faster                                                |
| pylint                   | 566 ms                                                       | 338 ms: 1.67x faster                                                |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                               |
| richards_super           | 90.6 ms                                                      | 57.0 ms: 1.59x faster                                               |
| crypto_pyaes             | 119 ms                                                       | 76.7 ms: 1.55x faster                                               |
| scimark_monte_carlo      | 107 ms                                                       | 69.5 ms: 1.55x faster                                               |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 610 ms: 1.53x faster                                                |
| pyflate                  | 733 ms                                                       | 487 ms: 1.50x faster                                                |
| go                       | 262 ms                                                       | 175 ms: 1.50x faster                                                |
| mako                     | 14.7 ms                                                      | 9.85 ms: 1.49x faster                                               |
| spectral_norm            | 139 ms                                                       | 93.7 ms: 1.49x faster                                               |
| float                    | 111 ms                                                       | 75.0 ms: 1.48x faster                                               |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.48x faster                                               |
| richards                 | 75.1 ms                                                      | 50.8 ms: 1.48x faster                                               |
| pickle_pure_python       | 455 us                                                       | 309 us: 1.47x faster                                                |
| nbody                    | 134 ms                                                       | 95.1 ms: 1.41x faster                                               |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                               |
| comprehensions           | 26.7 us                                                      | 19.5 us: 1.37x faster                                               |
| logging_simple           | 8.88 us                                                      | 6.52 us: 1.36x faster                                               |
| logging_format           | 9.64 us                                                      | 7.15 us: 1.35x faster                                               |
| tomli_loads              | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                              |
| pycparser                | 1.67 sec                                                     | 1.24 sec: 1.35x faster                                              |
| scimark_lu               | 167 ms                                                       | 124 ms: 1.35x faster                                                |
| unpickle_pure_python     | 312 us                                                       | 234 us: 1.33x faster                                                |
| xml_etree_process        | 75.9 ms                                                      | 57.9 ms: 1.31x faster                                               |
| html5lib                 | 94.6 ms                                                      | 72.5 ms: 1.31x faster                                               |
| thrift                   | 1.18 ms                                                      | 902 us: 1.30x faster                                                |
| deepcopy_memo            | 49.8 us                                                      | 38.4 us: 1.30x faster                                               |
| coroutines               | 30.3 ms                                                      | 23.4 ms: 1.29x faster                                               |
| tornado_http             | 157 ms                                                       | 122 ms: 1.29x faster                                                |
| regex_compile            | 190 ms                                                       | 148 ms: 1.28x faster                                                |
| bench_mp_pool            | 6.37 ms                                                      | 5.00 ms: 1.27x faster                                               |
| hexiom                   | 9.42 ms                                                      | 7.39 ms: 1.27x faster                                               |
| chameleon                | 9.44 ms                                                      | 7.46 ms: 1.27x faster                                               |
| pprint_pformat           | 2.15 sec                                                     | 1.71 sec: 1.26x faster                                              |
| fannkuch                 | 483 ms                                                       | 384 ms: 1.26x faster                                                |
| pprint_safe_repr         | 1.05 sec                                                     | 836 ms: 1.26x faster                                                |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.13 ms: 1.23x faster                                               |
| deepcopy                 | 468 us                                                       | 390 us: 1.20x faster                                                |
| genshi_text              | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                               |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                               |
| scimark_sor              | 180 ms                                                       | 153 ms: 1.18x faster                                                |
| dulwich_log              | 81.1 ms                                                      | 68.7 ms: 1.18x faster                                               |
| sympy_str                | 360 ms                                                       | 305 ms: 1.18x faster                                                |
| 2to3                     | 350 ms                                                       | 298 ms: 1.17x faster                                                |
| dask                     | 472 ms                                                       | 403 ms: 1.17x faster                                                |
| sympy_sum                | 193 ms                                                       | 164 ms: 1.17x faster                                                |
| sympy_expand             | 600 ms                                                       | 513 ms: 1.17x faster                                                |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                |
| deepcopy_reduce          | 4.01 us                                                      | 3.43 us: 1.17x faster                                               |
| mdp                      | 3.01 sec                                                     | 2.59 sec: 1.16x faster                                              |
| scimark_fft              | 361 ms                                                       | 313 ms: 1.16x faster                                                |
| mypy2                    | 933 ms                                                       | 827 ms: 1.13x faster                                                |
| nqueens                  | 115 ms                                                       | 103 ms: 1.12x faster                                                |
| sqlglot_optimize         | 70.1 ms                                                      | 62.7 ms: 1.12x faster                                               |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.12x faster                                               |
| sympy_integrate          | 28.2 ms                                                      | 25.4 ms: 1.11x faster                                               |
| xml_etree_generate       | 92.3 ms                                                      | 83.4 ms: 1.11x faster                                               |
| docutils                 | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                              |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.09x faster                                                |
| pathlib                  | 21.4 ms                                                      | 19.5 ms: 1.09x faster                                               |
| genshi_xml               | 63.3 ms                                                      | 58.0 ms: 1.09x faster                                               |
| regex_dna                | 261 ms                                                       | 241 ms: 1.09x faster                                                |
| json                     | 5.86 ms                                                      | 5.47 ms: 1.07x faster                                               |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.07x faster                                                |
| async_generators         | 421 ms                                                       | 397 ms: 1.06x faster                                                |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.06x faster                                               |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.05x faster                                               |
| regex_v8                 | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                               |
| meteor_contest           | 138 ms                                                       | 133 ms: 1.04x faster                                                |
| bench_thread_pool        | 1.14 ms                                                      | 1.10 ms: 1.04x faster                                               |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                |
| unpickle_list            | 4.65 us                                                      | 4.54 us: 1.02x faster                                               |
| create_gc_cycles         | 1.76 ms                                                      | 1.86 ms: 1.06x slower                                               |
| pickle_list              | 4.12 us                                                      | 4.43 us: 1.07x slower                                               |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.08x slower                                               |
| telco                    | 7.23 ms                                                      | 8.01 ms: 1.11x slower                                               |
| pickle_dict              | 29.5 us                                                      | 32.7 us: 1.11x slower                                               |
| unpickle                 | 13.5 us                                                      | 15.2 us: 1.12x slower                                               |
| regex_effbot             | 3.09 ms                                                      | 3.52 ms: 1.14x slower                                               |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                               |
| gc_traversal             | 3.42 ms                                                      | 4.41 ms: 1.29x slower                                               |
| coverage                 | 63.3 ms                                                      | 86.4 ms: 1.37x slower                                               |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                               |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-c35ee28-JIT/bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.20x