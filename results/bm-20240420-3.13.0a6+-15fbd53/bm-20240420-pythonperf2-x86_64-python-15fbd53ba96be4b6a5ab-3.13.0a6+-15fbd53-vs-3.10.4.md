# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 285 ms: 1.23x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                        |
| docutils       | 3.41 sec                                                     | 2.97 sec: 1.15x faster                                                       |
| html5lib       | 94.6 ms                                                      | 73.1 ms: 1.29x faster                                                        |
| tornado_http   | 157 ms                                                       | 120 ms: 1.30x faster                                                         |
| Geometric mean | (ref)                                                        | 1.24x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 373 ms: 1.85x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 898 ms: 1.78x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 466 ms: 1.76x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 618 ms: 1.52x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.72x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 86.9 ms: 1.54x faster                                                        |
| float          | 111 ms                                                       | 75.4 ms: 1.47x faster                                                        |
| pidigits       | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.32x faster                                                         |
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.2 ms: 1.08x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 307 us: 1.48x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 211 us: 1.48x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                       |
| xml_etree_process    | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.7 us: 1.23x faster                                                        |
| xml_etree_generate   | 92.3 ms                                                      | 83.8 ms: 1.10x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 151 ms: 1.06x faster                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 106 ms: 1.04x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.81 us: 1.04x slower                                                        |
| pickle               | 9.89 us                                                      | 10.2 us: 1.04x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 30.8 us: 1.05x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.9 us: 1.10x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 8.88 ms: 1.21x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.1 ms: 1.45x faster                                                        |
| django_template | 50.2 ms                                                      | 37.9 ms: 1.32x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 27.2 ms: 1.16x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 57.2 ms: 1.11x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.25x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 118 us: 4.55x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.26 ms: 2.30x faster                                                        |
| asyncio_tcp              | 779 ms                                                       | 378 ms: 2.06x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| raytrace                 | 489 ms                                                       | 254 ms: 1.92x faster                                                         |
| chaos                    | 109 ms                                                       | 58.5 ms: 1.86x faster                                                        |
| async_tree_none          | 692 ms                                                       | 373 ms: 1.85x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 60.3 ms: 1.78x faster                                                        |
| async_tree_io            | 1.60 sec                                                     | 898 ms: 1.78x faster                                                         |
| logging_silent           | 167 ns                                                       | 94.3 ns: 1.77x faster                                                        |
| async_tree_memoization   | 819 ms                                                       | 466 ms: 1.76x faster                                                         |
| scimark_lu               | 167 ms                                                       | 95.8 ms: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.4 ms: 1.72x faster                                                        |
| go                       | 262 ms                                                       | 156 ms: 1.68x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 72.2 ms: 1.65x faster                                                        |
| pylint                   | 566 ms                                                       | 344 ms: 1.65x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.38 ms: 1.62x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 5.98 ms: 1.58x faster                                                        |
| richards_super           | 90.6 ms                                                      | 57.6 ms: 1.57x faster                                                        |
| comprehensions           | 26.7 us                                                      | 17.0 us: 1.57x faster                                                        |
| pyflate                  | 733 ms                                                       | 474 ms: 1.55x faster                                                         |
| nbody                    | 134 ms                                                       | 86.9 ms: 1.54x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.76 ms: 1.52x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 618 ms: 1.52x faster                                                         |
| scimark_sor              | 180 ms                                                       | 120 ms: 1.51x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 307 us: 1.48x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 211 us: 1.48x faster                                                         |
| richards                 | 75.1 ms                                                      | 50.9 ms: 1.48x faster                                                        |
| float                    | 111 ms                                                       | 75.4 ms: 1.47x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.1 ms: 1.45x faster                                                        |
| coroutines               | 30.3 ms                                                      | 21.1 ms: 1.43x faster                                                        |
| spectral_norm            | 139 ms                                                       | 97.9 ms: 1.42x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.26 us: 1.42x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.58 ms: 1.39x faster                                                        |
| pycparser                | 1.67 sec                                                     | 1.22 sec: 1.38x faster                                                       |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.37x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.03 us: 1.37x faster                                                        |
| fannkuch                 | 483 ms                                                       | 361 ms: 1.34x faster                                                         |
| tomli_loads              | 2.92 sec                                                     | 2.19 sec: 1.33x faster                                                       |
| nqueens                  | 115 ms                                                       | 86.6 ms: 1.33x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.62 sec: 1.33x faster                                                       |
| regex_compile            | 190 ms                                                       | 143 ms: 1.32x faster                                                         |
| django_template          | 50.2 ms                                                      | 37.9 ms: 1.32x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 800 ms: 1.31x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 38.0 us: 1.31x faster                                                        |
| thrift                   | 1.18 ms                                                      | 897 us: 1.31x faster                                                         |
| tornado_http             | 157 ms                                                       | 120 ms: 1.30x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 73.1 ms: 1.29x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 896 us: 1.27x faster                                                         |
| chameleon                | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                        |
| sympy_sum                | 193 ms                                                       | 155 ms: 1.25x faster                                                         |
| scimark_fft              | 361 ms                                                       | 291 ms: 1.24x faster                                                         |
| pathlib                  | 21.4 ms                                                      | 17.3 ms: 1.23x faster                                                        |
| 2to3                     | 350 ms                                                       | 285 ms: 1.23x faster                                                         |
| json_loads               | 30.3 us                                                      | 24.7 us: 1.23x faster                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.15 ms: 1.22x faster                                                        |
| sympy_str                | 360 ms                                                       | 296 ms: 1.22x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 66.8 ms: 1.21x faster                                                        |
| sympy_integrate          | 28.2 ms                                                      | 23.3 ms: 1.21x faster                                                        |
| sqlglot_normalize        | 144 ms                                                       | 119 ms: 1.21x faster                                                         |
| mypy2                    | 933 ms                                                       | 773 ms: 1.21x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.50 sec: 1.20x faster                                                       |
| dask                     | 472 ms                                                       | 395 ms: 1.20x faster                                                         |
| sympy_expand             | 600 ms                                                       | 506 ms: 1.19x faster                                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 59.3 ms: 1.18x faster                                                        |
| deepcopy                 | 468 us                                                       | 397 us: 1.18x faster                                                         |
| async_generators         | 421 ms                                                       | 359 ms: 1.17x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 27.2 ms: 1.16x faster                                                        |
| docutils                 | 3.41 sec                                                     | 2.97 sec: 1.15x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.50 us: 1.15x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.06 ms: 1.12x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.03 ms: 1.12x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 57.2 ms: 1.11x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 83.8 ms: 1.10x faster                                                        |
| sqlite_synth             | 2.99 us                                                      | 2.72 us: 1.10x faster                                                        |
| meteor_contest           | 138 ms                                                       | 128 ms: 1.08x faster                                                         |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 25.2 ms: 1.08x faster                                                        |
| json                     | 5.86 ms                                                      | 5.44 ms: 1.08x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 151 ms: 1.06x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 106 ms: 1.04x faster                                                         |
| pidigits                 | 271 ms                                                       | 263 ms: 1.03x faster                                                         |
| unpickle_list            | 4.65 us                                                      | 4.81 us: 1.04x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.2 us: 1.04x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 30.8 us: 1.05x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.42 us: 1.07x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.93 ms: 1.09x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.9 us: 1.10x slower                                                        |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.13 ms: 1.13x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 8.88 ms: 1.21x slower                                                        |
| coverage                 | 63.3 ms                                                      | 82.9 ms: 1.31x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.58 ms: 1.34x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.31x faster                                                                 |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.11x