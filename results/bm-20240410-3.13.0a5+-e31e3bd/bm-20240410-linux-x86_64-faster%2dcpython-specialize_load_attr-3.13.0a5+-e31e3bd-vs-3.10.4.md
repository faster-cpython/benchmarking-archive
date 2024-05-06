# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: e31e3bd
- commit date: 2024-04-10
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 273 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.05 ms: 1.37x faster                                                            |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| html5lib       | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.9 ms: 1.45x faster                                                            |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 928 ms: 1.91x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 463 ms: 1.88x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 612 ms: 1.66x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.2 ms: 1.74x faster                                                            |
| float          | 117 ms                                                 | 78.6 ms: 1.49x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 137 ms: 1.38x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 304 us: 1.60x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 228 us: 1.45x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| json_loads           | 31.2 us                                                | 28.8 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.92 us: 1.03x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.27 us: 1.01x slower                                                            |
| pickle_dict          | 29.6 us                                                | 32.1 us: 1.09x slower                                                            |
| unpickle             | 14.4 us                                                | 15.9 us: 1.10x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.93 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                            |
| genshi_text    | 31.8 ms                                                | 24.6 ms: 1.30x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 53.6 ms: 1.23x faster                                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.64x faster                                                             |
| generators               | 80.1 ms                                                | 30.7 ms: 2.61x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.29 ms: 2.41x faster                                                            |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| pylint                   | 551 ms                                                 | 280 ms: 1.97x faster                                                             |
| raytrace                 | 507 ms                                                 | 262 ms: 1.93x faster                                                             |
| chaos                    | 115 ms                                                 | 60.5 ms: 1.91x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 928 ms: 1.91x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 463 ms: 1.88x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 507 ms: 1.82x faster                                                             |
| logging_silent           | 190 ns                                                 | 105 ns: 1.81x faster                                                             |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                                             |
| richards_super           | 94.7 ms                                                | 54.0 ms: 1.76x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 67.8 ms: 1.74x faster                                                            |
| nbody                    | 154 ms                                                 | 88.2 ms: 1.74x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 74.0 ms: 1.73x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.9 us: 1.70x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                            |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 612 ms: 1.66x faster                                                             |
| richards                 | 79.3 ms                                                | 48.0 ms: 1.65x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.48 ms: 1.60x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.60x faster                                                             |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.57x faster                                                            |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.52x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.9 us: 1.50x faster                                                            |
| pyflate                  | 716 ms                                                 | 481 ms: 1.49x faster                                                             |
| float                    | 117 ms                                                 | 78.6 ms: 1.49x faster                                                            |
| scimark_lu               | 176 ms                                                 | 119 ms: 1.48x faster                                                             |
| mako                     | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 228 us: 1.45x faster                                                             |
| tornado_http             | 136 ms                                                 | 93.9 ms: 1.45x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.86 us: 1.42x faster                                                            |
| logging_format           | 9.09 us                                                | 6.49 us: 1.40x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                           |
| regex_compile            | 188 ms                                                 | 137 ms: 1.38x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.05 ms: 1.37x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                                           |
| fannkuch                 | 532 ms                                                 | 392 ms: 1.36x faster                                                             |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 756 ms: 1.35x faster                                                             |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| thrift                   | 1.07 ms                                                | 801 us: 1.34x faster                                                             |
| html5lib                 | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.30x faster                                                            |
| genshi_text              | 31.8 ms                                                | 24.6 ms: 1.30x faster                                                            |
| nqueens                  | 106 ms                                                 | 82.7 ms: 1.28x faster                                                            |
| 2to3                     | 348 ms                                                 | 273 ms: 1.28x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.27x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.5 ms: 1.26x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 67.1 ms: 1.26x faster                                                            |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                             |
| scimark_fft              | 466 ms                                                 | 372 ms: 1.25x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 55.5 ms: 1.25x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.24 ms: 1.23x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 53.6 ms: 1.23x faster                                                            |
| sympy_str                | 346 ms                                                 | 282 ms: 1.23x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 740 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                            |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| sympy_expand             | 566 ms                                                 | 474 ms: 1.19x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 837 us: 1.18x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| json_loads               | 31.2 us                                                | 28.8 us: 1.09x faster                                                            |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                                           |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                             |
| pickle_list              | 5.08 us                                                | 4.92 us: 1.03x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.96 us: 1.02x faster                                                            |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                             |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| unpickle_list            | 5.20 us                                                | 5.27 us: 1.01x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.75 ms: 1.03x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.72 ms: 1.06x slower                                                            |
| pickle_dict              | 29.6 us                                                | 32.1 us: 1.09x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.9 us: 1.10x slower                                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| telco                    | 7.27 ms                                                | 8.62 ms: 1.19x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.3 ms: 1.23x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.93 ms: 1.51x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |

Benchmark hidden because not significant (2): bench_mp_pool, async_generators
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-e31e3bd/bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x