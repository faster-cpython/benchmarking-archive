# Results vs. 3.10.4

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: dedffa7
- commit date: 2024-05-01
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.41 ms: 1.31x faster                                                            |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.8 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 354 ms: 2.05x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 928 ms: 1.91x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.65x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.4 ms: 1.74x faster                                                            |
| float          | 117 ms                                                 | 79.1 ms: 1.48x faster                                                            |
| pidigits       | 191 ms                                                 | 195 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                  | 1.36x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                            |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.71 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 311 us: 1.56x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 221 us: 1.50x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 62.3 ms: 1.27x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 90.3 ms: 1.10x faster                                                            |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| unpickle_list        | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.08 ms: 1.19x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.3 ms: 1.44x faster                                                            |
| django_template | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.6 ms: 1.35x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 51.3 ms: 1.29x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 165 us: 3.31x faster                                                             |
| generators               | 80.1 ms                                                | 29.2 ms: 2.74x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                            |
| async_tree_none          | 728 ms                                                 | 354 ms: 2.05x faster                                                             |
| raytrace                 | 507 ms                                                 | 266 ms: 1.91x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 928 ms: 1.91x faster                                                             |
| chaos                    | 115 ms                                                 | 60.6 ms: 1.91x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.81x faster                                                             |
| logging_silent           | 190 ns                                                 | 106 ns: 1.79x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.75x faster                                                            |
| nbody                    | 154 ms                                                 | 88.4 ms: 1.74x faster                                                            |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                             |
| richards_super           | 94.7 ms                                                | 55.6 ms: 1.70x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 70.0 ms: 1.69x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.65x faster                                                             |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                             |
| go                       | 240 ms                                                 | 146 ms: 1.64x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.33 ms: 1.64x faster                                                            |
| richards                 | 79.3 ms                                                | 49.0 ms: 1.62x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.61 ms: 1.60x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 311 us: 1.56x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                            |
| spectral_norm            | 170 ms                                                 | 111 ms: 1.52x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.7 us: 1.51x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 221 us: 1.50x faster                                                             |
| scimark_lu               | 176 ms                                                 | 118 ms: 1.49x faster                                                             |
| float                    | 117 ms                                                 | 79.1 ms: 1.48x faster                                                            |
| pyflate                  | 716 ms                                                 | 489 ms: 1.46x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| tornado_http             | 136 ms                                                 | 93.8 ms: 1.45x faster                                                            |
| mako                     | 16.3 ms                                                | 11.3 ms: 1.44x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.79 us: 1.43x faster                                                            |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| django_template          | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.56 sec: 1.35x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.6 ms: 1.35x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 761 ms: 1.34x faster                                                             |
| nqueens                  | 106 ms                                                 | 79.6 ms: 1.33x faster                                                            |
| fannkuch                 | 532 ms                                                 | 402 ms: 1.32x faster                                                             |
| deepcopy                 | 479 us                                                 | 364 us: 1.32x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.41 ms: 1.31x faster                                                            |
| thrift                   | 1.07 ms                                                | 822 us: 1.30x faster                                                             |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                           |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.29x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 51.3 ms: 1.29x faster                                                            |
| 2to3                     | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 65.9 ms: 1.28x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 62.3 ms: 1.27x faster                                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.26x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.19 ms: 1.25x faster                                                            |
| scimark_fft              | 466 ms                                                 | 377 ms: 1.24x faster                                                             |
| djangocms                | 38.4 us                                                | 31.2 us: 1.23x faster                                                            |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                            |
| sympy_expand             | 566 ms                                                 | 472 ms: 1.20x faster                                                             |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 826 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| pathlib                  | 20.5 ms                                                | 17.5 ms: 1.17x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.57 sec: 1.11x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 90.3 ms: 1.10x faster                                                            |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                             |
| json                     | 5.69 ms                                                | 5.53 ms: 1.03x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| pickle_list              | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                             |
| pidigits                 | 191 ms                                                 | 195 ms: 1.02x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.71 ms: 1.02x slower                                                            |
| unpickle_list            | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                            |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.98 ms: 1.10x slower                                                            |
| telco                    | 7.27 ms                                                | 8.52 ms: 1.17x slower                                                            |
| coverage                 | 79.4 ms                                                | 93.8 ms: 1.18x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.08 ms: 1.19x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                     |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240501-3.13.0a6+-dedffa7/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x