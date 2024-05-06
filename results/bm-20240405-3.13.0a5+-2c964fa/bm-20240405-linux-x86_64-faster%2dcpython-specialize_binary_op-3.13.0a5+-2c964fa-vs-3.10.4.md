# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.30x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                            |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                           |
| html5lib       | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.3 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 351 ms: 2.08x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 912 ms: 1.94x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 460 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 605 ms: 1.68x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 95.9 ms: 1.60x faster                                                            |
| float          | 117 ms                                                 | 78.2 ms: 1.50x faster                                                            |
| pidigits       | 191 ms                                                 | 216 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                  | 1.28x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                            |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 221 us: 1.50x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.19 sec: 1.43x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.11 us: 1.02x faster                                                            |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                            |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.3 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 52.4 ms: 1.26x faster                                                            |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.76x faster                                                             |
| generators               | 80.1 ms                                                | 29.3 ms: 2.74x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.22 ms: 2.46x faster                                                            |
| async_tree_none          | 728 ms                                                 | 351 ms: 2.08x faster                                                             |
| pylint                   | 551 ms                                                 | 277 ms: 1.99x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 912 ms: 1.94x faster                                                             |
| raytrace                 | 507 ms                                                 | 265 ms: 1.91x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 460 ms: 1.89x faster                                                             |
| chaos                    | 115 ms                                                 | 62.8 ms: 1.84x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 69.9 ms: 1.83x faster                                                            |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                             |
| logging_silent           | 190 ns                                                 | 105 ns: 1.81x faster                                                             |
| scimark_sor              | 220 ms                                                 | 122 ms: 1.80x faster                                                             |
| richards_super           | 94.7 ms                                                | 52.7 ms: 1.80x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                                            |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 70.3 ms: 1.68x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 605 ms: 1.68x faster                                                             |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.30 ms: 1.65x faster                                                            |
| spectral_norm            | 170 ms                                                 | 103 ms: 1.65x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                            |
| nbody                    | 154 ms                                                 | 95.9 ms: 1.60x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                             |
| scimark_lu               | 176 ms                                                 | 113 ms: 1.56x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.9 ms: 1.53x faster                                                            |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                            |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.4 us: 1.52x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 221 us: 1.50x faster                                                             |
| float                    | 117 ms                                                 | 78.2 ms: 1.50x faster                                                            |
| tornado_http             | 136 ms                                                 | 94.3 ms: 1.45x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.19 sec: 1.43x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.81 us: 1.43x faster                                                            |
| logging_format           | 9.09 us                                                | 6.47 us: 1.40x faster                                                            |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                             |
| chameleon                | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                           |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.14 sec: 1.38x faster                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 739 ms: 1.38x faster                                                             |
| deepcopy                 | 479 us                                                 | 352 us: 1.36x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| fannkuch                 | 532 ms                                                 | 397 ms: 1.34x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| thrift                   | 1.07 ms                                                | 806 us: 1.33x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.14 us: 1.33x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.87 ms: 1.33x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                            |
| html5lib                 | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                            |
| nqueens                  | 106 ms                                                 | 81.0 ms: 1.31x faster                                                            |
| 2to3                     | 348 ms                                                 | 267 ms: 1.30x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.28x faster                                                             |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.27x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 52.4 ms: 1.26x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.1 ms: 1.25x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 67.3 ms: 1.25x faster                                                            |
| scimark_fft              | 466 ms                                                 | 375 ms: 1.24x faster                                                             |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 733 ms: 1.22x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.22x faster                                                            |
| sympy_expand             | 566 ms                                                 | 465 ms: 1.22x faster                                                             |
| dask                     | 441 ms                                                 | 366 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 827 us: 1.19x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.58 sec: 1.11x faster                                                           |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                             |
| json_loads               | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| json                     | 5.69 ms                                                | 5.45 ms: 1.04x faster                                                            |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.04x faster                                                            |
| pickle_list              | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| unpickle_list            | 5.20 us                                                | 5.11 us: 1.02x faster                                                            |
| async_generators         | 444 ms                                                 | 440 ms: 1.01x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.97 ms: 1.09x slower                                                            |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| pidigits                 | 191 ms                                                 | 216 ms: 1.13x slower                                                             |
| telco                    | 7.27 ms                                                | 8.43 ms: 1.16x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.3 us: 1.19x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.2 ms: 1.24x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-2c964fa/bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.09x