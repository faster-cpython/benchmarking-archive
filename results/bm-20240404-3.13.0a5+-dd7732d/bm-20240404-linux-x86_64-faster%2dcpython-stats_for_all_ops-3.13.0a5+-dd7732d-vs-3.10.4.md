# Results vs. 3.10.4

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: dd7732d
- commit date: 2024-04-04
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                          |
| chameleon      | 9.68 ms                                                | 6.98 ms: 1.39x faster                                                         |
| docutils       | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                        |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                         |
| tornado_http   | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 351 ms: 2.07x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 923 ms: 1.92x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 612 ms: 1.66x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 81.3 ms: 1.44x faster                                                         |
| nbody          | 154 ms                                                 | 127 ms: 1.21x faster                                                          |
| pidigits       | 191 ms                                                 | 198 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                  | 1.19x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.40x faster                                                          |
| regex_v8       | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                         |
| regex_dna      | 227 ms                                                 | 221 ms: 1.03x faster                                                          |
| regex_effbot   | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                          |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                          |
| tomli_loads          | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                         |
| xml_etree_process    | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.08x faster                                                          |
| json_loads           | 31.2 us                                                | 28.8 us: 1.08x faster                                                         |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                          |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                                         |
| unpickle             | 14.4 us                                                | 15.3 us: 1.07x slower                                                         |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                         |
| pickle_dict          | 29.6 us                                                | 34.2 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                  |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.2 ms: 1.46x faster                                                         |
| genshi_text    | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                         |
| genshi_xml     | 66.0 ms                                                | 51.0 ms: 1.30x faster                                                         |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.79x faster                                                          |
| generators               | 80.1 ms                                                | 29.6 ms: 2.70x faster                                                         |
| deltablue                | 7.91 ms                                                | 3.17 ms: 2.49x faster                                                         |
| async_tree_none          | 728 ms                                                 | 351 ms: 2.07x faster                                                          |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                          |
| async_tree_io            | 1.77 sec                                               | 923 ms: 1.92x faster                                                          |
| logging_silent           | 190 ns                                                 | 100 ns: 1.90x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                          |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                          |
| raytrace                 | 507 ms                                                 | 280 ms: 1.81x faster                                                          |
| richards_super           | 94.7 ms                                                | 52.5 ms: 1.80x faster                                                         |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.74x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 74.3 ms: 1.72x faster                                                         |
| richards                 | 79.3 ms                                                | 46.8 ms: 1.69x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                         |
| chaos                    | 115 ms                                                 | 68.9 ms: 1.68x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.23 ms: 1.67x faster                                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 612 ms: 1.66x faster                                                          |
| go                       | 240 ms                                                 | 145 ms: 1.65x faster                                                          |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.61x faster                                                         |
| scimark_sor              | 220 ms                                                 | 136 ms: 1.61x faster                                                          |
| scimark_monte_carlo      | 118 ms                                                 | 73.6 ms: 1.61x faster                                                         |
| deepcopy_memo            | 58.5 us                                                | 37.6 us: 1.56x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                          |
| coroutines               | 35.1 ms                                                | 23.7 ms: 1.48x faster                                                         |
| pyflate                  | 716 ms                                                 | 490 ms: 1.46x faster                                                          |
| mako                     | 16.3 ms                                                | 11.2 ms: 1.46x faster                                                         |
| scimark_lu               | 176 ms                                                 | 122 ms: 1.44x faster                                                          |
| tornado_http             | 136 ms                                                 | 94.6 ms: 1.44x faster                                                         |
| float                    | 117 ms                                                 | 81.3 ms: 1.44x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.85 us: 1.42x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                        |
| regex_compile            | 188 ms                                                 | 135 ms: 1.40x faster                                                          |
| tomli_loads              | 3.14 sec                                               | 2.26 sec: 1.39x faster                                                        |
| chameleon                | 9.68 ms                                                | 6.98 ms: 1.39x faster                                                         |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                         |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                                        |
| logging_format           | 9.09 us                                                | 6.59 us: 1.38x faster                                                         |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.38x faster                                                        |
| pprint_safe_repr         | 1.02 sec                                               | 742 ms: 1.37x faster                                                          |
| deepcopy                 | 479 us                                                 | 352 us: 1.36x faster                                                          |
| genshi_text              | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                         |
| thrift                   | 1.07 ms                                                | 809 us: 1.33x faster                                                          |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                         |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                         |
| deepcopy_reduce          | 4.17 us                                                | 3.20 us: 1.30x faster                                                         |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                          |
| xml_etree_process        | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                         |
| genshi_xml               | 66.0 ms                                                | 51.0 ms: 1.30x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                          |
| nqueens                  | 106 ms                                                 | 83.3 ms: 1.27x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                         |
| fannkuch                 | 532 ms                                                 | 419 ms: 1.27x faster                                                          |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                          |
| sqlglot_optimize         | 69.2 ms                                                | 55.1 ms: 1.25x faster                                                         |
| dulwich_log              | 84.3 ms                                                | 67.5 ms: 1.25x faster                                                         |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                                         |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                                          |
| nbody                    | 154 ms                                                 | 127 ms: 1.21x faster                                                          |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                         |
| sympy_expand             | 566 ms                                                 | 470 ms: 1.20x faster                                                          |
| dask                     | 441 ms                                                 | 369 ms: 1.20x faster                                                          |
| spectral_norm            | 170 ms                                                 | 142 ms: 1.19x faster                                                          |
| bench_thread_pool        | 986 us                                                 | 833 us: 1.18x faster                                                          |
| docutils                 | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                        |
| regex_v8                 | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                         |
| xml_etree_generate       | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.81 ms: 1.11x faster                                                         |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                          |
| scimark_fft              | 466 ms                                                 | 429 ms: 1.09x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.08x faster                                                          |
| json_loads               | 31.2 us                                                | 28.8 us: 1.08x faster                                                         |
| pathlib                  | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                         |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                          |
| json                     | 5.69 ms                                                | 5.43 ms: 1.05x faster                                                         |
| pickle_list              | 5.08 us                                                | 4.93 us: 1.03x faster                                                         |
| regex_dna                | 227 ms                                                 | 221 ms: 1.03x faster                                                          |
| mdp                      | 2.85 sec                                               | 2.78 sec: 1.03x faster                                                        |
| sqlite_synth             | 3.02 us                                                | 2.96 us: 1.02x faster                                                         |
| gc_traversal             | 3.62 ms                                                | 3.59 ms: 1.01x faster                                                         |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| async_generators         | 444 ms                                                 | 441 ms: 1.01x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                          |
| regex_effbot             | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                         |
| pidigits                 | 191 ms                                                 | 198 ms: 1.04x slower                                                          |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.07x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                         |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                         |
| pickle_dict              | 29.6 us                                                | 34.2 us: 1.15x slower                                                         |
| telco                    | 7.27 ms                                                | 8.68 ms: 1.19x slower                                                         |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.24x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 8.97 ms: 1.51x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                  |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-dd7732d/bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.10x