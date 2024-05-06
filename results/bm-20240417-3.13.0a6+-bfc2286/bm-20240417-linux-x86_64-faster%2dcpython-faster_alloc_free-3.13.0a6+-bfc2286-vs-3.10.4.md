# Results vs. 3.10.4

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: bfc2286
- commit date: 2024-04-17
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 272 ms: 1.28x faster                                                          |
| chameleon      | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                         |
| docutils       | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| html5lib       | 88.9 ms                                                | 68.6 ms: 1.29x faster                                                         |
| tornado_http   | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 350 ms: 2.08x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 912 ms: 1.94x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.89x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 602 ms: 1.69x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 84.7 ms: 1.81x faster                                                         |
| float          | 117 ms                                                 | 77.6 ms: 1.51x faster                                                         |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                  | 1.40x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.38x faster                                                          |
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                          |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                          |
| unpickle_pure_python | 331 us                                                 | 222 us: 1.49x faster                                                          |
| tomli_loads          | 3.14 sec                                               | 2.24 sec: 1.40x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                         |
| xml_etree_process    | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                         |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                          |
| pickle_list          | 5.08 us                                                | 5.41 us: 1.07x slower                                                         |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                         |
| pickle               | 10.7 us                                                | 12.1 us: 1.13x slower                                                         |
| pickle_dict          | 29.6 us                                                | 36.0 us: 1.22x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                                  |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 7.07 ms: 1.19x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                         |
| django_template | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                         |
| genshi_text     | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                         |
| genshi_xml      | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                         |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.73x faster                                                          |
| generators               | 80.1 ms                                                | 29.5 ms: 2.72x faster                                                         |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                         |
| async_tree_none          | 728 ms                                                 | 350 ms: 2.08x faster                                                          |
| async_tree_io            | 1.77 sec                                               | 912 ms: 1.94x faster                                                          |
| chaos                    | 115 ms                                                 | 60.4 ms: 1.91x faster                                                         |
| raytrace                 | 507 ms                                                 | 265 ms: 1.91x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.89x faster                                                          |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.82x faster                                                          |
| nbody                    | 154 ms                                                 | 84.7 ms: 1.81x faster                                                         |
| logging_silent           | 190 ns                                                 | 105 ns: 1.80x faster                                                          |
| scimark_sor              | 220 ms                                                 | 125 ms: 1.76x faster                                                          |
| richards_super           | 94.7 ms                                                | 54.0 ms: 1.76x faster                                                         |
| pylint                   | 551 ms                                                 | 321 ms: 1.72x faster                                                          |
| scimark_monte_carlo      | 118 ms                                                 | 68.9 ms: 1.72x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 74.6 ms: 1.71x faster                                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 602 ms: 1.69x faster                                                          |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.69x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.67x faster                                                         |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                          |
| richards                 | 79.3 ms                                                | 48.0 ms: 1.65x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.38 ms: 1.63x faster                                                         |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.60x faster                                                         |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                          |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                         |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.54x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 38.3 us: 1.53x faster                                                         |
| float                    | 117 ms                                                 | 77.6 ms: 1.51x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 222 us: 1.49x faster                                                          |
| pyflate                  | 716 ms                                                 | 483 ms: 1.48x faster                                                          |
| mako                     | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                         |
| tornado_http             | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.81 us: 1.43x faster                                                         |
| logging_format           | 9.09 us                                                | 6.47 us: 1.40x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 2.24 sec: 1.40x faster                                                        |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                        |
| spectral_norm            | 170 ms                                                 | 122 ms: 1.39x faster                                                          |
| regex_compile            | 188 ms                                                 | 136 ms: 1.38x faster                                                          |
| django_template          | 48.2 ms                                                | 35.1 ms: 1.37x faster                                                         |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                                        |
| chameleon                | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 752 ms: 1.35x faster                                                          |
| deepcopy                 | 479 us                                                 | 357 us: 1.34x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.34x faster                                                        |
| genshi_text              | 31.8 ms                                                | 23.7 ms: 1.34x faster                                                         |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                         |
| fannkuch                 | 532 ms                                                 | 401 ms: 1.33x faster                                                          |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                                          |
| nqueens                  | 106 ms                                                 | 81.0 ms: 1.31x faster                                                         |
| xml_etree_process        | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                         |
| html5lib                 | 88.9 ms                                                | 68.6 ms: 1.29x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.24 us: 1.29x faster                                                         |
| 2to3                     | 348 ms                                                 | 272 ms: 1.28x faster                                                          |
| genshi_xml               | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                         |
| dulwich_log              | 84.3 ms                                                | 66.7 ms: 1.26x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 20.5 ms: 1.26x faster                                                         |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                          |
| sqlglot_optimize         | 69.2 ms                                                | 55.5 ms: 1.25x faster                                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.21 ms: 1.24x faster                                                         |
| scimark_fft              | 466 ms                                                 | 376 ms: 1.24x faster                                                          |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                         |
| sympy_str                | 346 ms                                                 | 283 ms: 1.22x faster                                                          |
| djangocms                | 38.4 us                                                | 31.7 us: 1.21x faster                                                         |
| mypy2                    | 894 ms                                                 | 739 ms: 1.21x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                         |
| sympy_expand             | 566 ms                                                 | 476 ms: 1.19x faster                                                          |
| dask                     | 441 ms                                                 | 371 ms: 1.19x faster                                                          |
| pathlib                  | 20.5 ms                                                | 17.4 ms: 1.18x faster                                                         |
| bench_thread_pool        | 986 us                                                 | 840 us: 1.17x faster                                                          |
| docutils                 | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                         |
| xml_etree_generate       | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| json                     | 5.69 ms                                                | 5.24 ms: 1.09x faster                                                         |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                          |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                          |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.80 sec: 1.02x faster                                                        |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                          |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                          |
| async_generators         | 444 ms                                                 | 446 ms: 1.01x slower                                                          |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                                          |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                         |
| gc_traversal             | 3.62 ms                                                | 3.76 ms: 1.04x slower                                                         |
| pickle_list              | 5.08 us                                                | 5.41 us: 1.07x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                         |
| pickle                   | 10.7 us                                                | 12.1 us: 1.13x slower                                                         |
| telco                    | 7.27 ms                                                | 8.60 ms: 1.18x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 7.07 ms: 1.19x slower                                                         |
| pickle_dict              | 29.6 us                                                | 36.0 us: 1.22x slower                                                         |
| coverage                 | 79.4 ms                                                | 97.7 ms: 1.23x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                  |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240417-3.13.0a6+-bfc2286/bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x