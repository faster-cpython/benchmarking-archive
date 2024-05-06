# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 279 ms: 1.25x faster                                              |
| chameleon      | 9.68 ms                                                | 6.88 ms: 1.41x faster                                             |
| docutils       | 3.30 sec                                               | 2.91 sec: 1.13x faster                                            |
| html5lib       | 88.9 ms                                                | 65.7 ms: 1.35x faster                                             |
| tornado_http   | 136 ms                                                 | 95.7 ms: 1.43x faster                                             |
| Geometric mean | (ref)                                                  | 1.31x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                              |
| async_tree_memoization  | 870 ms                                                 | 455 ms: 1.91x faster                                              |
| async_tree_io           | 1.77 sec                                               | 933 ms: 1.90x faster                                              |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 609 ms: 1.67x faster                                              |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.9 ms: 1.67x faster                                             |
| float          | 117 ms                                                 | 78.1 ms: 1.50x faster                                             |
| pidigits       | 191 ms                                                 | 194 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                  | 1.35x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 145 ms: 1.30x faster                                              |
| regex_v8       | 27.8 ms                                                | 26.1 ms: 1.07x faster                                             |
| regex_dna      | 227 ms                                                 | 233 ms: 1.03x slower                                              |
| regex_effbot   | 3.63 ms                                                | 3.75 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 304 us: 1.60x faster                                              |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                            |
| unpickle_pure_python | 331 us                                                 | 240 us: 1.38x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.31x faster                                             |
| xml_etree_generate   | 99.4 ms                                                | 87.4 ms: 1.14x faster                                             |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                             |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                              |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                              |
| pickle               | 10.7 us                                                | 11.8 us: 1.10x slower                                             |
| unpickle             | 14.4 us                                                | 15.9 us: 1.11x slower                                             |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                             |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                      |

