# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 286 ms: 1.23x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.51 ms: 1.26x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.00 sec: 1.14x faster                                                       |
| html5lib       | 94.6 ms                                                      | 73.2 ms: 1.29x faster                                                        |
| tornado_http   | 157 ms                                                       | 120 ms: 1.31x faster                                                         |
| Geometric mean | (ref)                                                        | 1.24x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 369 ms: 1.87x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 907 ms: 1.76x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 466 ms: 1.76x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 616 ms: 1.52x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.72x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 85.7 ms: 1.56x faster                                                        |
| float          | 111 ms                                                       | 76.6 ms: 1.45x faster                                                        |
| pidigits       | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 145 ms: 1.31x faster                                                         |
| regex_dna      | 261 ms                                                       | 236 ms: 1.11x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.7 ms: 1.06x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 312 us                                                       | 210 us: 1.48x faster                                                         |
| pickle_pure_python   | 455 us                                                       | 308 us: 1.48x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                       |
| xml_etree_process    | 75.9 ms                                                      | 59.8 ms: 1.27x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.5 us: 1.24x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.07x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.72 us: 1.02x slower                                                        |
| pickle               | 9.89 us                                                      | 10.2 us: 1.04x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 31.0 us: 1.05x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.5 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.14x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 8.84 ms: 1.21x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.3 ms: 1.43x faster                                                        |
| django_template | 50.2 ms                                                      | 38.4 ms: 1.31x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 57.1 ms: 1.11x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.26x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 169 us: 3.18x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.20 ms: 2.35x faster                                                        |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.09x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.57 sec: 1.97x faster                                                       |
| raytrace                 | 489 ms                                                       | 249 ms: 1.96x faster                                                         |
| async_tree_none          | 692 ms                                                       | 369 ms: 1.87x faster                                                         |
| chaos                    | 109 ms                                                       | 59.2 ms: 1.83x faster                                                        |
| logging_silent           | 167 ns                                                       | 93.4 ns: 1.79x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 60.7 ms: 1.77x faster                                                        |
| async_tree_io            | 1.60 sec                                                     | 907 ms: 1.76x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 466 ms: 1.76x faster                                                         |
| scimark_lu               | 167 ms                                                       | 95.7 ms: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.0 ms: 1.74x faster                                                        |
| go                       | 262 ms                                                       | 157 ms: 1.66x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 72.3 ms: 1.65x faster                                                        |
| pylint                   | 566 ms                                                       | 344 ms: 1.65x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                                        |
| comprehensions           | 26.7 us                                                      | 16.9 us: 1.58x faster                                                        |
| richards_super           | 90.6 ms                                                      | 57.6 ms: 1.57x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 6.02 ms: 1.56x faster                                                        |
| nbody                    | 134 ms                                                       | 85.7 ms: 1.56x faster                                                        |
| scimark_sor              | 180 ms                                                       | 118 ms: 1.52x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 616 ms: 1.52x faster                                                         |
| pyflate                  | 733 ms                                                       | 483 ms: 1.52x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.78 ms: 1.51x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 210 us: 1.48x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 308 us: 1.48x faster                                                         |
| richards                 | 75.1 ms                                                      | 50.9 ms: 1.47x faster                                                        |
| coroutines               | 30.3 ms                                                      | 20.6 ms: 1.47x faster                                                        |
| float                    | 111 ms                                                       | 76.6 ms: 1.45x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.3 ms: 1.43x faster                                                        |
| spectral_norm            | 139 ms                                                       | 98.1 ms: 1.42x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.56 ms: 1.40x faster                                                        |
| fannkuch                 | 483 ms                                                       | 353 ms: 1.37x faster                                                         |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.58 us: 1.35x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.15 us: 1.35x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.33x faster                                                       |
| tomli_loads              | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                       |
| pprint_pformat           | 2.15 sec                                                     | 1.63 sec: 1.32x faster                                                       |
| nqueens                  | 115 ms                                                       | 87.0 ms: 1.32x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 798 ms: 1.32x faster                                                         |
| regex_compile            | 190 ms                                                       | 145 ms: 1.31x faster                                                         |
| thrift                   | 1.18 ms                                                      | 896 us: 1.31x faster                                                         |
| tornado_http             | 157 ms                                                       | 120 ms: 1.31x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 38.0 us: 1.31x faster                                                        |
| django_template          | 50.2 ms                                                      | 38.4 ms: 1.31x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 73.2 ms: 1.29x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 886 us: 1.29x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 59.8 ms: 1.27x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.51 ms: 1.26x faster                                                        |
| sympy_sum                | 193 ms                                                       | 154 ms: 1.25x faster                                                         |
| pathlib                  | 21.4 ms                                                      | 17.2 ms: 1.24x faster                                                        |
| json_loads               | 30.3 us                                                      | 24.5 us: 1.24x faster                                                        |
| sqlglot_normalize        | 144 ms                                                       | 117 ms: 1.23x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 65.9 ms: 1.23x faster                                                        |
| 2to3                     | 350 ms                                                       | 286 ms: 1.23x faster                                                         |
| sympy_str                | 360 ms                                                       | 296 ms: 1.22x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 23.2 ms: 1.22x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                        |
| deepcopy                 | 468 us                                                       | 388 us: 1.21x faster                                                         |
| mypy2                    | 933 ms                                                       | 774 ms: 1.21x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                       |
| sqlglot_optimize         | 70.1 ms                                                      | 58.3 ms: 1.20x faster                                                        |
| dask                     | 472 ms                                                       | 393 ms: 1.20x faster                                                         |
| sympy_expand             | 600 ms                                                       | 502 ms: 1.20x faster                                                         |
| async_generators         | 421 ms                                                       | 358 ms: 1.18x faster                                                         |
| scimark_fft              | 361 ms                                                       | 308 ms: 1.17x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.37 ms: 1.16x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.00 sec: 1.14x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.52 us: 1.14x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.06 ms: 1.12x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.04 ms: 1.12x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| regex_dna                | 261 ms                                                       | 236 ms: 1.11x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 57.1 ms: 1.11x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.73 us: 1.09x faster                                                        |
| meteor_contest           | 138 ms                                                       | 127 ms: 1.09x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 84.8 ms: 1.09x faster                                                        |
| json                     | 5.86 ms                                                      | 5.41 ms: 1.08x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.07x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 25.7 ms: 1.06x faster                                                        |
| pidigits                 | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.72 us: 1.02x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.2 us: 1.04x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 31.0 us: 1.05x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| telco                    | 7.23 ms                                                      | 7.90 ms: 1.09x slower                                                        |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.98 ms: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.5 us: 1.15x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 8.84 ms: 1.21x slower                                                        |
| coverage                 | 63.3 ms                                                      | 78.1 ms: 1.23x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.75 ms: 1.39x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.30x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.11x