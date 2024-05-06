# Results vs. 3.10.4

- fork: python
- ref: 3e06c7f719b99cc7f5e8
- machine: linux-x86_64
- commit hash: 3e06c7f
- commit date: 2024-04-26
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 304 ms: 1.15x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.58 ms: 1.25x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                                       |
| html5lib       | 94.6 ms                                                      | 74.0 ms: 1.28x faster                                                        |
| tornado_http   | 157 ms                                                       | 124 ms: 1.27x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 376 ms: 1.84x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 909 ms: 1.76x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 472 ms: 1.74x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 622 ms: 1.50x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.70x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.2 ms: 1.46x faster                                                        |
| nbody          | 134 ms                                                       | 99.1 ms: 1.35x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.27x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 143 ms: 1.33x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 24.9 ms: 1.09x faster                                                        |
| regex_dna      | 261 ms                                                       | 240 ms: 1.09x faster                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.44 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.09x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 312 us: 1.46x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 223 us: 1.40x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.12 sec: 1.37x faster                                                       |
| xml_etree_process    | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.9 us: 1.22x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 83.6 ms: 1.10x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 30.8 us: 1.04x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.50 us: 1.09x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.14x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 9.44 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.84 ms: 1.49x faster                                                        |
| django_template | 50.2 ms                                                      | 41.4 ms: 1.21x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 29.7 ms: 1.06x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.18x faster                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 186 us: 2.88x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 376 ms: 2.07x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.83 ms: 1.96x faster                                                        |
| async_tree_none          | 692 ms                                                       | 376 ms: 1.84x faster                                                         |
| raytrace                 | 489 ms                                                       | 275 ms: 1.78x faster                                                         |
| logging_silent           | 167 ns                                                       | 94.8 ns: 1.77x faster                                                        |
| async_tree_io            | 1.60 sec                                                     | 909 ms: 1.76x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 472 ms: 1.74x faster                                                         |
| richards_super           | 90.6 ms                                                      | 52.8 ms: 1.71x faster                                                        |
| generators               | 57.3 ms                                                      | 34.3 ms: 1.67x faster                                                        |
| chaos                    | 109 ms                                                       | 65.5 ms: 1.66x faster                                                        |
| richards                 | 75.1 ms                                                      | 46.6 ms: 1.61x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.58x faster                                                        |
| pyflate                  | 733 ms                                                       | 479 ms: 1.53x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 77.8 ms: 1.53x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 70.5 ms: 1.52x faster                                                        |
| pylint                   | 566 ms                                                       | 373 ms: 1.52x faster                                                         |
| go                       | 262 ms                                                       | 174 ms: 1.51x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 622 ms: 1.50x faster                                                         |
| spectral_norm            | 139 ms                                                       | 92.8 ms: 1.50x faster                                                        |
| mako                     | 14.7 ms                                                      | 9.84 ms: 1.49x faster                                                        |
| scimark_lu               | 167 ms                                                       | 113 ms: 1.47x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.47x faster                                                        |
| float                    | 111 ms                                                       | 76.2 ms: 1.46x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 312 us: 1.46x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 223 us: 1.40x faster                                                         |
| coroutines               | 30.3 ms                                                      | 21.9 ms: 1.39x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.42 us: 1.38x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.6 ms: 1.38x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.00 us: 1.38x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.12 sec: 1.37x faster                                                       |
| comprehensions           | 26.7 us                                                      | 19.6 us: 1.36x faster                                                        |
| nbody                    | 134 ms                                                       | 99.1 ms: 1.35x faster                                                        |
| regex_compile            | 190 ms                                                       | 143 ms: 1.33x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 4.91 ms: 1.30x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.6 ms: 1.30x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.6 us: 1.29x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 7.31 ms: 1.29x faster                                                        |
| thrift                   | 1.18 ms                                                      | 918 us: 1.28x faster                                                         |
| fannkuch                 | 483 ms                                                       | 377 ms: 1.28x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 74.0 ms: 1.28x faster                                                        |
| tornado_http             | 157 ms                                                       | 124 ms: 1.27x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 830 ms: 1.26x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.70 sec: 1.26x faster                                                       |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.08 ms: 1.25x faster                                                        |
| chameleon                | 9.44 ms                                                      | 7.58 ms: 1.25x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 17.5 ms: 1.22x faster                                                        |
| json_loads               | 30.3 us                                                      | 24.9 us: 1.22x faster                                                        |
| django_template          | 50.2 ms                                                      | 41.4 ms: 1.21x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 67.0 ms: 1.21x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 955 us: 1.20x faster                                                         |
| scimark_sor              | 180 ms                                                       | 151 ms: 1.19x faster                                                         |
| scimark_fft              | 361 ms                                                       | 309 ms: 1.17x faster                                                         |
| sympy_sum                | 193 ms                                                       | 165 ms: 1.17x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.58 sec: 1.16x faster                                                       |
| dask                     | 472 ms                                                       | 406 ms: 1.16x faster                                                         |
| 2to3                     | 350 ms                                                       | 304 ms: 1.15x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.48 us: 1.15x faster                                                        |
| sympy_str                | 360 ms                                                       | 313 ms: 1.15x faster                                                         |
| deepcopy                 | 468 us                                                       | 408 us: 1.15x faster                                                         |
| nqueens                  | 115 ms                                                       | 101 ms: 1.14x faster                                                         |
| sympy_expand             | 600 ms                                                       | 531 ms: 1.13x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 128 ms: 1.12x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.67 us: 1.12x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 83.6 ms: 1.10x faster                                                        |
| async_generators         | 421 ms                                                       | 382 ms: 1.10x faster                                                         |
| docutils                 | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                                       |
| sympy_integrate          | 28.2 ms                                                      | 25.7 ms: 1.10x faster                                                        |
| json                     | 5.86 ms                                                      | 5.36 ms: 1.09x faster                                                        |
| mypy2                    | 933 ms                                                       | 855 ms: 1.09x faster                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 24.9 ms: 1.09x faster                                                        |
| regex_dna                | 261 ms                                                       | 240 ms: 1.09x faster                                                         |
| sqlglot_optimize         | 70.1 ms                                                      | 64.7 ms: 1.08x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 29.7 ms: 1.06x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.05x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.11 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                         |
| pickle                   | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 30.8 us: 1.04x slower                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.90 ms: 1.08x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.50 us: 1.09x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.00 ms: 1.11x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.44 ms: 1.11x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                        |
| coverage                 | 63.3 ms                                                      | 78.0 ms: 1.23x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.34 ms: 1.27x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 9.44 ms: 1.29x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                 |

Benchmark hidden because not significant (3): genshi_xml, unpickle_list, asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-3e06c7f-JIT/bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.21x