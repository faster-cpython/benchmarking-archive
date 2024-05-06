# Results vs. 3.10.4

- fork: faster-cpython
- ref: faster_trashcan
- machine: linux-x86_64
- commit hash: 29e2a03
- commit date: 2024-04-11
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                        |
| chameleon      | 9.68 ms                                                | 6.80 ms: 1.42x faster                                                       |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                      |
| html5lib       | 88.9 ms                                                | 68.1 ms: 1.30x faster                                                       |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                                       |
| Geometric mean | (ref)                                                  | 1.33x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 354 ms: 2.06x faster                                                        |
| async_tree_io           | 1.77 sec                                               | 920 ms: 1.92x faster                                                        |
| async_tree_memoization  | 870 ms                                                 | 463 ms: 1.88x faster                                                        |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 615 ms: 1.65x faster                                                        |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.0 ms: 1.74x faster                                                       |
| float          | 117 ms                                                 | 78.0 ms: 1.50x faster                                                       |
| pidigits       | 191 ms                                                 | 203 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                        |
| regex_v8       | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                       |
| regex_dna      | 227 ms                                                 | 223 ms: 1.02x faster                                                        |
| regex_effbot   | 3.63 ms                                                | 3.81 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 298 us: 1.63x faster                                                        |
| unpickle_pure_python | 331 us                                                 | 224 us: 1.47x faster                                                        |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.46x faster                                                      |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                       |
| xml_etree_process    | 79.1 ms                                                | 60.5 ms: 1.31x faster                                                       |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                       |
| json_loads           | 31.2 us                                                | 28.8 us: 1.08x faster                                                       |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                        |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                        |
| pickle_list          | 5.08 us                                                | 4.94 us: 1.03x faster                                                       |
| unpickle_list        | 5.20 us                                                | 5.34 us: 1.03x slower                                                       |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                       |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                       |
| pickle_dict          | 29.6 us                                                | 34.2 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                       |
| python_startup_no_site | 5.93 ms                                                | 7.06 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                       |
| genshi_text    | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                       |
| genshi_xml     | 66.0 ms                                                | 51.3 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                  | 1.39x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                                        |
| generators               | 80.1 ms                                                | 30.3 ms: 2.64x faster                                                       |
| deltablue                | 7.91 ms                                                | 3.17 ms: 2.49x faster                                                       |
| async_tree_none          | 728 ms                                                 | 354 ms: 2.06x faster                                                        |
| pylint                   | 551 ms                                                 | 277 ms: 1.99x faster                                                        |
| logging_silent           | 190 ns                                                 | 96.0 ns: 1.98x faster                                                       |
| raytrace                 | 507 ms                                                 | 261 ms: 1.94x faster                                                        |
| chaos                    | 115 ms                                                 | 60.0 ms: 1.93x faster                                                       |
| async_tree_io            | 1.77 sec                                               | 920 ms: 1.92x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 463 ms: 1.88x faster                                                        |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                        |
| scimark_sor              | 220 ms                                                 | 122 ms: 1.79x faster                                                        |
| richards_super           | 94.7 ms                                                | 52.9 ms: 1.79x faster                                                       |
| nbody                    | 154 ms                                                 | 88.0 ms: 1.74x faster                                                       |
| scimark_monte_carlo      | 118 ms                                                 | 68.5 ms: 1.73x faster                                                       |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.72x faster                                                       |
| richards                 | 79.3 ms                                                | 46.5 ms: 1.70x faster                                                       |
| go                       | 240 ms                                                 | 142 ms: 1.70x faster                                                        |
| crypto_pyaes             | 128 ms                                                 | 75.9 ms: 1.68x faster                                                       |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                       |
| hexiom                   | 10.4 ms                                                | 6.26 ms: 1.66x faster                                                       |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 615 ms: 1.65x faster                                                        |
| pickle_pure_python       | 484 us                                                 | 298 us: 1.63x faster                                                        |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.61x faster                                                       |
| deepcopy_memo            | 58.5 us                                                | 37.6 us: 1.56x faster                                                       |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                       |
| scimark_lu               | 176 ms                                                 | 116 ms: 1.51x faster                                                        |
| coroutines               | 35.1 ms                                                | 23.2 ms: 1.51x faster                                                       |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.50x faster                                                        |
| float                    | 117 ms                                                 | 78.0 ms: 1.50x faster                                                       |
| pyflate                  | 716 ms                                                 | 479 ms: 1.49x faster                                                        |
| unpickle_pure_python     | 331 us                                                 | 224 us: 1.47x faster                                                        |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.46x faster                                                      |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                                       |
| logging_simple           | 8.30 us                                                | 5.74 us: 1.45x faster                                                       |
| logging_format           | 9.09 us                                                | 6.37 us: 1.43x faster                                                       |
| chameleon                | 9.68 ms                                                | 6.80 ms: 1.42x faster                                                       |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                      |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                       |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.38x faster                                                      |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                      |
| pprint_safe_repr         | 1.02 sec                                               | 746 ms: 1.36x faster                                                        |
| fannkuch                 | 532 ms                                                 | 390 ms: 1.36x faster                                                        |
| genshi_text              | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                       |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                       |
| deepcopy                 | 479 us                                                 | 360 us: 1.33x faster                                                        |
| thrift                   | 1.07 ms                                                | 811 us: 1.32x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 60.5 ms: 1.31x faster                                                       |
| html5lib                 | 88.9 ms                                                | 68.1 ms: 1.30x faster                                                       |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                        |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                        |
| genshi_xml               | 66.0 ms                                                | 51.3 ms: 1.29x faster                                                       |
| nqueens                  | 106 ms                                                 | 82.2 ms: 1.29x faster                                                       |
| deepcopy_reduce          | 4.17 us                                                | 3.26 us: 1.28x faster                                                       |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                                       |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                        |
| dulwich_log              | 84.3 ms                                                | 66.8 ms: 1.26x faster                                                       |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                                       |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                        |
| scimark_fft              | 466 ms                                                 | 378 ms: 1.23x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                       |
| mypy2                    | 894 ms                                                 | 736 ms: 1.21x faster                                                        |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.33 ms: 1.21x faster                                                       |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                       |
| sympy_expand             | 566 ms                                                 | 469 ms: 1.21x faster                                                        |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                        |
| bench_thread_pool        | 986 us                                                 | 836 us: 1.18x faster                                                        |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                                      |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                       |
| mdp                      | 2.85 sec                                               | 2.58 sec: 1.10x faster                                                      |
| pathlib                  | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                       |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.08x faster                                                        |
| json_loads               | 31.2 us                                                | 28.8 us: 1.08x faster                                                       |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                        |
| regex_v8                 | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                       |
| json                     | 5.69 ms                                                | 5.35 ms: 1.06x faster                                                       |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                        |
| pickle_list              | 5.08 us                                                | 4.94 us: 1.03x faster                                                       |
| regex_dna                | 227 ms                                                 | 223 ms: 1.02x faster                                                        |
| sqlite_synth             | 3.02 us                                                | 2.99 us: 1.01x faster                                                       |
| async_generators         | 444 ms                                                 | 439 ms: 1.01x faster                                                        |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                       |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                        |
| unpickle_list            | 5.20 us                                                | 5.34 us: 1.03x slower                                                       |
| regex_effbot             | 3.63 ms                                                | 3.81 ms: 1.05x slower                                                       |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                       |
| pidigits                 | 191 ms                                                 | 203 ms: 1.06x slower                                                        |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                       |
| gc_traversal             | 3.62 ms                                                | 3.95 ms: 1.09x slower                                                       |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                       |
| pickle_dict              | 29.6 us                                                | 34.2 us: 1.16x slower                                                       |
| python_startup_no_site   | 5.93 ms                                                | 7.06 ms: 1.19x slower                                                       |
| telco                    | 7.27 ms                                                | 8.74 ms: 1.20x slower                                                       |
| coverage                 | 79.4 ms                                                | 97.6 ms: 1.23x slower                                                       |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240411-3.13.0a6+-29e2a03/bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x