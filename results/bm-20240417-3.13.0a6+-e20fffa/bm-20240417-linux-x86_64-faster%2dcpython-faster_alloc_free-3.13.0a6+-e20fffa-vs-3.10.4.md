# Results vs. 3.10.4

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: e20fffa
- commit date: 2024-04-17
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                                          |
| chameleon      | 9.68 ms                                                | 7.20 ms: 1.34x faster                                                         |
| docutils       | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| html5lib       | 88.9 ms                                                | 66.9 ms: 1.33x faster                                                         |
| tornado_http   | 136 ms                                                 | 94.1 ms: 1.45x faster                                                         |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 358 ms: 2.03x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 927 ms: 1.91x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 85.0 ms: 1.81x faster                                                         |
| float          | 117 ms                                                 | 77.2 ms: 1.52x faster                                                         |
| pidigits       | 191 ms                                                 | 191 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                  | 1.40x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.39x faster                                                          |
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| regex_dna      | 227 ms                                                 | 221 ms: 1.02x faster                                                          |
| regex_effbot   | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                          |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                          |
| tomli_loads          | 3.14 sec                                               | 2.18 sec: 1.44x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                         |
| xml_etree_process    | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                         |
| json_loads           | 31.2 us                                                | 27.5 us: 1.13x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 88.9 ms: 1.12x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.04x faster                                                          |
| pickle_list          | 5.08 us                                                | 4.89 us: 1.04x faster                                                         |
| unpickle_list        | 5.20 us                                                | 5.08 us: 1.02x faster                                                         |
| unpickle             | 14.4 us                                                | 14.8 us: 1.03x slower                                                         |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                         |
| pickle_dict          | 29.6 us                                                | 32.7 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 7.06 ms: 1.19x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                         |
| django_template | 48.2 ms                                                | 35.0 ms: 1.38x faster                                                         |
| genshi_text     | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                         |
| genshi_xml      | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                         |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.73x faster                                                          |
| generators               | 80.1 ms                                                | 30.4 ms: 2.64x faster                                                         |
| deltablue                | 7.91 ms                                                | 3.22 ms: 2.46x faster                                                         |
| async_tree_none          | 728 ms                                                 | 358 ms: 2.03x faster                                                          |
| raytrace                 | 507 ms                                                 | 257 ms: 1.97x faster                                                          |
| chaos                    | 115 ms                                                 | 60.2 ms: 1.92x faster                                                         |
| async_tree_io            | 1.77 sec                                               | 927 ms: 1.91x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                          |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                          |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                          |
| nbody                    | 154 ms                                                 | 85.0 ms: 1.81x faster                                                         |
| richards_super           | 94.7 ms                                                | 52.9 ms: 1.79x faster                                                         |
| scimark_sor              | 220 ms                                                 | 125 ms: 1.76x faster                                                          |
| crypto_pyaes             | 128 ms                                                 | 72.9 ms: 1.75x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 68.2 ms: 1.73x faster                                                         |
| pylint                   | 551 ms                                                 | 320 ms: 1.72x faster                                                          |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.72x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                         |
| richards                 | 79.3 ms                                                | 47.1 ms: 1.68x faster                                                         |
| go                       | 240 ms                                                 | 143 ms: 1.68x faster                                                          |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                          |
| hexiom                   | 10.4 ms                                                | 6.35 ms: 1.64x faster                                                         |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                         |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.56x faster                                                         |
| pyflate                  | 716 ms                                                 | 461 ms: 1.55x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 38.4 us: 1.52x faster                                                         |
| float                    | 117 ms                                                 | 77.2 ms: 1.52x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                          |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.51x faster                                                          |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                         |
| scimark_lu               | 176 ms                                                 | 118 ms: 1.49x faster                                                          |
| tornado_http             | 136 ms                                                 | 94.1 ms: 1.45x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 2.18 sec: 1.44x faster                                                        |
| logging_simple           | 8.30 us                                                | 5.77 us: 1.44x faster                                                         |
| logging_format           | 9.09 us                                                | 6.40 us: 1.42x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.83 sec: 1.40x faster                                                        |
| regex_compile            | 188 ms                                                 | 135 ms: 1.39x faster                                                          |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                         |
| django_template          | 48.2 ms                                                | 35.0 ms: 1.38x faster                                                         |
| fannkuch                 | 532 ms                                                 | 390 ms: 1.36x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                        |
| chameleon                | 9.68 ms                                                | 7.20 ms: 1.34x faster                                                         |
| deepcopy                 | 479 us                                                 | 356 us: 1.34x faster                                                          |
| pprint_pformat           | 2.10 sec                                               | 1.57 sec: 1.34x faster                                                        |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                         |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                         |
| html5lib                 | 88.9 ms                                                | 66.9 ms: 1.33x faster                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 766 ms: 1.33x faster                                                          |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                         |
| xml_etree_process        | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                         |
| nqueens                  | 106 ms                                                 | 81.8 ms: 1.29x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                          |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                                          |
| dulwich_log              | 84.3 ms                                                | 66.1 ms: 1.28x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 20.5 ms: 1.26x faster                                                         |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                          |
| genshi_xml               | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                         |
| sqlglot_optimize         | 69.2 ms                                                | 55.5 ms: 1.25x faster                                                         |
| scimark_fft              | 466 ms                                                 | 374 ms: 1.25x faster                                                          |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.26 ms: 1.23x faster                                                         |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                         |
| sympy_str                | 346 ms                                                 | 282 ms: 1.22x faster                                                          |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                         |
| djangocms                | 38.4 us                                                | 31.8 us: 1.21x faster                                                         |
| dask                     | 441 ms                                                 | 369 ms: 1.19x faster                                                          |
| sympy_expand             | 566 ms                                                 | 474 ms: 1.19x faster                                                          |
| bench_thread_pool        | 986 us                                                 | 837 us: 1.18x faster                                                          |
| pathlib                  | 20.5 ms                                                | 17.5 ms: 1.17x faster                                                         |
| docutils                 | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                        |
| json_loads               | 31.2 us                                                | 27.5 us: 1.13x faster                                                         |
| xml_etree_generate       | 99.4 ms                                                | 88.9 ms: 1.12x faster                                                         |
| json                     | 5.69 ms                                                | 5.14 ms: 1.11x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.58 sec: 1.10x faster                                                        |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.08x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                          |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.04x faster                                                          |
| pickle_list              | 5.08 us                                                | 4.89 us: 1.04x faster                                                         |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                         |
| regex_dna                | 227 ms                                                 | 221 ms: 1.02x faster                                                          |
| unpickle_list            | 5.20 us                                                | 5.08 us: 1.02x faster                                                         |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                         |
| pidigits                 | 191 ms                                                 | 191 ms: 1.00x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                          |
| unpickle                 | 14.4 us                                                | 14.8 us: 1.03x slower                                                         |
| regex_effbot             | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                         |
| gc_traversal             | 3.62 ms                                                | 3.88 ms: 1.07x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                         |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                         |
| pickle_dict              | 29.6 us                                                | 32.7 us: 1.11x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 7.06 ms: 1.19x slower                                                         |
| telco                    | 7.27 ms                                                | 8.69 ms: 1.20x slower                                                         |
| coverage                 | 79.4 ms                                                | 97.9 ms: 1.23x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                  |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240417-3.13.0a6+-e20fffa/bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x