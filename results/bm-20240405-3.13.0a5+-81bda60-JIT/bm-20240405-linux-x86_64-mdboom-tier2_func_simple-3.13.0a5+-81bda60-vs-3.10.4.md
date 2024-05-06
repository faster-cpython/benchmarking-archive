# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 279 ms: 1.25x faster                                                |
| chameleon      | 9.68 ms                                                | 7.07 ms: 1.37x faster                                               |
| docutils       | 3.30 sec                                               | 2.94 sec: 1.12x faster                                              |
| html5lib       | 88.9 ms                                                | 68.7 ms: 1.29x faster                                               |
| tornado_http   | 136 ms                                                 | 96.6 ms: 1.41x faster                                               |
| Geometric mean | (ref)                                                  | 1.29x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 354 ms: 2.05x faster                                                |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.90x faster                                                |
| async_tree_io           | 1.77 sec                                               | 937 ms: 1.89x faster                                                |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.3 ms: 1.66x faster                                               |
| float          | 117 ms                                                 | 77.0 ms: 1.52x faster                                               |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.36x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 144 ms: 1.31x faster                                                |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                               |
| regex_dna      | 227 ms                                                 | 230 ms: 1.02x slower                                                |
| regex_effbot   | 3.63 ms                                                | 3.86 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                                |
| tomli_loads          | 3.14 sec                                               | 2.03 sec: 1.55x faster                                              |
| unpickle_pure_python | 331 us                                                 | 241 us: 1.37x faster                                                |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                               |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.32x faster                                               |
| xml_etree_generate   | 99.4 ms                                                | 87.8 ms: 1.13x faster                                               |
| json_loads           | 31.2 us                                                | 28.2 us: 1.11x faster                                               |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.07x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                                |
| pickle_list          | 5.08 us                                                | 4.99 us: 1.02x faster                                               |
| unpickle_list        | 5.20 us                                                | 5.12 us: 1.01x faster                                               |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                               |
| unpickle             | 14.4 us                                                | 16.1 us: 1.12x slower                                               |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                               |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.33x faster                                               |
| python_startup_no_site | 5.93 ms                                                | 9.45 ms: 1.59x slower                                               |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.52x faster                                               |
| genshi_text    | 31.8 ms                                                | 25.2 ms: 1.27x faster                                               |
| genshi_xml     | 66.0 ms                                                | 54.1 ms: 1.22x faster                                               |
| Geometric mean | (ref)                                                  | 1.33x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.76x faster                                                |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                               |
| deltablue                | 7.91 ms                                                | 3.70 ms: 2.14x faster                                               |
| async_tree_none          | 728 ms                                                 | 354 ms: 2.05x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.90x faster                                                |
| async_tree_io            | 1.77 sec                                               | 937 ms: 1.89x faster                                                |
| richards_super           | 94.7 ms                                                | 50.3 ms: 1.88x faster                                               |
| pylint                   | 551 ms                                                 | 295 ms: 1.87x faster                                                |
| chaos                    | 115 ms                                                 | 62.6 ms: 1.84x faster                                               |
| raytrace                 | 507 ms                                                 | 275 ms: 1.84x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                |
| richards                 | 79.3 ms                                                | 44.2 ms: 1.80x faster                                               |
| logging_silent           | 190 ns                                                 | 106 ns: 1.78x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                               |
| scimark_monte_carlo      | 118 ms                                                 | 70.7 ms: 1.67x faster                                               |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                |
| nbody                    | 154 ms                                                 | 92.3 ms: 1.66x faster                                               |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                               |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.61x faster                                               |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                                |
| scimark_sor              | 220 ms                                                 | 140 ms: 1.57x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                               |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                               |
| tomli_loads              | 3.14 sec                                               | 2.03 sec: 1.55x faster                                              |
| go                       | 240 ms                                                 | 155 ms: 1.55x faster                                                |
| pyflate                  | 716 ms                                                 | 468 ms: 1.53x faster                                                |
| float                    | 117 ms                                                 | 77.0 ms: 1.52x faster                                               |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 39.0 us: 1.50x faster                                               |
| hexiom                   | 10.4 ms                                                | 7.01 ms: 1.48x faster                                               |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.47x faster                                                |
| logging_simple           | 8.30 us                                                | 5.83 us: 1.42x faster                                               |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                               |
| tornado_http             | 136 ms                                                 | 96.6 ms: 1.41x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                              |
| unpickle_pure_python     | 331 us                                                 | 241 us: 1.37x faster                                                |
| chameleon                | 9.68 ms                                                | 7.07 ms: 1.37x faster                                               |
| scimark_fft              | 466 ms                                                 | 341 ms: 1.36x faster                                                |
| fannkuch                 | 532 ms                                                 | 393 ms: 1.35x faster                                                |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                               |
| pprint_safe_repr         | 1.02 sec                                               | 762 ms: 1.34x faster                                                |
| scimark_lu               | 176 ms                                                 | 132 ms: 1.33x faster                                                |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.33x faster                                               |
| deepcopy                 | 479 us                                                 | 363 us: 1.32x faster                                                |
| pprint_pformat           | 2.10 sec                                               | 1.59 sec: 1.32x faster                                              |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.32x faster                                               |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.94 ms: 1.31x faster                                               |
| regex_compile            | 188 ms                                                 | 144 ms: 1.31x faster                                                |
| thrift                   | 1.07 ms                                                | 828 us: 1.30x faster                                                |
| html5lib                 | 88.9 ms                                                | 68.7 ms: 1.29x faster                                               |
| pycparser                | 1.58 sec                                               | 1.22 sec: 1.29x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.25 us: 1.28x faster                                               |
| genshi_text              | 31.8 ms                                                | 25.2 ms: 1.27x faster                                               |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                |
| 2to3                     | 348 ms                                                 | 279 ms: 1.25x faster                                                |
| genshi_xml               | 66.0 ms                                                | 54.1 ms: 1.22x faster                                               |
| dulwich_log              | 84.3 ms                                                | 70.1 ms: 1.20x faster                                               |
| sqlglot_optimize         | 69.2 ms                                                | 57.6 ms: 1.20x faster                                               |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                               |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                               |
| dask                     | 441 ms                                                 | 375 ms: 1.18x faster                                                |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                |
| nqueens                  | 106 ms                                                 | 90.5 ms: 1.17x faster                                               |
| sympy_integrate          | 25.8 ms                                                | 22.1 ms: 1.17x faster                                               |
| sympy_str                | 346 ms                                                 | 297 ms: 1.16x faster                                                |
| bench_thread_pool        | 986 us                                                 | 857 us: 1.15x faster                                                |
| sympy_expand             | 566 ms                                                 | 496 ms: 1.14x faster                                                |
| mypy2                    | 894 ms                                                 | 786 ms: 1.14x faster                                                |
| xml_etree_generate       | 99.4 ms                                                | 87.8 ms: 1.13x faster                                               |
| docutils                 | 3.30 sec                                               | 2.94 sec: 1.12x faster                                              |
| json_loads               | 31.2 us                                                | 28.2 us: 1.11x faster                                               |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                               |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                |
| pathlib                  | 20.5 ms                                                | 19.0 ms: 1.08x faster                                               |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.07x faster                                                |
| json                     | 5.69 ms                                                | 5.36 ms: 1.06x faster                                               |
| sqlite_synth             | 3.02 us                                                | 2.88 us: 1.05x faster                                               |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                                |
| mdp                      | 2.85 sec                                               | 2.77 sec: 1.03x faster                                              |
| pickle_list              | 5.08 us                                                | 4.99 us: 1.02x faster                                               |
| unpickle_list            | 5.20 us                                                | 5.12 us: 1.01x faster                                               |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                |
| regex_dna                | 227 ms                                                 | 230 ms: 1.02x slower                                                |
| async_generators         | 444 ms                                                 | 461 ms: 1.04x slower                                                |
| gc_traversal             | 3.62 ms                                                | 3.77 ms: 1.04x slower                                               |
| regex_effbot             | 3.63 ms                                                | 3.86 ms: 1.06x slower                                               |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.07x slower                                               |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                               |
| unpickle                 | 14.4 us                                                | 16.1 us: 1.12x slower                                               |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                               |
| telco                    | 7.27 ms                                                | 8.68 ms: 1.20x slower                                               |
| coverage                 | 79.4 ms                                                | 98.9 ms: 1.24x slower                                               |
| python_startup_no_site   | 5.93 ms                                                | 9.45 ms: 1.59x slower                                               |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                        |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x