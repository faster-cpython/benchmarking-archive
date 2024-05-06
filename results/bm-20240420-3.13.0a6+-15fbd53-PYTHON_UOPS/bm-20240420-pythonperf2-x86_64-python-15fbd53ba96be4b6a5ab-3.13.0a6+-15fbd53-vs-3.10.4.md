# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 314 ms: 1.12x faster                                                         |
| chameleon      | 9.44 ms                                                      | 8.34 ms: 1.13x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.24 sec: 1.05x faster                                                       |
| html5lib       | 94.6 ms                                                      | 79.0 ms: 1.20x faster                                                        |
| tornado_http   | 157 ms                                                       | 127 ms: 1.24x faster                                                         |
| Geometric mean | (ref)                                                        | 1.15x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 384 ms: 1.80x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 919 ms: 1.74x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 478 ms: 1.72x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 631 ms: 1.48x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.68x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 84.7 ms: 1.31x faster                                                        |
| nbody          | 134 ms                                                       | 110 ms: 1.22x faster                                                         |
| pidigits       | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.18x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                        |
| regex_compile  | 190 ms                                                       | 194 ms: 1.02x slower                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.63 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 320 us: 1.42x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 61.2 ms: 1.24x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.5 us: 1.24x faster                                                        |
| unpickle_pure_python | 312 us                                                       | 283 us: 1.10x faster                                                         |
| xml_etree_parse      | 160 ms                                                       | 149 ms: 1.08x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.73 sec: 1.07x faster                                                       |
| xml_etree_generate   | 92.3 ms                                                      | 88.5 ms: 1.04x faster                                                        |
| unpickle_list        | 4.65 us                                                      | 4.58 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 110 ms: 1.01x faster                                                         |
| pickle_dict          | 29.5 us                                                      | 30.6 us: 1.04x slower                                                        |
| pickle               | 9.89 us                                                      | 10.4 us: 1.06x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.52 us: 1.10x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 8.90 ms: 1.21x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 50.2 ms                                                      | 41.5 ms: 1.21x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 27.5 ms: 1.14x faster                                                        |
| mako            | 14.7 ms                                                      | 13.0 ms: 1.13x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 60.2 ms: 1.05x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.13x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 126 us: 4.26x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 378 ms: 2.06x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.60 sec: 1.94x faster                                                       |
| deltablue                | 7.50 ms                                                      | 4.12 ms: 1.82x faster                                                        |
| async_tree_none          | 692 ms                                                       | 384 ms: 1.80x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 919 ms: 1.74x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 478 ms: 1.72x faster                                                         |
| logging_silent           | 167 ns                                                       | 98.1 ns: 1.71x faster                                                        |
| generators               | 57.3 ms                                                      | 34.0 ms: 1.69x faster                                                        |
| raytrace                 | 489 ms                                                       | 299 ms: 1.64x faster                                                         |
| pylint                   | 566 ms                                                       | 370 ms: 1.53x faster                                                         |
| richards_super           | 90.6 ms                                                      | 59.6 ms: 1.52x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 631 ms: 1.48x faster                                                         |
| chaos                    | 109 ms                                                       | 73.3 ms: 1.48x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.55 ms: 1.44x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 320 us: 1.42x faster                                                         |
| richards                 | 75.1 ms                                                      | 53.3 ms: 1.41x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 85.5 ms: 1.39x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.95 ms: 1.38x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.2 ms: 1.37x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.73 ms: 1.35x faster                                                        |
| float                    | 111 ms                                                       | 84.7 ms: 1.31x faster                                                        |
| thrift                   | 1.18 ms                                                      | 899 us: 1.31x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.86 us: 1.29x faster                                                        |
| go                       | 262 ms                                                       | 204 ms: 1.28x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.55 us: 1.28x faster                                                        |
| pyflate                  | 733 ms                                                       | 587 ms: 1.25x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.34 sec: 1.25x faster                                                       |
| xml_etree_process        | 75.9 ms                                                      | 61.2 ms: 1.24x faster                                                        |
| json_loads               | 30.3 us                                                      | 24.5 us: 1.24x faster                                                        |
| tornado_http             | 157 ms                                                       | 127 ms: 1.24x faster                                                         |
| nbody                    | 134 ms                                                       | 110 ms: 1.22x faster                                                         |
| django_template          | 50.2 ms                                                      | 41.5 ms: 1.21x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 41.4 us: 1.20x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 17.8 ms: 1.20x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 79.0 ms: 1.20x faster                                                        |
| scimark_lu               | 167 ms                                                       | 140 ms: 1.19x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 90.3 ms: 1.19x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 965 us: 1.18x faster                                                         |
| deepcopy                 | 468 us                                                       | 404 us: 1.16x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.47 us: 1.16x faster                                                        |
| dask                     | 472 ms                                                       | 410 ms: 1.15x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 27.5 ms: 1.14x faster                                                        |
| mdp                      | 3.01 sec                                                     | 2.63 sec: 1.14x faster                                                       |
| scimark_sor              | 180 ms                                                       | 159 ms: 1.14x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 127 ms: 1.13x faster                                                         |
| chameleon                | 9.44 ms                                                      | 8.34 ms: 1.13x faster                                                        |
| mako                     | 14.7 ms                                                      | 13.0 ms: 1.13x faster                                                        |
| 2to3                     | 350 ms                                                       | 314 ms: 1.12x faster                                                         |
| comprehensions           | 26.7 us                                                      | 23.9 us: 1.12x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 283 us: 1.10x faster                                                         |
| mypy2                    | 933 ms                                                       | 846 ms: 1.10x faster                                                         |
| json                     | 5.86 ms                                                      | 5.39 ms: 1.09x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 74.8 ms: 1.08x faster                                                        |
| sympy_sum                | 193 ms                                                       | 178 ms: 1.08x faster                                                         |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 149 ms: 1.08x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 26.2 ms: 1.07x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 2.01 sec: 1.07x faster                                                       |
| async_generators         | 421 ms                                                       | 392 ms: 1.07x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 981 ms: 1.07x faster                                                         |
| tomli_loads              | 2.92 sec                                                     | 2.73 sec: 1.07x faster                                                       |
| regex_v8                 | 27.2 ms                                                      | 25.6 ms: 1.06x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.82 us: 1.06x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 66.5 ms: 1.05x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.24 sec: 1.05x faster                                                       |
| genshi_xml               | 63.3 ms                                                      | 60.2 ms: 1.05x faster                                                        |
| fannkuch                 | 483 ms                                                       | 459 ms: 1.05x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                        |
| sympy_str                | 360 ms                                                       | 343 ms: 1.05x faster                                                         |
| sympy_expand             | 600 ms                                                       | 573 ms: 1.05x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 88.5 ms: 1.04x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.03x faster                                                        |
| nqueens                  | 115 ms                                                       | 111 ms: 1.03x faster                                                         |
| pidigits                 | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.58 us: 1.02x faster                                                        |
| meteor_contest           | 138 ms                                                       | 137 ms: 1.01x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 110 ms: 1.01x faster                                                         |
| spectral_norm            | 139 ms                                                       | 140 ms: 1.01x slower                                                         |
| regex_compile            | 190 ms                                                       | 194 ms: 1.02x slower                                                         |
| pickle_dict              | 29.5 us                                                      | 30.6 us: 1.04x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.4 us: 1.06x slower                                                        |
| scimark_fft              | 361 ms                                                       | 396 ms: 1.10x slower                                                         |
| pickle_list              | 4.12 us                                                      | 4.52 us: 1.10x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.94 ms: 1.10x slower                                                        |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 5.95 ms: 1.17x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.63 ms: 1.18x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.67 ms: 1.20x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 8.90 ms: 1.21x slower                                                        |
| coverage                 | 63.3 ms                                                      | 81.8 ms: 1.29x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.44 ms: 1.30x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.18x faster                                                                 |

Benchmark hidden because not significant (2): hexiom, asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.12x