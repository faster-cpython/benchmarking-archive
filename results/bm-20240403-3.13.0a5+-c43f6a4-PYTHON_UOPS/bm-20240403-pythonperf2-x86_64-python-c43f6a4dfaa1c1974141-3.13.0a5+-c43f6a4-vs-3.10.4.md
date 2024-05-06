# Results vs. 3.10.4

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: linux-x86_64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.14x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 320 ms: 1.09x faster                                                         |
| chameleon      | 9.44 ms                                                      | 8.00 ms: 1.18x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.29 sec: 1.04x faster                                                       |
| html5lib       | 94.6 ms                                                      | 79.1 ms: 1.20x faster                                                        |
| tornado_http   | 157 ms                                                       | 128 ms: 1.23x faster                                                         |
| Geometric mean | (ref)                                                        | 1.14x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization  | 819 ms                                                       | 459 ms: 1.78x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 905 ms: 1.77x faster                                                         |
| async_tree_none         | 692 ms                                                       | 394 ms: 1.76x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 623 ms: 1.50x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.70x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 101 ms: 1.11x faster                                                         |
| nbody          | 134 ms                                                       | 130 ms: 1.03x faster                                                         |
| pidigits       | 271 ms                                                       | 265 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 261 ms                                                       | 239 ms: 1.09x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 26.6 ms: 1.02x faster                                                        |
| regex_compile  | 190 ms                                                       | 208 ms: 1.10x slower                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 324 us: 1.40x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.2 us: 1.20x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 64.6 ms: 1.18x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 147 ms: 1.09x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.89 sec: 1.01x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 310 us: 1.01x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 93.8 ms: 1.02x slower                                                        |
| unpickle_list        | 4.65 us                                                      | 4.77 us: 1.03x slower                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 114 ms: 1.03x slower                                                         |
| pickle_list          | 4.12 us                                                      | 4.46 us: 1.08x slower                                                        |
| pickle               | 9.89 us                                                      | 10.8 us: 1.10x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 32.7 us: 1.11x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.2 ms: 1.53x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text    | 31.4 ms                                                      | 27.9 ms: 1.13x faster                                                        |
| mako           | 14.7 ms                                                      | 14.0 ms: 1.05x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 62.2 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 126 us: 4.26x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 379 ms: 2.06x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.60 sec: 1.94x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.97 ms: 1.89x faster                                                        |
| async_tree_memoization   | 819 ms                                                       | 459 ms: 1.78x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 905 ms: 1.77x faster                                                         |
| async_tree_none          | 692 ms                                                       | 394 ms: 1.76x faster                                                         |
| generators               | 57.3 ms                                                      | 33.0 ms: 1.74x faster                                                        |
| logging_silent           | 167 ns                                                       | 99.4 ns: 1.68x faster                                                        |
| pylint                   | 566 ms                                                       | 346 ms: 1.63x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 623 ms: 1.50x faster                                                         |
| raytrace                 | 489 ms                                                       | 336 ms: 1.45x faster                                                         |
| chaos                    | 109 ms                                                       | 75.9 ms: 1.43x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.57 ms: 1.42x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 324 us: 1.40x faster                                                         |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.3 ms: 1.36x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.99 ms: 1.35x faster                                                        |
| richards_super           | 90.6 ms                                                      | 67.4 ms: 1.34x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.63 us: 1.34x faster                                                        |
| thrift                   | 1.18 ms                                                      | 893 us: 1.32x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.33 us: 1.32x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 92.2 ms: 1.29x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.97 ms: 1.28x faster                                                        |
| go                       | 262 ms                                                       | 205 ms: 1.28x faster                                                         |
| richards                 | 75.1 ms                                                      | 61.0 ms: 1.23x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.36 sec: 1.23x faster                                                       |
| tornado_http             | 157 ms                                                       | 128 ms: 1.23x faster                                                         |
| json_loads               | 30.3 us                                                      | 25.2 us: 1.20x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 79.1 ms: 1.20x faster                                                        |
| chameleon                | 9.44 ms                                                      | 8.00 ms: 1.18x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 64.6 ms: 1.18x faster                                                        |
| dask                     | 472 ms                                                       | 416 ms: 1.13x faster                                                         |
| pyflate                  | 733 ms                                                       | 649 ms: 1.13x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 27.9 ms: 1.13x faster                                                        |
| deepcopy                 | 468 us                                                       | 417 us: 1.12x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.68 sec: 1.12x faster                                                       |
| scimark_lu               | 167 ms                                                       | 149 ms: 1.12x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.59 us: 1.12x faster                                                        |
| sqlglot_normalize        | 144 ms                                                       | 130 ms: 1.11x faster                                                         |
| float                    | 111 ms                                                       | 101 ms: 1.11x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 45.1 us: 1.10x faster                                                        |
| 2to3                     | 350 ms                                                       | 320 ms: 1.09x faster                                                         |
| regex_dna                | 261 ms                                                       | 239 ms: 1.09x faster                                                         |
| json                     | 5.86 ms                                                      | 5.38 ms: 1.09x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 147 ms: 1.09x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 99.0 ms: 1.09x faster                                                        |
| mypy2                    | 933 ms                                                       | 862 ms: 1.08x faster                                                         |
| async_generators         | 421 ms                                                       | 391 ms: 1.08x faster                                                         |
| sympy_sum                | 193 ms                                                       | 180 ms: 1.07x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 2.01 sec: 1.07x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 983 ms: 1.07x faster                                                         |
| pathlib                  | 21.4 ms                                                      | 20.3 ms: 1.05x faster                                                        |
| mako                     | 14.7 ms                                                      | 14.0 ms: 1.05x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                        |
| scimark_sor              | 180 ms                                                       | 172 ms: 1.05x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 26.9 ms: 1.05x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.87 us: 1.04x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 77.8 ms: 1.04x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 67.5 ms: 1.04x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.04x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.29 sec: 1.04x faster                                                       |
| nbody                    | 134 ms                                                       | 130 ms: 1.03x faster                                                         |
| sympy_str                | 360 ms                                                       | 350 ms: 1.03x faster                                                         |
| sympy_expand             | 600 ms                                                       | 584 ms: 1.03x faster                                                         |
| pidigits                 | 271 ms                                                       | 265 ms: 1.02x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 26.6 ms: 1.02x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 62.2 ms: 1.02x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.89 sec: 1.01x faster                                                       |
| unpickle_pure_python     | 312 us                                                       | 310 us: 1.01x faster                                                         |
| asyncio_websockets       | 390 ms                                                       | 395 ms: 1.01x slower                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 93.8 ms: 1.02x slower                                                        |
| unpickle_list            | 4.65 us                                                      | 4.77 us: 1.03x slower                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 114 ms: 1.03x slower                                                         |
| meteor_contest           | 138 ms                                                       | 143 ms: 1.03x slower                                                         |
| nqueens                  | 115 ms                                                       | 122 ms: 1.06x slower                                                         |
| fannkuch                 | 483 ms                                                       | 520 ms: 1.08x slower                                                         |
| pickle_list              | 4.12 us                                                      | 4.46 us: 1.08x slower                                                        |
| regex_compile            | 190 ms                                                       | 208 ms: 1.10x slower                                                         |
| pickle                   | 9.89 us                                                      | 10.8 us: 1.10x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.94 ms: 1.10x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 32.7 us: 1.11x slower                                                        |
| spectral_norm            | 139 ms                                                       | 154 ms: 1.11x slower                                                         |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.29 ms: 1.15x slower                                                        |
| hexiom                   | 9.42 ms                                                      | 10.8 ms: 1.15x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                        |
| scimark_fft              | 361 ms                                                       | 437 ms: 1.21x slower                                                         |
| gc_traversal             | 3.42 ms                                                      | 4.35 ms: 1.27x slower                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 6.68 ms: 1.32x slower                                                        |
| coverage                 | 63.3 ms                                                      | 87.6 ms: 1.38x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.2 ms: 1.53x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.14x faster                                                                 |

Benchmark hidden because not significant (2): bench_thread_pool, comprehensions
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-c43f6a4-PYTHON_UOPS/bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x