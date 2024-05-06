# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 08a7899
- commit date: 2024-04-09
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 270 ms: 1.29x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.81 ms: 1.42x faster                                                            |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.7 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 351 ms: 2.08x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 921 ms: 1.92x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 606 ms: 1.68x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.8 ms: 1.73x faster                                                            |
| float          | 117 ms                                                 | 78.5 ms: 1.49x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                            |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 220 us: 1.50x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.11 sec: 1.48x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.0 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.8 ms: 1.52x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.3 ms: 1.37x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 51.7 ms: 1.28x faster                                                            |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.75x faster                                                             |
| generators               | 80.1 ms                                                | 29.3 ms: 2.73x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.18 ms: 2.48x faster                                                            |
| async_tree_none          | 728 ms                                                 | 351 ms: 2.08x faster                                                             |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                             |
| chaos                    | 115 ms                                                 | 60.0 ms: 1.92x faster                                                            |
| raytrace                 | 507 ms                                                 | 264 ms: 1.92x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 921 ms: 1.92x faster                                                             |
| logging_silent           | 190 ns                                                 | 99.8 ns: 1.90x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.82x faster                                                             |
| richards_super           | 94.7 ms                                                | 52.9 ms: 1.79x faster                                                            |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 66.9 ms: 1.77x faster                                                            |
| nbody                    | 154 ms                                                 | 88.8 ms: 1.73x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                                            |
| richards                 | 79.3 ms                                                | 46.7 ms: 1.70x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.69x faster                                                            |
| go                       | 240 ms                                                 | 142 ms: 1.69x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 75.9 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 606 ms: 1.68x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.26 ms: 1.66x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 37.2 us: 1.57x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.57x faster                                                            |
| spectral_norm            | 170 ms                                                 | 110 ms: 1.55x faster                                                             |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.53x faster                                                             |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.52x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 220 us: 1.50x faster                                                             |
| pyflate                  | 716 ms                                                 | 477 ms: 1.50x faster                                                             |
| float                    | 117 ms                                                 | 78.5 ms: 1.49x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.11 sec: 1.48x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.64 us: 1.47x faster                                                            |
| logging_format           | 9.09 us                                                | 6.28 us: 1.45x faster                                                            |
| tornado_http             | 136 ms                                                 | 94.7 ms: 1.44x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.81 ms: 1.42x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.3 ms: 1.37x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                                           |
| deepcopy                 | 479 us                                                 | 355 us: 1.35x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 754 ms: 1.35x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| fannkuch                 | 532 ms                                                 | 395 ms: 1.34x faster                                                             |
| html5lib                 | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.32x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.17 us: 1.32x faster                                                            |
| thrift                   | 1.07 ms                                                | 816 us: 1.31x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                            |
| nqueens                  | 106 ms                                                 | 81.5 ms: 1.30x faster                                                            |
| 2to3                     | 348 ms                                                 | 270 ms: 1.29x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 51.7 ms: 1.28x faster                                                            |
| scimark_fft              | 466 ms                                                 | 365 ms: 1.28x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                                            |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.2 ms: 1.26x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.21 ms: 1.24x faster                                                            |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| sympy_expand             | 566 ms                                                 | 467 ms: 1.21x faster                                                             |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                            |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 835 us: 1.18x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.08x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                            |
| json                     | 5.69 ms                                                | 5.32 ms: 1.07x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                           |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| async_generators         | 444 ms                                                 | 447 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| unpickle_list            | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.74 ms: 1.03x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                                            |
| telco                    | 7.27 ms                                                | 8.52 ms: 1.17x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.0 us: 1.18x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.2 ms: 1.24x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240409-3.13.0a5+-08a7899/bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x