# Results vs. 3.10.4

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: a7b858b
- commit date: 2024-05-02
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.22 ms: 1.34x faster                                                            |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 70.3 ms: 1.26x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.2 ms: 1.46x faster                                                            |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 927 ms: 1.91x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 613 ms: 1.66x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.5 ms: 1.72x faster                                                            |
| float          | 117 ms                                                 | 78.9 ms: 1.48x faster                                                            |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.36x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                            |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 320 us: 1.51x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 220 us: 1.50x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.13 sec: 1.47x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.16 us: 1.02x slower                                                            |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.3 ms: 1.45x faster                                                            |
| django_template | 48.2 ms                                                | 34.7 ms: 1.39x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.0 ms: 1.38x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 50.8 ms: 1.30x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 165 us: 3.30x faster                                                             |
| generators               | 80.1 ms                                                | 29.4 ms: 2.73x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                            |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| go                       | 240 ms                                                 | 119 ms: 2.01x faster                                                             |
| raytrace                 | 507 ms                                                 | 262 ms: 1.94x faster                                                             |
| chaos                    | 115 ms                                                 | 60.5 ms: 1.91x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 927 ms: 1.91x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.5 ms: 1.77x faster                                                            |
| pylint                   | 551 ms                                                 | 318 ms: 1.74x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.73x faster                                                            |
| nbody                    | 154 ms                                                 | 89.5 ms: 1.72x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.22 ms: 1.67x faster                                                            |
| richards                 | 79.3 ms                                                | 47.4 ms: 1.67x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 613 ms: 1.66x faster                                                             |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 74.2 ms: 1.59x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.2 ms: 1.58x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 37.6 us: 1.56x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 83.7 ms: 1.53x faster                                                            |
| pyflate                  | 716 ms                                                 | 470 ms: 1.52x faster                                                             |
| scimark_lu               | 176 ms                                                 | 116 ms: 1.52x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 320 us: 1.51x faster                                                             |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.51x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 220 us: 1.50x faster                                                             |
| float                    | 117 ms                                                 | 78.9 ms: 1.48x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.13 sec: 1.47x faster                                                           |
| tornado_http             | 136 ms                                                 | 93.2 ms: 1.46x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.70 us: 1.46x faster                                                            |
| mako                     | 16.3 ms                                                | 11.3 ms: 1.45x faster                                                            |
| logging_format           | 9.09 us                                                | 6.33 us: 1.44x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| django_template          | 48.2 ms                                                | 34.7 ms: 1.39x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.0 ms: 1.38x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                           |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.35x faster                                                           |
| fannkuch                 | 532 ms                                                 | 394 ms: 1.35x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.22 ms: 1.34x faster                                                            |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 761 ms: 1.34x faster                                                             |
| nqueens                  | 106 ms                                                 | 79.6 ms: 1.33x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                                            |
| thrift                   | 1.07 ms                                                | 823 us: 1.30x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 50.8 ms: 1.30x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 65.5 ms: 1.29x faster                                                            |
| 2to3                     | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                             |
| scimark_fft              | 466 ms                                                 | 368 ms: 1.26x faster                                                             |
| html5lib                 | 88.9 ms                                                | 70.3 ms: 1.26x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.5 ms: 1.25x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.20 ms: 1.24x faster                                                            |
| sympy_str                | 346 ms                                                 | 280 ms: 1.23x faster                                                             |
| djangocms                | 38.4 us                                                | 31.2 us: 1.23x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                            |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| sympy_expand             | 566 ms                                                 | 473 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 828 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.10x faster                                                             |
| json_loads               | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.05x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.90 us: 1.04x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                           |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| async_generators         | 444 ms                                                 | 442 ms: 1.00x faster                                                             |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                             |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.16 us: 1.02x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.81 ms: 1.05x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| telco                    | 7.27 ms                                                | 8.50 ms: 1.17x slower                                                            |
| coverage                 | 79.4 ms                                                | 93.8 ms: 1.18x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.9 us: 1.21x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |

Benchmark hidden because not significant (2): regex_effbot, unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240502-3.13.0a6+-a7b858b/bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.10x