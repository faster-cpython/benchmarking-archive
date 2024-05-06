# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: b917d1f
- commit date: 2024-04-03
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 278 ms: 1.25x faster                                          |
| chameleon      | 9.68 ms                                                | 6.92 ms: 1.40x faster                                         |
| docutils       | 3.30 sec                                               | 2.89 sec: 1.14x faster                                        |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                         |
| tornado_http   | 136 ms                                                 | 97.0 ms: 1.41x faster                                         |
| Geometric mean | (ref)                                                  | 1.30x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 457 ms: 1.90x faster                                          |
| async_tree_none         | 728 ms                                                 | 390 ms: 1.87x faster                                          |
| async_tree_io           | 1.77 sec                                               | 951 ms: 1.86x faster                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 600 ms: 1.69x faster                                          |
| Geometric mean          | (ref)                                                  | 1.83x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.8 ms: 1.65x faster                                         |
| float          | 117 ms                                                 | 77.6 ms: 1.51x faster                                         |
| pidigits       | 191 ms                                                 | 190 ms: 1.00x faster                                          |
| Geometric mean | (ref)                                                  | 1.36x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 147 ms: 1.28x faster                                          |
| regex_v8       | 27.8 ms                                                | 25.9 ms: 1.07x faster                                         |
| regex_dna      | 227 ms                                                 | 229 ms: 1.01x slower                                          |
| regex_effbot   | 3.63 ms                                                | 3.75 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                  | 1.07x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 307 us: 1.58x faster                                          |
| tomli_loads          | 3.14 sec                                               | 2.08 sec: 1.51x faster                                        |
| unpickle_pure_python | 331 us                                                 | 239 us: 1.38x faster                                          |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.34x faster                                         |
| xml_etree_process    | 79.1 ms                                                | 59.9 ms: 1.32x faster                                         |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                         |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                         |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                          |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                          |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                         |
| unpickle_list        | 5.20 us                                                | 5.14 us: 1.01x faster                                         |
| pickle               | 10.7 us                                                | 11.8 us: 1.10x slower                                         |
| unpickle             | 14.4 us                                                | 16.0 us: 1.11x slower                                         |
| pickle_dict          | 29.6 us                                                | 34.5 us: 1.16x slower                                         |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                         |
| python_startup_no_site | 5.93 ms                                                | 9.57 ms: 1.61x slower                                         |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                         |
| django_template | 48.2 ms                                                | 36.3 ms: 1.33x faster                                         |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                         |
| genshi_xml      | 66.0 ms                                                | 55.3 ms: 1.19x faster                                         |
| Geometric mean  | (ref)                                                  | 1.33x faster                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 110 us: 4.93x faster                                          |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                         |
| deltablue                | 7.91 ms                                                | 3.47 ms: 2.28x faster                                         |
| async_tree_memoization   | 870 ms                                                 | 457 ms: 1.90x faster                                          |
| async_tree_none          | 728 ms                                                 | 390 ms: 1.87x faster                                          |
| async_tree_io            | 1.77 sec                                               | 951 ms: 1.86x faster                                          |
| chaos                    | 115 ms                                                 | 63.0 ms: 1.83x faster                                         |
| logging_silent           | 190 ns                                                 | 104 ns: 1.82x faster                                          |
| asyncio_tcp              | 922 ms                                                 | 508 ms: 1.82x faster                                          |
| richards_super           | 94.7 ms                                                | 53.6 ms: 1.77x faster                                         |
| raytrace                 | 507 ms                                                 | 294 ms: 1.72x faster                                          |
| crypto_pyaes             | 128 ms                                                 | 74.5 ms: 1.72x faster                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 600 ms: 1.69x faster                                          |
| scimark_monte_carlo      | 118 ms                                                 | 69.8 ms: 1.69x faster                                         |
| richards                 | 79.3 ms                                                | 46.9 ms: 1.69x faster                                         |
| scimark_sor              | 220 ms                                                 | 131 ms: 1.68x faster                                          |
| nbody                    | 154 ms                                                 | 92.8 ms: 1.65x faster                                         |
| pylint                   | 551 ms                                                 | 336 ms: 1.64x faster                                          |
| sqlglot_parse            | 2.17 ms                                                | 1.34 ms: 1.62x faster                                         |
| pickle_pure_python       | 484 us                                                 | 307 us: 1.58x faster                                          |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.57x faster                                         |
| comprehensions           | 28.8 us                                                | 18.5 us: 1.56x faster                                         |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                         |
| go                       | 240 ms                                                 | 157 ms: 1.53x faster                                          |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                         |
| tomli_loads              | 3.14 sec                                               | 2.08 sec: 1.51x faster                                        |
| float                    | 117 ms                                                 | 77.6 ms: 1.51x faster                                         |
| deepcopy_memo            | 58.5 us                                                | 39.1 us: 1.49x faster                                         |
| pyflate                  | 716 ms                                                 | 483 ms: 1.48x faster                                          |
| spectral_norm            | 170 ms                                                 | 118 ms: 1.44x faster                                          |
| hexiom                   | 10.4 ms                                                | 7.33 ms: 1.42x faster                                         |
| tornado_http             | 136 ms                                                 | 97.0 ms: 1.41x faster                                         |
| chameleon                | 9.68 ms                                                | 6.92 ms: 1.40x faster                                         |
| logging_simple           | 8.30 us                                                | 5.97 us: 1.39x faster                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.39x faster                                        |
| unpickle_pure_python     | 331 us                                                 | 239 us: 1.38x faster                                          |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                        |
| logging_format           | 9.09 us                                                | 6.67 us: 1.36x faster                                         |
| scimark_fft              | 466 ms                                                 | 345 ms: 1.35x faster                                          |
| pprint_safe_repr         | 1.02 sec                                               | 755 ms: 1.35x faster                                          |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.34x faster                                         |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                          |
| deepcopy                 | 479 us                                                 | 360 us: 1.33x faster                                          |
| django_template          | 48.2 ms                                                | 36.3 ms: 1.33x faster                                         |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.33x faster                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.16 us: 1.32x faster                                         |
| xml_etree_process        | 79.1 ms                                                | 59.9 ms: 1.32x faster                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.93 ms: 1.31x faster                                         |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                          |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                         |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                         |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                         |
| regex_compile            | 188 ms                                                 | 147 ms: 1.28x faster                                          |
| pycparser                | 1.58 sec                                               | 1.23 sec: 1.28x faster                                        |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                          |
| 2to3                     | 348 ms                                                 | 278 ms: 1.25x faster                                          |
| djangocms                | 38.4 us                                                | 30.8 us: 1.25x faster                                         |
| sqlglot_optimize         | 69.2 ms                                                | 57.9 ms: 1.20x faster                                         |
| dulwich_log              | 84.3 ms                                                | 70.6 ms: 1.19x faster                                         |
| genshi_xml               | 66.0 ms                                                | 55.3 ms: 1.19x faster                                         |
| sympy_str                | 346 ms                                                 | 290 ms: 1.19x faster                                          |
| sympy_sum                | 196 ms                                                 | 165 ms: 1.19x faster                                          |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                         |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                         |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                         |
| nqueens                  | 106 ms                                                 | 90.7 ms: 1.17x faster                                         |
| dask                     | 441 ms                                                 | 379 ms: 1.16x faster                                          |
| sympy_expand             | 566 ms                                                 | 489 ms: 1.16x faster                                          |
| bench_thread_pool        | 986 us                                                 | 855 us: 1.15x faster                                          |
| docutils                 | 3.30 sec                                               | 2.89 sec: 1.14x faster                                        |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                         |
| mypy2                    | 894 ms                                                 | 787 ms: 1.14x faster                                          |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                         |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                          |
| regex_v8                 | 27.8 ms                                                | 25.9 ms: 1.07x faster                                         |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                        |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                          |
| pathlib                  | 20.5 ms                                                | 19.2 ms: 1.07x faster                                         |
| json                     | 5.69 ms                                                | 5.37 ms: 1.06x faster                                         |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                          |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                         |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                         |
| unpickle_list            | 5.20 us                                                | 5.14 us: 1.01x faster                                         |
| pidigits                 | 191 ms                                                 | 190 ms: 1.00x faster                                          |
| regex_dna                | 227 ms                                                 | 229 ms: 1.01x slower                                          |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                          |
| regex_effbot             | 3.63 ms                                                | 3.75 ms: 1.03x slower                                         |
| async_generators         | 444 ms                                                 | 461 ms: 1.04x slower                                          |
| create_gc_cycles         | 1.62 ms                                                | 1.69 ms: 1.05x slower                                         |
| gc_traversal             | 3.62 ms                                                | 3.94 ms: 1.09x slower                                         |
| pickle                   | 10.7 us                                                | 11.8 us: 1.10x slower                                         |
| unpickle                 | 14.4 us                                                | 16.0 us: 1.11x slower                                         |
| pickle_dict              | 29.6 us                                                | 34.5 us: 1.16x slower                                         |
| telco                    | 7.27 ms                                                | 8.73 ms: 1.20x slower                                         |
| coverage                 | 79.4 ms                                                | 97.0 ms: 1.22x slower                                         |
| python_startup_no_site   | 5.93 ms                                                | 9.57 ms: 1.61x slower                                         |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                  |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-b917d1f-JIT/bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x