Benchmark hidden because not significant (2): pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                             |
| python_startup_no_site | 5.93 ms                                                | 9.55 ms: 1.61x slower                                             |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.9 ms: 1.50x faster                                             |
| genshi_text    | 31.8 ms                                                | 24.2 ms: 1.32x faster                                             |
| genshi_xml     | 66.0 ms                                                | 53.2 ms: 1.24x faster                                             |
| Geometric mean | (ref)                                                  | 1.35x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                              |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                             |
| deltablue                | 7.91 ms                                                | 3.76 ms: 2.11x faster                                             |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                              |
| async_tree_memoization   | 870 ms                                                 | 455 ms: 1.91x faster                                              |
| async_tree_io            | 1.77 sec                                               | 933 ms: 1.90x faster                                              |
| chaos                    | 115 ms                                                 | 61.7 ms: 1.87x faster                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.87x faster                                              |
| pylint                   | 551 ms                                                 | 298 ms: 1.85x faster                                              |
| raytrace                 | 507 ms                                                 | 278 ms: 1.82x faster                                              |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                              |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.79x faster                                             |
| scimark_monte_carlo      | 118 ms                                                 | 68.7 ms: 1.72x faster                                             |
| richards                 | 79.3 ms                                                | 46.7 ms: 1.70x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 75.4 ms: 1.70x faster                                             |
| scimark_sor              | 220 ms                                                 | 130 ms: 1.68x faster                                              |
| nbody                    | 154 ms                                                 | 91.9 ms: 1.67x faster                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 609 ms: 1.67x faster                                              |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                             |
| comprehensions           | 28.8 us                                                | 17.8 us: 1.62x faster                                             |
| go                       | 240 ms                                                 | 150 ms: 1.60x faster                                              |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.60x faster                                              |
| coroutines               | 35.1 ms                                                | 22.1 ms: 1.59x faster                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                             |
| deepcopy_memo            | 58.5 us                                                | 38.0 us: 1.54x faster                                             |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                            |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                             |
| hexiom                   | 10.4 ms                                                | 6.93 ms: 1.50x faster                                             |
| float                    | 117 ms                                                 | 78.1 ms: 1.50x faster                                             |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.50x faster                                              |
| pyflate                  | 716 ms                                                 | 481 ms: 1.49x faster                                              |
| tornado_http             | 136 ms                                                 | 95.7 ms: 1.43x faster                                             |
| chameleon                | 9.68 ms                                                | 6.88 ms: 1.41x faster                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                            |
| logging_format           | 9.09 us                                                | 6.59 us: 1.38x faster                                             |
| unpickle_pure_python     | 331 us                                                 | 240 us: 1.38x faster                                              |
| scimark_fft              | 466 ms                                                 | 338 ms: 1.38x faster                                              |
| logging_simple           | 8.30 us                                                | 6.08 us: 1.37x faster                                             |
| pprint_safe_repr         | 1.02 sec                                               | 745 ms: 1.37x faster                                              |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                            |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                              |
| html5lib                 | 88.9 ms                                                | 65.7 ms: 1.35x faster                                             |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| scimark_lu               | 176 ms                                                 | 131 ms: 1.34x faster                                              |
| fannkuch                 | 532 ms                                                 | 399 ms: 1.33x faster                                              |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.89 ms: 1.32x faster                                             |
| genshi_text              | 31.8 ms                                                | 24.2 ms: 1.32x faster                                             |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                             |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.31x faster                                             |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                            |
| regex_compile            | 188 ms                                                 | 145 ms: 1.30x faster                                              |
| thrift                   | 1.07 ms                                                | 827 us: 1.30x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.24 us: 1.29x faster                                             |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.27x faster                                              |
| 2to3                     | 348 ms                                                 | 279 ms: 1.25x faster                                              |
| genshi_xml               | 66.0 ms                                                | 53.2 ms: 1.24x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 57.6 ms: 1.20x faster                                             |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                             |
| nqueens                  | 106 ms                                                 | 89.0 ms: 1.19x faster                                             |
| dulwich_log              | 84.3 ms                                                | 71.3 ms: 1.18x faster                                             |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                             |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                             |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                              |
| sympy_str                | 346 ms                                                 | 295 ms: 1.17x faster                                              |
| dask                     | 441 ms                                                 | 377 ms: 1.17x faster                                              |
| bench_thread_pool        | 986 us                                                 | 854 us: 1.16x faster                                              |
| sympy_expand             | 566 ms                                                 | 496 ms: 1.14x faster                                              |
| xml_etree_generate       | 99.4 ms                                                | 87.4 ms: 1.14x faster                                             |
| mypy2                    | 894 ms                                                 | 788 ms: 1.13x faster                                              |
| docutils                 | 3.30 sec                                               | 2.91 sec: 1.13x faster                                            |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                              |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                             |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                              |
| regex_v8                 | 27.8 ms                                                | 26.1 ms: 1.07x faster                                             |
| mdp                      | 2.85 sec                                               | 2.70 sec: 1.06x faster                                            |
| json                     | 5.69 ms                                                | 5.39 ms: 1.05x faster                                             |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                             |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                              |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                              |
| pidigits                 | 191 ms                                                 | 194 ms: 1.01x slower                                              |
| regex_dna                | 227 ms                                                 | 233 ms: 1.03x slower                                              |
| regex_effbot             | 3.63 ms                                                | 3.75 ms: 1.03x slower                                             |
| async_generators         | 444 ms                                                 | 459 ms: 1.03x slower                                              |
| gc_traversal             | 3.62 ms                                                | 3.79 ms: 1.05x slower                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                             |
| pickle                   | 10.7 us                                                | 11.8 us: 1.10x slower                                             |
| unpickle                 | 14.4 us                                                | 15.9 us: 1.11x slower                                             |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                             |
| telco                    | 7.27 ms                                                | 8.65 ms: 1.19x slower                                             |
| coverage                 | 79.4 ms                                                | 101 ms: 1.27x slower                                              |
| unpack_sequence          | 60.0 ns                                                | 89.6 ns: 1.49x slower                                             |
| python_startup_no_site   | 5.93 ms                                                | 9.55 ms: 1.61x slower                                             |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                      |

Benchmark hidden because not significant (3): pickle_list, bench_mp_pool, unpickle_list
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-8eee1b4-JIT/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x