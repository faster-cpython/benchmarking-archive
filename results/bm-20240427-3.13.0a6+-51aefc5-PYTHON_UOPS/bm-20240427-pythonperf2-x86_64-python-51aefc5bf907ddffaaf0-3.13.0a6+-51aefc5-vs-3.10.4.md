# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.14x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 326 ms: 1.07x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.94 ms: 1.19x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.28 sec: 1.04x faster                                                       |
| html5lib       | 94.6 ms                                                      | 80.4 ms: 1.18x faster                                                        |
| tornado_http   | 157 ms                                                       | 126 ms: 1.25x faster                                                         |
| Geometric mean | (ref)                                                        | 1.14x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 386 ms: 1.79x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 927 ms: 1.72x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 485 ms: 1.69x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 634 ms: 1.48x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.67x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 92.8 ms: 1.20x faster                                                        |
| nbody          | 134 ms                                                       | 119 ms: 1.13x faster                                                         |
| pidigits       | 271 ms                                                       | 264 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.12x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                        |
| regex_dna      | 261 ms                                                       | 245 ms: 1.07x faster                                                         |
| regex_compile  | 190 ms                                                       | 199 ms: 1.05x slower                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.62 ms: 1.17x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 323 us: 1.41x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.8 ms: 1.34x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.6 us: 1.23x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 64.2 ms: 1.18x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.09x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 301 us: 1.04x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.86 sec: 1.02x faster                                                       |
| xml_etree_generate   | 92.3 ms                                                      | 91.6 ms: 1.01x faster                                                        |
| unpickle_list        | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 112 ms: 1.01x slower                                                         |
| pickle_list          | 4.12 us                                                      | 4.37 us: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 32.9 us: 1.12x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 8.91 ms: 1.22x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 50.2 ms                                                      | 43.0 ms: 1.17x faster                                                        |
| mako            | 14.7 ms                                                      | 14.3 ms: 1.03x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 31.8 ms: 1.01x slower                                                        |
| genshi_xml      | 63.3 ms                                                      | 65.8 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 197 us: 2.73x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 387 ms: 2.01x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.60 sec: 1.94x faster                                                       |
| async_tree_none          | 692 ms                                                       | 386 ms: 1.79x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 927 ms: 1.72x faster                                                         |
| deltablue                | 7.50 ms                                                      | 4.36 ms: 1.72x faster                                                        |
| generators               | 57.3 ms                                                      | 33.8 ms: 1.70x faster                                                        |
| async_tree_memoization   | 819 ms                                                       | 485 ms: 1.69x faster                                                         |
| logging_silent           | 167 ns                                                       | 100 ns: 1.67x faster                                                         |
| raytrace                 | 489 ms                                                       | 306 ms: 1.60x faster                                                         |
| pylint                   | 566 ms                                                       | 378 ms: 1.50x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 634 ms: 1.48x faster                                                         |
| richards_super           | 90.6 ms                                                      | 62.7 ms: 1.45x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.55 ms: 1.45x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 323 us: 1.41x faster                                                         |
| chaos                    | 109 ms                                                       | 77.3 ms: 1.40x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.0 ms: 1.38x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.95 ms: 1.37x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.71 ms: 1.35x faster                                                        |
| richards                 | 75.1 ms                                                      | 55.6 ms: 1.35x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.8 ms: 1.34x faster                                                        |
| thrift                   | 1.18 ms                                                      | 895 us: 1.31x faster                                                         |
| logging_format           | 9.64 us                                                      | 7.36 us: 1.31x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.79 us: 1.31x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 91.3 ms: 1.31x faster                                                        |
| go                       | 262 ms                                                       | 207 ms: 1.26x faster                                                         |
| tornado_http             | 157 ms                                                       | 126 ms: 1.25x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.34 sec: 1.25x faster                                                       |
| json_loads               | 30.3 us                                                      | 24.6 us: 1.23x faster                                                        |
| float                    | 111 ms                                                       | 92.8 ms: 1.20x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.94 ms: 1.19x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 64.2 ms: 1.18x faster                                                        |
| scimark_lu               | 167 ms                                                       | 141 ms: 1.18x faster                                                         |
| pyflate                  | 733 ms                                                       | 621 ms: 1.18x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 80.4 ms: 1.18x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 18.3 ms: 1.17x faster                                                        |
| django_template          | 50.2 ms                                                      | 43.0 ms: 1.17x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 42.7 us: 1.17x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 980 us: 1.16x faster                                                         |
| deepcopy                 | 468 us                                                       | 410 us: 1.14x faster                                                         |
| dask                     | 472 ms                                                       | 417 ms: 1.13x faster                                                         |
| nbody                    | 134 ms                                                       | 119 ms: 1.13x faster                                                         |
| scimark_sor              | 180 ms                                                       | 161 ms: 1.12x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.59 us: 1.12x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 97.9 ms: 1.10x faster                                                        |
| mdp                      | 3.01 sec                                                     | 2.75 sec: 1.09x faster                                                       |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.09x faster                                                         |
| sympy_sum                | 193 ms                                                       | 178 ms: 1.08x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 133 ms: 1.08x faster                                                         |
| mypy2                    | 933 ms                                                       | 868 ms: 1.07x faster                                                         |
| 2to3                     | 350 ms                                                       | 326 ms: 1.07x faster                                                         |
| async_generators         | 421 ms                                                       | 393 ms: 1.07x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                        |
| json                     | 5.86 ms                                                      | 5.50 ms: 1.07x faster                                                        |
| regex_dna                | 261 ms                                                       | 245 ms: 1.07x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 26.5 ms: 1.06x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 76.8 ms: 1.06x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.87 us: 1.04x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.28 sec: 1.04x faster                                                       |
| sympy_expand             | 600 ms                                                       | 577 ms: 1.04x faster                                                         |
| sympy_str                | 360 ms                                                       | 346 ms: 1.04x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 301 us: 1.04x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.15 ms: 1.03x faster                                                        |
| pidigits                 | 271 ms                                                       | 264 ms: 1.03x faster                                                         |
| mako                     | 14.7 ms                                                      | 14.3 ms: 1.03x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.13 ms: 1.03x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 2.11 sec: 1.02x faster                                                       |
| sqlglot_optimize         | 70.1 ms                                                      | 68.8 ms: 1.02x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.86 sec: 1.02x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 1.04 sec: 1.01x faster                                                       |
| xml_etree_generate       | 92.3 ms                                                      | 91.6 ms: 1.01x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.62 us: 1.01x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 31.8 ms: 1.01x slower                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 112 ms: 1.01x slower                                                         |
| nqueens                  | 115 ms                                                       | 119 ms: 1.03x slower                                                         |
| comprehensions           | 26.7 us                                                      | 27.6 us: 1.04x slower                                                        |
| spectral_norm            | 139 ms                                                       | 144 ms: 1.04x slower                                                         |
| genshi_xml               | 63.3 ms                                                      | 65.8 ms: 1.04x slower                                                        |
| meteor_contest           | 138 ms                                                       | 144 ms: 1.04x slower                                                         |
| regex_compile            | 190 ms                                                       | 199 ms: 1.05x slower                                                         |
| pickle_list              | 4.12 us                                                      | 4.37 us: 1.06x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 32.9 us: 1.12x slower                                                        |
| hexiom                   | 9.42 ms                                                      | 10.6 ms: 1.12x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.0 ms: 1.13x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.14x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.62 ms: 1.17x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 2.07 ms: 1.17x slower                                                        |
| scimark_fft              | 361 ms                                                       | 425 ms: 1.18x slower                                                         |
| telco                    | 7.23 ms                                                      | 8.59 ms: 1.19x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 8.91 ms: 1.22x slower                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 6.28 ms: 1.24x slower                                                        |
| coverage                 | 63.3 ms                                                      | 80.0 ms: 1.27x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.91 ms: 1.44x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.14x faster                                                                 |

Benchmark hidden because not significant (2): asyncio_websockets, fannkuch
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.12x