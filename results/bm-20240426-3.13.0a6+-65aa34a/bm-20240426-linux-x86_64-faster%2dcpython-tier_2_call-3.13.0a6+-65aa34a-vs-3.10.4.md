# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.30x faster                                                    |
| chameleon      | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                   |
| docutils       | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                  |
| html5lib       | 88.9 ms                                                | 65.6 ms: 1.35x faster                                                   |
| tornado_http   | 136 ms                                                 | 94.4 ms: 1.45x faster                                                   |
| Geometric mean | (ref)                                                  | 1.33x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                    |
| async_tree_io           | 1.77 sec                                               | 917 ms: 1.93x faster                                                    |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                                    |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 615 ms: 1.65x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.4 ms: 1.76x faster                                                   |
| float          | 117 ms                                                 | 78.8 ms: 1.49x faster                                                   |
| pidigits       | 191 ms                                                 | 194 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                  | 1.37x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                    |
| regex_v8       | 27.8 ms                                                | 26.3 ms: 1.05x faster                                                   |
| regex_dna      | 227 ms                                                 | 232 ms: 1.02x slower                                                    |
| regex_effbot   | 3.63 ms                                                | 3.85 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                    |
| unpickle_pure_python | 331 us                                                 | 213 us: 1.55x faster                                                    |
| tomli_loads          | 3.14 sec                                               | 2.14 sec: 1.47x faster                                                  |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                   |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.32x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                   |
| json_loads           | 31.2 us                                                | 27.4 us: 1.14x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                    |
| pickle_list          | 5.08 us                                                | 5.21 us: 1.03x slower                                                   |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                   |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                   |
| pickle_dict          | 29.6 us                                                | 34.4 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                            |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                   |
| django_template | 48.2 ms                                                | 34.4 ms: 1.40x faster                                                   |
| genshi_text     | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                   |
| genshi_xml      | 66.0 ms                                                | 51.1 ms: 1.29x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 163 us: 3.34x faster                                                    |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                   |
| deltablue                | 7.91 ms                                                | 3.22 ms: 2.46x faster                                                   |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                    |
| logging_silent           | 190 ns                                                 | 96.3 ns: 1.97x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 917 ms: 1.93x faster                                                    |
| chaos                    | 115 ms                                                 | 60.3 ms: 1.91x faster                                                   |
| raytrace                 | 507 ms                                                 | 267 ms: 1.90x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                                    |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                    |
| richards_super           | 94.7 ms                                                | 53.2 ms: 1.78x faster                                                   |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                                    |
| scimark_monte_carlo      | 118 ms                                                 | 67.2 ms: 1.76x faster                                                   |
| nbody                    | 154 ms                                                 | 87.4 ms: 1.76x faster                                                   |
| pylint                   | 551 ms                                                 | 318 ms: 1.74x faster                                                    |
| comprehensions           | 28.8 us                                                | 16.9 us: 1.70x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 75.2 ms: 1.70x faster                                                   |
| hexiom                   | 10.4 ms                                                | 6.15 ms: 1.69x faster                                                   |
| go                       | 240 ms                                                 | 142 ms: 1.69x faster                                                    |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 615 ms: 1.65x faster                                                    |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                    |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.61x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 213 us: 1.55x faster                                                    |
| pyflate                  | 716 ms                                                 | 464 ms: 1.54x faster                                                    |
| scimark_lu               | 176 ms                                                 | 118 ms: 1.50x faster                                                    |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 39.1 us: 1.50x faster                                                   |
| float                    | 117 ms                                                 | 78.8 ms: 1.49x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.14 sec: 1.47x faster                                                  |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.47x faster                                                    |
| tornado_http             | 136 ms                                                 | 94.4 ms: 1.45x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.83 us: 1.42x faster                                                   |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                                   |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                    |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                  |
| django_template          | 48.2 ms                                                | 34.4 ms: 1.40x faster                                                   |
| chameleon                | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                   |
| fannkuch                 | 532 ms                                                 | 383 ms: 1.39x faster                                                    |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.39x faster                                                  |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 742 ms: 1.37x faster                                                    |
| genshi_text              | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                   |
| html5lib                 | 88.9 ms                                                | 65.6 ms: 1.35x faster                                                   |
| deepcopy                 | 479 us                                                 | 355 us: 1.35x faster                                                    |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.32x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.32x faster                                                   |
| thrift                   | 1.07 ms                                                | 816 us: 1.31x faster                                                    |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.31x faster                                                    |
| 2to3                     | 348 ms                                                 | 267 ms: 1.30x faster                                                    |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                   |
| nqueens                  | 106 ms                                                 | 81.6 ms: 1.30x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 51.1 ms: 1.29x faster                                                   |
| scimark_fft              | 466 ms                                                 | 365 ms: 1.28x faster                                                    |
| sympy_integrate          | 25.8 ms                                                | 20.2 ms: 1.28x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 66.0 ms: 1.28x faster                                                   |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                    |
| sqlglot_optimize         | 69.2 ms                                                | 54.7 ms: 1.26x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.17 ms: 1.25x faster                                                   |
| sympy_str                | 346 ms                                                 | 276 ms: 1.25x faster                                                    |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                   |
| djangocms                | 38.4 us                                                | 31.4 us: 1.23x faster                                                   |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                                    |
| sympy_expand             | 566 ms                                                 | 467 ms: 1.21x faster                                                    |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                   |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                    |
| bench_thread_pool        | 986 us                                                 | 829 us: 1.19x faster                                                    |
| docutils                 | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                  |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                   |
| json_loads               | 31.2 us                                                | 27.4 us: 1.14x faster                                                   |
| json                     | 5.69 ms                                                | 5.12 ms: 1.11x faster                                                   |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                    |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                    |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                    |
| regex_v8                 | 27.8 ms                                                | 26.3 ms: 1.05x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.03x faster                                                   |
| gc_traversal             | 3.62 ms                                                | 3.55 ms: 1.02x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                  |
| async_generators         | 444 ms                                                 | 440 ms: 1.01x faster                                                    |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                   |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                    |
| pidigits                 | 191 ms                                                 | 194 ms: 1.01x slower                                                    |
| regex_dna                | 227 ms                                                 | 232 ms: 1.02x slower                                                    |
| pickle_list              | 5.08 us                                                | 5.21 us: 1.03x slower                                                   |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.85 ms: 1.06x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                   |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                   |
| pickle_dict              | 29.6 us                                                | 34.4 us: 1.16x slower                                                   |
| telco                    | 7.27 ms                                                | 8.49 ms: 1.17x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                   |
| coverage                 | 79.4 ms                                                | 98.6 ms: 1.24x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                            |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x