# Results vs. 3.10.4

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 297 ms: 1.18x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.41 ms: 1.27x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.09 sec: 1.10x faster                                                       |
| html5lib       | 94.6 ms                                                      | 72.2 ms: 1.31x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.29x faster                                                         |
| Geometric mean | (ref)                                                        | 1.23x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 849 ms: 1.88x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 444 ms: 1.85x faster                                                         |
| async_tree_none         | 692 ms                                                       | 380 ms: 1.82x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 608 ms: 1.54x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.77x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.9 ms: 1.46x faster                                                        |
| nbody          | 134 ms                                                       | 101 ms: 1.33x faster                                                         |
| pidigits       | 271 ms                                                       | 262 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.26x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.29x faster                                                         |
| regex_dna      | 261 ms                                                       | 247 ms: 1.06x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.45 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 309 us: 1.47x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 239 us: 1.31x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| xml_etree_generate   | 92.3 ms                                                      | 84.0 ms: 1.10x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 149 ms: 1.07x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.07x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.58 us: 1.01x faster                                                        |
| pickle_list          | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 33.7 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 9.91 ms: 1.48x faster                                                        |
| genshi_text    | 31.4 ms                                                      | 26.8 ms: 1.17x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 58.5 ms: 1.08x faster                                                        |
| Geometric mean | (ref)                                                        | 1.23x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 119 us: 4.51x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.58 ms: 2.10x faster                                                        |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 849 ms: 1.88x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 444 ms: 1.85x faster                                                         |
| async_tree_none          | 692 ms                                                       | 380 ms: 1.82x faster                                                         |
| logging_silent           | 167 ns                                                       | 95.9 ns: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.3 ms: 1.72x faster                                                        |
| raytrace                 | 489 ms                                                       | 285 ms: 1.72x faster                                                         |
| chaos                    | 109 ms                                                       | 64.1 ms: 1.69x faster                                                        |
| pylint                   | 566 ms                                                       | 336 ms: 1.68x faster                                                         |
| richards_super           | 90.6 ms                                                      | 56.8 ms: 1.60x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.41 ms: 1.59x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 77.1 ms: 1.54x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 608 ms: 1.54x faster                                                         |
| pyflate                  | 733 ms                                                       | 482 ms: 1.52x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 71.5 ms: 1.50x faster                                                        |
| spectral_norm            | 139 ms                                                       | 93.2 ms: 1.49x faster                                                        |
| richards                 | 75.1 ms                                                      | 50.6 ms: 1.49x faster                                                        |
| mako                     | 14.7 ms                                                      | 9.91 ms: 1.48x faster                                                        |
| go                       | 262 ms                                                       | 177 ms: 1.48x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.48x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 309 us: 1.47x faster                                                         |
| float                    | 111 ms                                                       | 75.9 ms: 1.46x faster                                                        |
| scimark_lu               | 167 ms                                                       | 121 ms: 1.38x faster                                                         |
| coroutines               | 30.3 ms                                                      | 22.0 ms: 1.37x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.5 us: 1.37x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.15 sec: 1.36x faster                                                       |
| logging_simple           | 8.88 us                                                      | 6.54 us: 1.36x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.21 us: 1.34x faster                                                        |
| nbody                    | 134 ms                                                       | 101 ms: 1.33x faster                                                         |
| thrift                   | 1.18 ms                                                      | 890 us: 1.32x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 72.2 ms: 1.31x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                                       |
| unpickle_pure_python     | 312 us                                                       | 239 us: 1.31x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.6 us: 1.29x faster                                                        |
| tornado_http             | 157 ms                                                       | 122 ms: 1.29x faster                                                         |
| regex_compile            | 190 ms                                                       | 148 ms: 1.29x faster                                                         |
| hexiom                   | 9.42 ms                                                      | 7.39 ms: 1.27x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.41 ms: 1.27x faster                                                        |
| fannkuch                 | 483 ms                                                       | 385 ms: 1.25x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.74 sec: 1.24x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 5.15 ms: 1.24x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 851 ms: 1.23x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.13 ms: 1.23x faster                                                        |
| json_loads               | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| deepcopy                 | 468 us                                                       | 394 us: 1.19x faster                                                         |
| 2to3                     | 350 ms                                                       | 297 ms: 1.18x faster                                                         |
| sympy_str                | 360 ms                                                       | 306 ms: 1.18x faster                                                         |
| sympy_sum                | 193 ms                                                       | 164 ms: 1.18x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 122 ms: 1.17x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.42 us: 1.17x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 26.8 ms: 1.17x faster                                                        |
| scimark_sor              | 180 ms                                                       | 154 ms: 1.17x faster                                                         |
| dask                     | 472 ms                                                       | 404 ms: 1.17x faster                                                         |
| sympy_expand             | 600 ms                                                       | 514 ms: 1.17x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 69.8 ms: 1.16x faster                                                        |
| scimark_fft              | 361 ms                                                       | 314 ms: 1.15x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.64 sec: 1.14x faster                                                       |
| mypy2                    | 933 ms                                                       | 826 ms: 1.13x faster                                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 62.3 ms: 1.13x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.12x faster                                                        |
| sympy_integrate          | 28.2 ms                                                      | 25.5 ms: 1.11x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.09 sec: 1.10x faster                                                       |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 84.0 ms: 1.10x faster                                                        |
| nqueens                  | 115 ms                                                       | 105 ms: 1.09x faster                                                         |
| async_generators         | 421 ms                                                       | 388 ms: 1.08x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 58.5 ms: 1.08x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 149 ms: 1.07x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.07x faster                                                         |
| json                     | 5.86 ms                                                      | 5.51 ms: 1.06x faster                                                        |
| regex_dna                | 261 ms                                                       | 247 ms: 1.06x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                        |
| meteor_contest           | 138 ms                                                       | 131 ms: 1.06x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.06x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 26.0 ms: 1.05x faster                                                        |
| pidigits                 | 271 ms                                                       | 262 ms: 1.04x faster                                                         |
| bench_thread_pool        | 1.14 ms                                                      | 1.11 ms: 1.03x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.58 us: 1.01x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.84 ms: 1.04x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| telco                    | 7.23 ms                                                      | 7.98 ms: 1.10x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.45 ms: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 33.7 us: 1.14x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| coverage                 | 63.3 ms                                                      | 81.8 ms: 1.29x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.54 ms: 1.33x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-027fa2e-JIT/bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.20x