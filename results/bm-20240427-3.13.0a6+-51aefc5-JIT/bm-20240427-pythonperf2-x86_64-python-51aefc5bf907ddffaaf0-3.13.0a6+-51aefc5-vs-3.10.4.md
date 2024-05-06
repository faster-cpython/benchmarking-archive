# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 303 ms: 1.16x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.67 ms: 1.23x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.09 sec: 1.11x faster                                                       |
| html5lib       | 94.6 ms                                                      | 73.8 ms: 1.28x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.29x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 370 ms: 1.87x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 902 ms: 1.77x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 468 ms: 1.75x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 618 ms: 1.51x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.72x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.1 ms: 1.46x faster                                                        |
| nbody          | 134 ms                                                       | 97.1 ms: 1.38x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                         |
| regex_dna      | 261 ms                                                       | 241 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.8 ms: 1.05x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.53 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 320 us: 1.42x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 221 us: 1.41x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.11 sec: 1.38x faster                                                       |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.6 us: 1.23x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 145 ms: 1.10x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 100 ms: 1.10x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.6 ms: 1.09x faster                                                        |
| unpickle_list        | 4.65 us                                                      | 4.75 us: 1.02x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.44 us: 1.08x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.9 us: 1.10x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 33.2 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 9.41 ms: 1.28x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.86 ms: 1.49x faster                                                        |
| django_template | 50.2 ms                                                      | 40.3 ms: 1.25x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 29.1 ms: 1.08x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 62.8 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.19x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 184 us: 2.92x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 374 ms: 2.08x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.80 ms: 1.97x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                       |
| async_tree_none          | 692 ms                                                       | 370 ms: 1.87x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 902 ms: 1.77x faster                                                         |
| raytrace                 | 489 ms                                                       | 277 ms: 1.76x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 468 ms: 1.75x faster                                                         |
| richards_super           | 90.6 ms                                                      | 52.2 ms: 1.74x faster                                                        |
| logging_silent           | 167 ns                                                       | 97.2 ns: 1.72x faster                                                        |
| generators               | 57.3 ms                                                      | 34.6 ms: 1.66x faster                                                        |
| chaos                    | 109 ms                                                       | 65.8 ms: 1.65x faster                                                        |
| richards                 | 75.1 ms                                                      | 46.2 ms: 1.63x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.56x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 77.7 ms: 1.53x faster                                                        |
| pyflate                  | 733 ms                                                       | 478 ms: 1.53x faster                                                         |
| pylint                   | 566 ms                                                       | 370 ms: 1.53x faster                                                         |
| go                       | 262 ms                                                       | 171 ms: 1.53x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 70.3 ms: 1.53x faster                                                        |
| spectral_norm            | 139 ms                                                       | 91.3 ms: 1.52x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 618 ms: 1.51x faster                                                         |
| mako                     | 14.7 ms                                                      | 9.86 ms: 1.49x faster                                                        |
| float                    | 111 ms                                                       | 76.1 ms: 1.46x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.84 ms: 1.46x faster                                                        |
| scimark_lu               | 167 ms                                                       | 117 ms: 1.43x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 320 us: 1.42x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 221 us: 1.41x faster                                                         |
| coroutines               | 30.3 ms                                                      | 21.6 ms: 1.41x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.11 sec: 1.38x faster                                                       |
| nbody                    | 134 ms                                                       | 97.1 ms: 1.38x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.4 us: 1.37x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.24 sec: 1.35x faster                                                       |
| logging_simple           | 8.88 us                                                      | 6.57 us: 1.35x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.17 us: 1.35x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.75 ms: 1.34x faster                                                        |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 37.6 us: 1.32x faster                                                        |
| thrift                   | 1.18 ms                                                      | 892 us: 1.32x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 7.30 ms: 1.29x faster                                                        |
| tornado_http             | 157 ms                                                       | 122 ms: 1.29x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 73.8 ms: 1.28x faster                                                        |
| fannkuch                 | 483 ms                                                       | 385 ms: 1.25x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.07 ms: 1.25x faster                                                        |
| django_template          | 50.2 ms                                                      | 40.3 ms: 1.25x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.74 sec: 1.24x faster                                                       |
| json_loads               | 30.3 us                                                      | 24.6 us: 1.23x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.67 ms: 1.23x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 856 ms: 1.23x faster                                                         |
| pathlib                  | 21.4 ms                                                      | 17.5 ms: 1.22x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 66.8 ms: 1.21x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 964 us: 1.18x faster                                                         |
| deepcopy                 | 468 us                                                       | 396 us: 1.18x faster                                                         |
| dask                     | 472 ms                                                       | 400 ms: 1.18x faster                                                         |
| sympy_sum                | 193 ms                                                       | 164 ms: 1.18x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.42 us: 1.17x faster                                                        |
| scimark_sor              | 180 ms                                                       | 154 ms: 1.17x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.58 sec: 1.16x faster                                                       |
| scimark_fft              | 361 ms                                                       | 311 ms: 1.16x faster                                                         |
| sympy_expand             | 600 ms                                                       | 517 ms: 1.16x faster                                                         |
| sympy_str                | 360 ms                                                       | 311 ms: 1.16x faster                                                         |
| 2to3                     | 350 ms                                                       | 303 ms: 1.16x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                         |
| nqueens                  | 115 ms                                                       | 102 ms: 1.13x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.66 us: 1.12x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.09 sec: 1.11x faster                                                       |
| sympy_integrate          | 28.2 ms                                                      | 25.5 ms: 1.10x faster                                                        |
| async_generators         | 421 ms                                                       | 381 ms: 1.10x faster                                                         |
| mypy2                    | 933 ms                                                       | 846 ms: 1.10x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 145 ms: 1.10x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 100 ms: 1.10x faster                                                         |
| json                     | 5.86 ms                                                      | 5.34 ms: 1.10x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 64.1 ms: 1.09x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 84.6 ms: 1.09x faster                                                        |
| regex_dna                | 261 ms                                                       | 241 ms: 1.08x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 29.1 ms: 1.08x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.8 ms: 1.05x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 62.8 ms: 1.01x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.75 us: 1.02x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.88 ms: 1.07x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.44 us: 1.08x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| telco                    | 7.23 ms                                                      | 7.97 ms: 1.10x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.9 us: 1.10x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 33.2 us: 1.13x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.53 ms: 1.14x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| coverage                 | 63.3 ms                                                      | 76.6 ms: 1.21x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 9.41 ms: 1.28x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.42 ms: 1.29x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.21x