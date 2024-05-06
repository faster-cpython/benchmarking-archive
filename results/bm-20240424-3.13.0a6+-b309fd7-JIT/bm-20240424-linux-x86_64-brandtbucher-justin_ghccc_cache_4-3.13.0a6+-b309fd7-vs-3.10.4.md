# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache_4
- machine: linux-x86_64
- commit hash: b309fd7
- commit date: 2024-04-24
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 290 ms: 1.20x faster                                                         |
| chameleon      | 9.68 ms                                                | 7.24 ms: 1.34x faster                                                        |
| docutils       | 3.30 sec                                               | 3.00 sec: 1.10x faster                                                       |
| html5lib       | 88.9 ms                                                | 70.0 ms: 1.27x faster                                                        |
| tornado_http   | 136 ms                                                 | 98.0 ms: 1.39x faster                                                        |
| Geometric mean | (ref)                                                  | 1.26x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 367 ms: 1.98x faster                                                         |
| async_tree_io           | 1.77 sec                                               | 940 ms: 1.88x faster                                                         |
| async_tree_memoization  | 870 ms                                                 | 478 ms: 1.82x faster                                                         |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 624 ms: 1.63x faster                                                         |
| Geometric mean          | (ref)                                                  | 1.82x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 83.1 ms: 1.85x faster                                                        |
| float          | 117 ms                                                 | 75.3 ms: 1.55x faster                                                        |
| pidigits       | 191 ms                                                 | 210 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 24.5 ms: 1.13x faster                                                        |
| regex_compile  | 188 ms                                                 | 171 ms: 1.10x faster                                                         |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                         |
| regex_effbot   | 3.63 ms                                                | 4.23 ms: 1.17x slower                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 309 us: 1.57x faster                                                         |
| tomli_loads          | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 240 us: 1.37x faster                                                         |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                        |
| xml_etree_process    | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                        |
| json_loads           | 31.2 us                                                | 27.4 us: 1.14x faster                                                        |
| xml_etree_parse      | 168 ms                                                 | 148 ms: 1.13x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 88.1 ms: 1.13x faster                                                        |
| xml_etree_iterparse  | 115 ms                                                 | 104 ms: 1.12x faster                                                         |
| unpickle_list        | 5.20 us                                                | 5.34 us: 1.03x slower                                                        |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                        |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                        |
| pickle_dict          | 29.6 us                                                | 34.9 us: 1.18x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                        |
| python_startup_no_site | 5.93 ms                                                | 7.71 ms: 1.30x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                        |
| django_template | 48.2 ms                                                | 37.5 ms: 1.28x faster                                                        |
| genshi_text     | 31.8 ms                                                | 25.2 ms: 1.26x faster                                                        |
| genshi_xml      | 66.0 ms                                                | 61.1 ms: 1.08x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.28x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 116 us: 4.70x faster                                                         |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                        |
| deltablue                | 7.91 ms                                                | 3.77 ms: 2.10x faster                                                        |
| async_tree_none          | 728 ms                                                 | 367 ms: 1.98x faster                                                         |
| async_tree_io            | 1.77 sec                                               | 940 ms: 1.88x faster                                                         |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                         |
| nbody                    | 154 ms                                                 | 83.1 ms: 1.85x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 478 ms: 1.82x faster                                                         |
| asyncio_tcp              | 922 ms                                                 | 517 ms: 1.78x faster                                                         |
| raytrace                 | 507 ms                                                 | 288 ms: 1.76x faster                                                         |
| richards_super           | 94.7 ms                                                | 54.3 ms: 1.75x faster                                                        |
| crypto_pyaes             | 128 ms                                                 | 73.7 ms: 1.73x faster                                                        |
| chaos                    | 115 ms                                                 | 67.4 ms: 1.71x faster                                                        |
| richards                 | 79.3 ms                                                | 47.7 ms: 1.66x faster                                                        |
| scimark_sor              | 220 ms                                                 | 133 ms: 1.65x faster                                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 624 ms: 1.63x faster                                                         |
| pylint                   | 551 ms                                                 | 341 ms: 1.62x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 74.6 ms: 1.58x faster                                                        |
| spectral_norm            | 170 ms                                                 | 108 ms: 1.57x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.38 ms: 1.57x faster                                                        |
| pickle_pure_python       | 484 us                                                 | 309 us: 1.57x faster                                                         |
| float                    | 117 ms                                                 | 75.3 ms: 1.55x faster                                                        |
| go                       | 240 ms                                                 | 155 ms: 1.55x faster                                                         |
| coroutines               | 35.1 ms                                                | 22.9 ms: 1.53x faster                                                        |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                        |
| comprehensions           | 28.8 us                                                | 19.0 us: 1.52x faster                                                        |
| sqlglot_transpile        | 2.57 ms                                                | 1.70 ms: 1.51x faster                                                        |
| tomli_loads              | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                       |
| deepcopy_memo            | 58.5 us                                                | 40.1 us: 1.46x faster                                                        |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.55 ms: 1.42x faster                                                        |
| scimark_fft              | 466 ms                                                 | 333 ms: 1.40x faster                                                         |
| pyflate                  | 716 ms                                                 | 514 ms: 1.39x faster                                                         |
| tornado_http             | 136 ms                                                 | 98.0 ms: 1.39x faster                                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                       |
| unpickle_pure_python     | 331 us                                                 | 240 us: 1.37x faster                                                         |
| fannkuch                 | 532 ms                                                 | 391 ms: 1.36x faster                                                         |
| logging_simple           | 8.30 us                                                | 6.11 us: 1.36x faster                                                        |
| scimark_lu               | 176 ms                                                 | 130 ms: 1.36x faster                                                         |
| logging_format           | 9.09 us                                                | 6.70 us: 1.36x faster                                                        |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                        |
| chameleon                | 9.68 ms                                                | 7.24 ms: 1.34x faster                                                        |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                        |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                       |
| thrift                   | 1.07 ms                                                | 829 us: 1.29x faster                                                         |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                        |
| deepcopy                 | 479 us                                                 | 372 us: 1.29x faster                                                         |
| django_template          | 48.2 ms                                                | 37.5 ms: 1.28x faster                                                        |
| html5lib                 | 88.9 ms                                                | 70.0 ms: 1.27x faster                                                        |
| hexiom                   | 10.4 ms                                                | 8.20 ms: 1.27x faster                                                        |
| genshi_text              | 31.8 ms                                                | 25.2 ms: 1.26x faster                                                        |
| sqlglot_normalize        | 143 ms                                                 | 116 ms: 1.23x faster                                                         |
| 2to3                     | 348 ms                                                 | 290 ms: 1.20x faster                                                         |
| djangocms                | 38.4 us                                                | 32.5 us: 1.18x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.23 ms: 1.17x faster                                                        |
| dulwich_log              | 84.3 ms                                                | 72.2 ms: 1.17x faster                                                        |
| sqlglot_optimize         | 69.2 ms                                                | 59.5 ms: 1.16x faster                                                        |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                        |
| dask                     | 441 ms                                                 | 380 ms: 1.16x faster                                                         |
| json_loads               | 31.2 us                                                | 27.4 us: 1.14x faster                                                        |
| pathlib                  | 20.5 ms                                                | 18.0 ms: 1.14x faster                                                        |
| xml_etree_parse          | 168 ms                                                 | 148 ms: 1.13x faster                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 897 ms: 1.13x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 24.5 ms: 1.13x faster                                                        |
| sympy_sum                | 196 ms                                                 | 174 ms: 1.13x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 22.8 ms: 1.13x faster                                                        |
| bench_thread_pool        | 986 us                                                 | 874 us: 1.13x faster                                                         |
| xml_etree_generate       | 99.4 ms                                                | 88.1 ms: 1.13x faster                                                        |
| xml_etree_iterparse      | 115 ms                                                 | 104 ms: 1.12x faster                                                         |
| sympy_str                | 346 ms                                                 | 310 ms: 1.11x faster                                                         |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                                        |
| nqueens                  | 106 ms                                                 | 95.5 ms: 1.11x faster                                                        |
| mypy2                    | 894 ms                                                 | 809 ms: 1.11x faster                                                         |
| regex_compile            | 188 ms                                                 | 171 ms: 1.10x faster                                                         |
| docutils                 | 3.30 sec                                               | 3.00 sec: 1.10x faster                                                       |
| pprint_pformat           | 2.10 sec                                               | 1.94 sec: 1.09x faster                                                       |
| genshi_xml               | 66.0 ms                                                | 61.1 ms: 1.08x faster                                                        |
| sympy_expand             | 566 ms                                                 | 524 ms: 1.08x faster                                                         |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.68 sec: 1.06x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                                        |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                         |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                         |
| unpickle_list            | 5.20 us                                                | 5.34 us: 1.03x slower                                                        |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                        |
| async_generators         | 444 ms                                                 | 471 ms: 1.06x slower                                                         |
| gc_traversal             | 3.62 ms                                                | 3.93 ms: 1.09x slower                                                        |
| pidigits                 | 191 ms                                                 | 210 ms: 1.10x slower                                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.79 ms: 1.10x slower                                                        |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                        |
| regex_effbot             | 3.63 ms                                                | 4.23 ms: 1.17x slower                                                        |
| pickle_dict              | 29.6 us                                                | 34.9 us: 1.18x slower                                                        |
| telco                    | 7.27 ms                                                | 8.84 ms: 1.22x slower                                                        |
| coverage                 | 79.4 ms                                                | 98.3 ms: 1.24x slower                                                        |
| python_startup_no_site   | 5.93 ms                                                | 7.71 ms: 1.30x slower                                                        |
| Geometric mean           | (ref)                                                  | 1.29x faster                                                                 |

Benchmark hidden because not significant (2): bench_mp_pool, pickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240424-3.13.0a6+-b309fd7-JIT/bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.24x