# Results vs. 3.10.4

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 277 ms: 1.26x faster                                          |
| chameleon      | 9.68 ms                                                | 6.86 ms: 1.41x faster                                         |
| docutils       | 3.30 sec                                               | 2.92 sec: 1.13x faster                                        |
| html5lib       | 88.9 ms                                                | 67.7 ms: 1.31x faster                                         |
| tornado_http   | 136 ms                                                 | 96.1 ms: 1.42x faster                                         |
| Geometric mean | (ref)                                                  | 1.30x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                          |
| async_tree_memoization  | 870 ms                                                 | 458 ms: 1.90x faster                                          |
| async_tree_io           | 1.77 sec                                               | 932 ms: 1.90x faster                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                          |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.1 ms: 1.68x faster                                         |
| float          | 117 ms                                                 | 76.9 ms: 1.52x faster                                         |
| pidigits       | 191 ms                                                 | 207 ms: 1.08x slower                                          |
| Geometric mean | (ref)                                                  | 1.33x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 147 ms: 1.28x faster                                          |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.07x faster                                         |
| regex_dna      | 227 ms                                                 | 233 ms: 1.03x slower                                          |
| regex_effbot   | 3.63 ms                                                | 3.78 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                  | 1.07x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                          |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                        |
| unpickle_pure_python | 331 us                                                 | 239 us: 1.38x faster                                          |
| json_dumps           | 14.2 ms                                                | 10.4 ms: 1.36x faster                                         |
| xml_etree_process    | 79.1 ms                                                | 59.6 ms: 1.33x faster                                         |
| xml_etree_generate   | 99.4 ms                                                | 86.5 ms: 1.15x faster                                         |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                         |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                          |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                          |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                         |
| unpickle_list        | 5.20 us                                                | 5.29 us: 1.02x slower                                         |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                         |
| unpickle             | 14.4 us                                                | 16.2 us: 1.13x slower                                         |
| pickle_dict          | 29.6 us                                                | 33.9 us: 1.15x slower                                         |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                         |
| python_startup_no_site | 5.93 ms                                                | 9.52 ms: 1.61x slower                                         |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.8 ms: 1.51x faster                                         |
| genshi_text    | 31.8 ms                                                | 24.8 ms: 1.28x faster                                         |
| genshi_xml     | 66.0 ms                                                | 55.4 ms: 1.19x faster                                         |
| Geometric mean | (ref)                                                  | 1.32x faster                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.77x faster                                          |
| generators               | 80.1 ms                                                | 29.5 ms: 2.71x faster                                         |
| deltablue                | 7.91 ms                                                | 3.45 ms: 2.30x faster                                         |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                          |
| async_tree_memoization   | 870 ms                                                 | 458 ms: 1.90x faster                                          |
| async_tree_io            | 1.77 sec                                               | 932 ms: 1.90x faster                                          |
| chaos                    | 115 ms                                                 | 61.8 ms: 1.87x faster                                         |
| pylint                   | 551 ms                                                 | 297 ms: 1.86x faster                                          |
| logging_silent           | 190 ns                                                 | 103 ns: 1.85x faster                                          |
| raytrace                 | 507 ms                                                 | 279 ms: 1.81x faster                                          |
| richards_super           | 94.7 ms                                                | 52.7 ms: 1.80x faster                                         |
| asyncio_tcp              | 922 ms                                                 | 515 ms: 1.79x faster                                          |
| scimark_monte_carlo      | 118 ms                                                 | 68.8 ms: 1.72x faster                                         |
| richards                 | 79.3 ms                                                | 46.3 ms: 1.71x faster                                         |
| crypto_pyaes             | 128 ms                                                 | 75.5 ms: 1.69x faster                                         |
| nbody                    | 154 ms                                                 | 91.1 ms: 1.68x faster                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                          |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                         |
| scimark_sor              | 220 ms                                                 | 136 ms: 1.62x faster                                          |
| comprehensions           | 28.8 us                                                | 18.1 us: 1.59x faster                                         |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                         |
| go                       | 240 ms                                                 | 154 ms: 1.55x faster                                          |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.54x faster                                         |
| float                    | 117 ms                                                 | 76.9 ms: 1.52x faster                                         |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                        |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                         |
| deepcopy_memo            | 58.5 us                                                | 38.8 us: 1.51x faster                                         |
| pyflate                  | 716 ms                                                 | 476 ms: 1.50x faster                                          |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.47x faster                                          |
| hexiom                   | 10.4 ms                                                | 7.10 ms: 1.46x faster                                         |
| tornado_http             | 136 ms                                                 | 96.1 ms: 1.42x faster                                         |
| chameleon                | 9.68 ms                                                | 6.86 ms: 1.41x faster                                         |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.39x faster                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.39x faster                                        |
| logging_simple           | 8.30 us                                                | 5.99 us: 1.39x faster                                         |
| unpickle_pure_python     | 331 us                                                 | 239 us: 1.38x faster                                          |
| logging_format           | 9.09 us                                                | 6.62 us: 1.37x faster                                         |
| pprint_safe_repr         | 1.02 sec                                               | 748 ms: 1.36x faster                                          |
| json_dumps               | 14.2 ms                                                | 10.4 ms: 1.36x faster                                         |
| scimark_fft              | 466 ms                                                 | 343 ms: 1.36x faster                                          |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                          |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.84 ms: 1.34x faster                                         |
| xml_etree_process        | 79.1 ms                                                | 59.6 ms: 1.33x faster                                         |
| fannkuch                 | 532 ms                                                 | 401 ms: 1.32x faster                                          |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.32x faster                                          |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                         |
| html5lib                 | 88.9 ms                                                | 67.7 ms: 1.31x faster                                         |
| thrift                   | 1.07 ms                                                | 823 us: 1.30x faster                                          |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                        |
| genshi_text              | 31.8 ms                                                | 24.8 ms: 1.28x faster                                         |
| regex_compile            | 188 ms                                                 | 147 ms: 1.28x faster                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.27 us: 1.27x faster                                         |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.27x faster                                          |
| 2to3                     | 348 ms                                                 | 277 ms: 1.26x faster                                          |
| sqlglot_optimize         | 69.2 ms                                                | 57.7 ms: 1.20x faster                                         |
| genshi_xml               | 66.0 ms                                                | 55.4 ms: 1.19x faster                                         |
| dulwich_log              | 84.3 ms                                                | 70.9 ms: 1.19x faster                                         |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                         |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                         |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                          |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.18x faster                                          |
| sympy_str                | 346 ms                                                 | 295 ms: 1.17x faster                                          |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                         |
| xml_etree_generate       | 99.4 ms                                                | 86.5 ms: 1.15x faster                                         |
| bench_thread_pool        | 986 us                                                 | 858 us: 1.15x faster                                          |
| sympy_expand             | 566 ms                                                 | 493 ms: 1.15x faster                                          |
| nqueens                  | 106 ms                                                 | 92.2 ms: 1.15x faster                                         |
| mypy2                    | 894 ms                                                 | 788 ms: 1.13x faster                                          |
| docutils                 | 3.30 sec                                               | 2.92 sec: 1.13x faster                                        |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                         |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                          |
| pathlib                  | 20.5 ms                                                | 18.9 ms: 1.08x faster                                         |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.07x faster                                         |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                          |
| json                     | 5.69 ms                                                | 5.36 ms: 1.06x faster                                         |
| sqlite_synth             | 3.02 us                                                | 2.88 us: 1.05x faster                                         |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                          |
| pickle_list              | 5.08 us                                                | 4.96 us: 1.02x faster                                         |
| mdp                      | 2.85 sec                                               | 2.83 sec: 1.01x faster                                        |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                          |
| unpickle_list            | 5.20 us                                                | 5.29 us: 1.02x slower                                         |
| regex_dna                | 227 ms                                                 | 233 ms: 1.03x slower                                          |
| async_generators         | 444 ms                                                 | 461 ms: 1.04x slower                                          |
| regex_effbot             | 3.63 ms                                                | 3.78 ms: 1.04x slower                                         |
| gc_traversal             | 3.62 ms                                                | 3.80 ms: 1.05x slower                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                         |
| pidigits                 | 191 ms                                                 | 207 ms: 1.08x slower                                          |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                         |
| unpickle                 | 14.4 us                                                | 16.2 us: 1.13x slower                                         |
| pickle_dict              | 29.6 us                                                | 33.9 us: 1.15x slower                                         |
| telco                    | 7.27 ms                                                | 8.49 ms: 1.17x slower                                         |
| coverage                 | 79.4 ms                                                | 100 ms: 1.26x slower                                          |
| python_startup_no_site   | 5.93 ms                                                | 9.52 ms: 1.61x slower                                         |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                  |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-c35ee28-JIT/bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x