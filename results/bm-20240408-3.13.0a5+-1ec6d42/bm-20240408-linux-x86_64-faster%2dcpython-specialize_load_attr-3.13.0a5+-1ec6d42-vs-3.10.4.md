# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 1ec6d42
- commit date: 2024-04-08
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.01 ms: 1.38x faster                                                            |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.9 ms: 1.29x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 926 ms: 1.91x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.5 ms: 1.72x faster                                                            |
| float          | 117 ms                                                 | 79.3 ms: 1.48x faster                                                            |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.39x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                            |
| regex_dna      | 227 ms                                                 | 232 ms: 1.02x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.86 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 226 us: 1.46x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.5 ms: 1.31x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 87.9 ms: 1.13x faster                                                            |
| json_loads           | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.00 us: 1.04x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.35 us: 1.05x slower                                                            |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.93 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 52.6 ms: 1.26x faster                                                            |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.76x faster                                                             |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.27 ms: 2.42x faster                                                            |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                             |
| pylint                   | 551 ms                                                 | 282 ms: 1.96x faster                                                             |
| raytrace                 | 507 ms                                                 | 265 ms: 1.91x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 926 ms: 1.91x faster                                                             |
| chaos                    | 115 ms                                                 | 60.8 ms: 1.90x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.89x faster                                                             |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.7 ms: 1.76x faster                                                            |
| scimark_sor              | 220 ms                                                 | 125 ms: 1.76x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 68.1 ms: 1.74x faster                                                            |
| nbody                    | 154 ms                                                 | 89.5 ms: 1.72x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 76.0 ms: 1.68x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                            |
| richards                 | 79.3 ms                                                | 47.4 ms: 1.67x faster                                                            |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.47 ms: 1.61x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.1 ms: 1.59x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                             |
| scimark_lu               | 176 ms                                                 | 114 ms: 1.54x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.2 us: 1.53x faster                                                            |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                                             |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.52x faster                                                             |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                            |
| float                    | 117 ms                                                 | 79.3 ms: 1.48x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 226 us: 1.46x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.45x faster                                                           |
| tornado_http             | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| logging_simple           | 8.30 us                                                | 5.88 us: 1.41x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| logging_format           | 9.09 us                                                | 6.55 us: 1.39x faster                                                            |
| regex_compile            | 188 ms                                                 | 136 ms: 1.39x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.01 ms: 1.38x faster                                                            |
| fannkuch                 | 532 ms                                                 | 393 ms: 1.35x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 1.56 sec: 1.35x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 761 ms: 1.34x faster                                                             |
| genshi_text              | 31.8 ms                                                | 23.8 ms: 1.34x faster                                                            |
| thrift                   | 1.07 ms                                                | 811 us: 1.32x faster                                                             |
| deepcopy                 | 479 us                                                 | 364 us: 1.31x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 60.5 ms: 1.31x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.31x faster                                                           |
| html5lib                 | 88.9 ms                                                | 68.9 ms: 1.29x faster                                                            |
| scimark_fft              | 466 ms                                                 | 362 ms: 1.29x faster                                                             |
| 2to3                     | 348 ms                                                 | 271 ms: 1.28x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.27x faster                                                             |
| nqueens                  | 106 ms                                                 | 83.7 ms: 1.26x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.15 ms: 1.26x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.32 us: 1.26x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 52.6 ms: 1.26x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 20.6 ms: 1.25x faster                                                            |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.6 ms: 1.25x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.9 ms: 1.24x faster                                                            |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 742 ms: 1.20x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                            |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| sympy_expand             | 566 ms                                                 | 473 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 839 us: 1.18x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 87.9 ms: 1.13x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                            |
| json_loads               | 31.2 us                                                | 28.7 us: 1.09x faster                                                            |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.65 sec: 1.07x faster                                                           |
| json                     | 5.69 ms                                                | 5.38 ms: 1.06x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| unpickle_list            | 5.20 us                                                | 5.00 us: 1.04x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                            |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                             |
| async_generators         | 444 ms                                                 | 448 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                             |
| regex_dna                | 227 ms                                                 | 232 ms: 1.02x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.76 ms: 1.04x slower                                                            |
| pickle_list              | 5.08 us                                                | 5.35 us: 1.05x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.86 ms: 1.06x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| telco                    | 7.27 ms                                                | 8.54 ms: 1.18x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.2 ms: 1.22x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.93 ms: 1.50x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-1ec6d42/bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.09x