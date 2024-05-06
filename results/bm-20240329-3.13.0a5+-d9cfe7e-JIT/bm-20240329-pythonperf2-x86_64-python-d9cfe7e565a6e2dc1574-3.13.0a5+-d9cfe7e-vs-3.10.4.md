# Results vs. 3.10.4

- fork: python
- ref: d9cfe7e565a6e2dc1574
- machine: linux-x86_64
- commit hash: d9cfe7e
- commit date: 2024-03-29
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.43 ms: 1.27x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                       |
| html5lib       | 94.6 ms                                                      | 73.4 ms: 1.29x faster                                                        |
| tornado_http   | 157 ms                                                       | 124 ms: 1.26x faster                                                         |
| Geometric mean | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 377 ms: 1.83x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 454 ms: 1.81x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 907 ms: 1.76x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 600 ms: 1.56x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.74x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 79.5 ms: 1.40x faster                                                        |
| nbody          | 134 ms                                                       | 98.3 ms: 1.37x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.26x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| regex_dna      | 261 ms                                                       | 244 ms: 1.07x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.42 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 316 us: 1.44x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 235 us: 1.33x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 58.5 ms: 1.30x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.8 us: 1.18x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 83.9 ms: 1.10x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 104 ms: 1.07x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| pickle_list          | 4.12 us                                                      | 4.38 us: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 33.0 us: 1.12x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.5 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| django_template | 50.2 ms                                                      | 41.2 ms: 1.22x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 26.8 ms: 1.17x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 59.1 ms: 1.07x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.22x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 122 us: 4.40x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.10x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.85 ms: 1.95x faster                                                        |
| async_tree_none          | 692 ms                                                       | 377 ms: 1.83x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 454 ms: 1.81x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 907 ms: 1.76x faster                                                         |
| logging_silent           | 167 ns                                                       | 97.2 ns: 1.72x faster                                                        |
| generators               | 57.3 ms                                                      | 34.6 ms: 1.66x faster                                                        |
| chaos                    | 109 ms                                                       | 67.5 ms: 1.61x faster                                                        |
| raytrace                 | 489 ms                                                       | 308 ms: 1.59x faster                                                         |
| richards_super           | 90.6 ms                                                      | 58.0 ms: 1.56x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 600 ms: 1.56x faster                                                         |
| pylint                   | 566 ms                                                       | 364 ms: 1.55x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.45 ms: 1.55x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 77.5 ms: 1.54x faster                                                        |
| spectral_norm            | 139 ms                                                       | 93.2 ms: 1.49x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 72.9 ms: 1.47x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.0 ms: 1.47x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.84 ms: 1.45x faster                                                        |
| go                       | 262 ms                                                       | 180 ms: 1.45x faster                                                         |
| richards                 | 75.1 ms                                                      | 51.9 ms: 1.45x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 316 us: 1.44x faster                                                         |
| pyflate                  | 733 ms                                                       | 519 ms: 1.41x faster                                                         |
| float                    | 111 ms                                                       | 79.5 ms: 1.40x faster                                                        |
| scimark_lu               | 167 ms                                                       | 120 ms: 1.39x faster                                                         |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.38x faster                                                        |
| nbody                    | 134 ms                                                       | 98.3 ms: 1.37x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.7 us: 1.35x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                       |
| coroutines               | 30.3 ms                                                      | 22.5 ms: 1.35x faster                                                        |
| thrift                   | 1.18 ms                                                      | 882 us: 1.33x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 235 us: 1.33x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.33 us: 1.32x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.80 us: 1.31x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.5 ms: 1.30x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.3 us: 1.30x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.29 sec: 1.30x faster                                                       |
| html5lib                 | 94.6 ms                                                      | 73.4 ms: 1.29x faster                                                        |
| regex_compile            | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| fannkuch                 | 483 ms                                                       | 379 ms: 1.27x faster                                                         |
| chameleon                | 9.44 ms                                                      | 7.43 ms: 1.27x faster                                                        |
| tornado_http             | 157 ms                                                       | 124 ms: 1.26x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.72 sec: 1.25x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 841 ms: 1.25x faster                                                         |
| hexiom                   | 9.42 ms                                                      | 7.57 ms: 1.24x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 5.16 ms: 1.24x faster                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.15 ms: 1.22x faster                                                        |
| django_template          | 50.2 ms                                                      | 41.2 ms: 1.22x faster                                                        |
| deepcopy                 | 468 us                                                       | 388 us: 1.20x faster                                                         |
| sympy_str                | 360 ms                                                       | 304 ms: 1.19x faster                                                         |
| sympy_sum                | 193 ms                                                       | 163 ms: 1.18x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.40 us: 1.18x faster                                                        |
| json_loads               | 30.3 us                                                      | 25.8 us: 1.18x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 26.8 ms: 1.17x faster                                                        |
| sympy_expand             | 600 ms                                                       | 512 ms: 1.17x faster                                                         |
| scimark_sor              | 180 ms                                                       | 154 ms: 1.17x faster                                                         |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 69.8 ms: 1.16x faster                                                        |
| scimark_fft              | 361 ms                                                       | 312 ms: 1.16x faster                                                         |
| dask                     | 472 ms                                                       | 408 ms: 1.16x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.62 sec: 1.15x faster                                                       |
| mypy2                    | 933 ms                                                       | 833 ms: 1.12x faster                                                         |
| nqueens                  | 115 ms                                                       | 103 ms: 1.12x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.11x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                       |
| sqlglot_optimize         | 70.1 ms                                                      | 63.6 ms: 1.10x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.71 us: 1.10x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 83.9 ms: 1.10x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                        |
| json                     | 5.86 ms                                                      | 5.41 ms: 1.08x faster                                                        |
| async_generators         | 421 ms                                                       | 390 ms: 1.08x faster                                                         |
| regex_dna                | 261 ms                                                       | 244 ms: 1.07x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 59.1 ms: 1.07x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 104 ms: 1.07x faster                                                         |
| meteor_contest           | 138 ms                                                       | 131 ms: 1.06x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.06x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| unpack_sequence          | 59.9 ns                                                      | 58.5 ns: 1.02x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.79 ms: 1.01x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.38 us: 1.06x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| telco                    | 7.23 ms                                                      | 7.97 ms: 1.10x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.42 ms: 1.11x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 33.0 us: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.5 us: 1.15x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.38 ms: 1.28x slower                                                        |
| coverage                 | 63.3 ms                                                      | 83.0 ms: 1.31x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.24x faster                                                                 |

Benchmark hidden because not significant (2): bench_thread_pool, asyncio_websockets
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x