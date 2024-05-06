# Results vs. 3.10.4

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 846a7ef
- commit date: 2024-05-01
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                            |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 69.5 ms: 1.28x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.7 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 914 ms: 1.93x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.6 ms: 1.71x faster                                                            |
| float          | 117 ms                                                 | 78.2 ms: 1.50x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                            |
| regex_dna      | 227 ms                                                 | 221 ms: 1.03x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 318 us: 1.52x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 218 us: 1.51x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 61.8 ms: 1.28x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.4 ms: 1.12x faster                                                            |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.8 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.4 ms: 1.43x faster                                                            |
| django_template | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.3 ms: 1.37x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 50.6 ms: 1.31x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 161 us: 3.39x faster                                                             |
| generators               | 80.1 ms                                                | 29.2 ms: 2.74x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                            |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                                             |
| go                       | 240 ms                                                 | 119 ms: 2.01x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 914 ms: 1.93x faster                                                             |
| chaos                    | 115 ms                                                 | 60.1 ms: 1.92x faster                                                            |
| raytrace                 | 507 ms                                                 | 266 ms: 1.91x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| logging_silent           | 190 ns                                                 | 103 ns: 1.84x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 511 ms: 1.80x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.7 ms: 1.76x faster                                                            |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.72x faster                                                            |
| nbody                    | 154 ms                                                 | 89.6 ms: 1.71x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                             |
| scimark_sor              | 220 ms                                                 | 132 ms: 1.66x faster                                                             |
| richards                 | 79.3 ms                                                | 47.9 ms: 1.66x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.28 ms: 1.66x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 73.9 ms: 1.60x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                            |
| scimark_lu               | 176 ms                                                 | 114 ms: 1.55x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.1 us: 1.53x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 83.5 ms: 1.53x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 318 us: 1.52x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 218 us: 1.51x faster                                                             |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.51x faster                                                             |
| pyflate                  | 716 ms                                                 | 476 ms: 1.51x faster                                                             |
| float                    | 117 ms                                                 | 78.2 ms: 1.50x faster                                                            |
| tornado_http             | 136 ms                                                 | 93.7 ms: 1.45x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.78 us: 1.44x faster                                                            |
| mako                     | 16.3 ms                                                | 11.4 ms: 1.43x faster                                                            |
| logging_format           | 9.09 us                                                | 6.44 us: 1.41x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| django_template          | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                           |
| genshi_text              | 31.8 ms                                                | 23.3 ms: 1.37x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 751 ms: 1.36x faster                                                             |
| deepcopy                 | 479 us                                                 | 354 us: 1.35x faster                                                             |
| nqueens                  | 106 ms                                                 | 78.9 ms: 1.34x faster                                                            |
| fannkuch                 | 532 ms                                                 | 402 ms: 1.32x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 50.6 ms: 1.31x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                            |
| thrift                   | 1.07 ms                                                | 833 us: 1.29x faster                                                             |
| 2to3                     | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 61.8 ms: 1.28x faster                                                            |
| html5lib                 | 88.9 ms                                                | 69.5 ms: 1.28x faster                                                            |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.28x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 66.1 ms: 1.28x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.10 ms: 1.27x faster                                                            |
| scimark_fft              | 466 ms                                                 | 367 ms: 1.27x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 55.1 ms: 1.26x faster                                                            |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| djangocms                | 38.4 us                                                | 31.4 us: 1.22x faster                                                            |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                            |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                             |
| sympy_expand             | 566 ms                                                 | 473 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 831 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 88.4 ms: 1.12x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.59 sec: 1.10x faster                                                           |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                                            |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| json                     | 5.69 ms                                                | 5.39 ms: 1.06x faster                                                            |
| regex_dna                | 227 ms                                                 | 221 ms: 1.03x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.96 us: 1.02x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| async_generators         | 444 ms                                                 | 446 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.75 ms: 1.04x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                            |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.8 us: 1.18x slower                                                            |
| telco                    | 7.27 ms                                                | 8.62 ms: 1.19x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 96.8 ms: 1.22x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240501-3.13.0a6+-846a7ef/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x