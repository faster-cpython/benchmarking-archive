# Results vs. 3.10.4

- fork: python
- ref: 434bc593df4c0274b8af
- machine: linux-x86_64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 298 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.72 ms: 1.22x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                       |
| html5lib       | 94.6 ms                                                      | 75.4 ms: 1.26x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 846 ms: 1.89x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 439 ms: 1.87x faster                                                         |
| async_tree_none         | 692 ms                                                       | 374 ms: 1.85x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 602 ms: 1.56x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.78x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.3 ms: 1.48x faster                                                        |
| nbody          | 134 ms                                                       | 96.3 ms: 1.39x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.29x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 147 ms: 1.29x faster                                                         |
| regex_dna      | 261 ms                                                       | 237 ms: 1.10x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.61 ms: 1.17x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 313 us: 1.45x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 225 us: 1.38x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| xml_etree_process    | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.2 us: 1.20x faster                                                        |
| xml_etree_generate   | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 148 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.08x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.61 us: 1.01x faster                                                        |
| pickle_dict          | 29.5 us                                                      | 30.6 us: 1.04x slower                                                        |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.45 us: 1.08x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| genshi_text    | 31.4 ms                                                      | 26.7 ms: 1.18x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 59.7 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                        | 1.22x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 128 us: 4.18x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.76 ms: 1.99x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 846 ms: 1.89x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 439 ms: 1.87x faster                                                         |
| async_tree_none          | 692 ms                                                       | 374 ms: 1.85x faster                                                         |
| raytrace                 | 489 ms                                                       | 272 ms: 1.80x faster                                                         |
| richards_super           | 90.6 ms                                                      | 51.9 ms: 1.74x faster                                                        |
| logging_silent           | 167 ns                                                       | 97.2 ns: 1.72x faster                                                        |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.72x faster                                                        |
| pylint                   | 566 ms                                                       | 334 ms: 1.70x faster                                                         |
| chaos                    | 109 ms                                                       | 64.6 ms: 1.68x faster                                                        |
| richards                 | 75.1 ms                                                      | 45.7 ms: 1.64x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.58x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 602 ms: 1.56x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 77.2 ms: 1.54x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 70.2 ms: 1.53x faster                                                        |
| go                       | 262 ms                                                       | 172 ms: 1.53x faster                                                         |
| spectral_norm            | 139 ms                                                       | 93.2 ms: 1.49x faster                                                        |
| float                    | 111 ms                                                       | 75.3 ms: 1.48x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.47x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| pyflate                  | 733 ms                                                       | 501 ms: 1.46x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 313 us: 1.45x faster                                                         |
| scimark_lu               | 167 ms                                                       | 119 ms: 1.40x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.34 us: 1.40x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.1 us: 1.40x faster                                                        |
| nbody                    | 134 ms                                                       | 96.3 ms: 1.39x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 225 us: 1.38x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.00 us: 1.38x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.1 ms: 1.37x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 4.68 ms: 1.36x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.25 sec: 1.33x faster                                                       |
| thrift                   | 1.18 ms                                                      | 885 us: 1.33x faster                                                         |
| hexiom                   | 9.42 ms                                                      | 7.15 ms: 1.32x faster                                                        |
| regex_compile            | 190 ms                                                       | 147 ms: 1.29x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.8 us: 1.28x faster                                                        |
| tornado_http             | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 834 ms: 1.26x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.71 sec: 1.26x faster                                                       |
| html5lib                 | 94.6 ms                                                      | 75.4 ms: 1.26x faster                                                        |
| fannkuch                 | 483 ms                                                       | 388 ms: 1.24x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.14 ms: 1.23x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.72 ms: 1.22x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 947 us: 1.20x faster                                                         |
| json_loads               | 30.3 us                                                      | 25.2 us: 1.20x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 67.8 ms: 1.20x faster                                                        |
| scimark_sor              | 180 ms                                                       | 151 ms: 1.19x faster                                                         |
| sympy_sum                | 193 ms                                                       | 163 ms: 1.19x faster                                                         |
| sympy_expand             | 600 ms                                                       | 507 ms: 1.18x faster                                                         |
| sympy_str                | 360 ms                                                       | 305 ms: 1.18x faster                                                         |
| dask                     | 472 ms                                                       | 400 ms: 1.18x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 26.7 ms: 1.18x faster                                                        |
| deepcopy                 | 468 us                                                       | 398 us: 1.18x faster                                                         |
| 2to3                     | 350 ms                                                       | 298 ms: 1.17x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.57 sec: 1.17x faster                                                       |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                         |
| scimark_fft              | 361 ms                                                       | 314 ms: 1.15x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.51 us: 1.14x faster                                                        |
| mypy2                    | 933 ms                                                       | 819 ms: 1.14x faster                                                         |
| nqueens                  | 115 ms                                                       | 102 ms: 1.13x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 25.2 ms: 1.12x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.69 us: 1.11x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 63.1 ms: 1.11x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                       |
| async_generators         | 421 ms                                                       | 380 ms: 1.11x faster                                                         |
| json                     | 5.86 ms                                                      | 5.30 ms: 1.11x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.3 ms: 1.10x faster                                                        |
| regex_dna                | 261 ms                                                       | 237 ms: 1.10x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 84.7 ms: 1.09x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 148 ms: 1.08x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.08x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 59.7 ms: 1.06x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.06x faster                                                        |
| meteor_contest           | 138 ms                                                       | 133 ms: 1.04x faster                                                         |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.61 us: 1.01x faster                                                        |
| pickle_dict              | 29.5 us                                                      | 30.6 us: 1.04x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.86 ms: 1.06x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.45 us: 1.08x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.22 ms: 1.14x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.61 ms: 1.17x slower                                                        |
| coverage                 | 63.3 ms                                                      | 81.6 ms: 1.29x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.58 ms: 1.34x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.27x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x