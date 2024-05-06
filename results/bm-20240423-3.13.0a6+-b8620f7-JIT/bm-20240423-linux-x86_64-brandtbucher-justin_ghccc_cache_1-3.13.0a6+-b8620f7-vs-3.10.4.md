# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache_1
- machine: linux-x86_64
- commit hash: b8620f7
- commit date: 2024-04-23
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 277 ms: 1.26x faster                                                         |
| chameleon      | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                        |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                       |
| html5lib       | 88.9 ms                                                | 68.8 ms: 1.29x faster                                                        |
| tornado_http   | 136 ms                                                 | 95.7 ms: 1.42x faster                                                        |
| Geometric mean | (ref)                                                  | 1.29x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 359 ms: 2.03x faster                                                         |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                         |
| async_tree_io           | 1.77 sec                                               | 949 ms: 1.86x faster                                                         |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                                         |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 81.0 ms: 1.90x faster                                                        |
| float          | 117 ms                                                 | 73.7 ms: 1.59x faster                                                        |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.45x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                         |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                        |
| regex_dna      | 227 ms                                                 | 229 ms: 1.01x slower                                                         |
| regex_effbot   | 3.63 ms                                                | 4.21 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.92 sec: 1.64x faster                                                       |
| pickle_pure_python   | 484 us                                                 | 309 us: 1.57x faster                                                         |
| unpickle_pure_python | 331 us                                                 | 223 us: 1.48x faster                                                         |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                        |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                        |
| json_loads           | 31.2 us                                                | 27.3 us: 1.14x faster                                                        |
| xml_etree_iterparse  | 115 ms                                                 | 101 ms: 1.14x faster                                                         |
| xml_etree_generate   | 99.4 ms                                                | 87.6 ms: 1.13x faster                                                        |
| xml_etree_parse      | 168 ms                                                 | 148 ms: 1.13x faster                                                         |
| pickle_list          | 5.08 us                                                | 5.06 us: 1.00x faster                                                        |
| unpickle             | 14.4 us                                                | 15.3 us: 1.06x slower                                                        |
| pickle               | 10.7 us                                                | 11.8 us: 1.10x slower                                                        |
| pickle_dict          | 29.6 us                                                | 35.6 us: 1.20x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                        |
| python_startup_no_site | 5.93 ms                                                | 7.68 ms: 1.30x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 9.91 ms: 1.65x faster                                                        |
| django_template | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                        |
| genshi_text     | 31.8 ms                                                | 24.1 ms: 1.32x faster                                                        |
| genshi_xml      | 66.0 ms                                                | 55.9 ms: 1.18x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.73x faster                                                         |
| generators               | 80.1 ms                                                | 29.9 ms: 2.67x faster                                                        |
| deltablue                | 7.91 ms                                                | 3.64 ms: 2.17x faster                                                        |
| async_tree_none          | 728 ms                                                 | 359 ms: 2.03x faster                                                         |
| richards_super           | 94.7 ms                                                | 49.1 ms: 1.93x faster                                                        |
| logging_silent           | 190 ns                                                 | 99.0 ns: 1.92x faster                                                        |
| nbody                    | 154 ms                                                 | 81.0 ms: 1.90x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                         |
| richards                 | 79.3 ms                                                | 42.4 ms: 1.87x faster                                                        |
| chaos                    | 115 ms                                                 | 61.8 ms: 1.87x faster                                                        |
| async_tree_io            | 1.77 sec                                               | 949 ms: 1.86x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 63.6 ms: 1.86x faster                                                        |
| crypto_pyaes             | 128 ms                                                 | 68.9 ms: 1.85x faster                                                        |
| raytrace                 | 507 ms                                                 | 274 ms: 1.85x faster                                                         |
| asyncio_tcp              | 922 ms                                                 | 515 ms: 1.79x faster                                                         |
| spectral_norm            | 170 ms                                                 | 98.5 ms: 1.72x faster                                                        |
| scimark_sor              | 220 ms                                                 | 129 ms: 1.71x faster                                                         |
| comprehensions           | 28.8 us                                                | 16.9 us: 1.70x faster                                                        |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                                         |
| pylint                   | 551 ms                                                 | 333 ms: 1.66x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.65x faster                                                        |
| mako                     | 16.3 ms                                                | 9.91 ms: 1.65x faster                                                        |
| tomli_loads              | 3.14 sec                                               | 1.92 sec: 1.64x faster                                                       |
| go                       | 240 ms                                                 | 148 ms: 1.63x faster                                                         |
| pyflate                  | 716 ms                                                 | 443 ms: 1.62x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.54 ms: 1.59x faster                                                        |
| float                    | 117 ms                                                 | 73.7 ms: 1.59x faster                                                        |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.57x faster                                                        |
| pickle_pure_python       | 484 us                                                 | 309 us: 1.57x faster                                                         |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                        |
| scimark_fft              | 466 ms                                                 | 310 ms: 1.50x faster                                                         |
| deepcopy_memo            | 58.5 us                                                | 39.1 us: 1.50x faster                                                        |
| fannkuch                 | 532 ms                                                 | 356 ms: 1.49x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 223 us: 1.48x faster                                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.42 ms: 1.46x faster                                                        |
| logging_simple           | 8.30 us                                                | 5.76 us: 1.44x faster                                                        |
| tornado_http             | 136 ms                                                 | 95.7 ms: 1.42x faster                                                        |
| pprint_pformat           | 2.10 sec                                               | 1.48 sec: 1.42x faster                                                       |
| pprint_safe_repr         | 1.02 sec                                               | 717 ms: 1.42x faster                                                         |
| logging_format           | 9.09 us                                                | 6.41 us: 1.42x faster                                                        |
| scimark_lu               | 176 ms                                                 | 125 ms: 1.40x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                       |
| chameleon                | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                        |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                         |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                                       |
| django_template          | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                        |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                        |
| genshi_text              | 31.8 ms                                                | 24.1 ms: 1.32x faster                                                        |
| deepcopy                 | 479 us                                                 | 364 us: 1.32x faster                                                         |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                        |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                        |
| thrift                   | 1.07 ms                                                | 827 us: 1.30x faster                                                         |
| html5lib                 | 88.9 ms                                                | 68.8 ms: 1.29x faster                                                        |
| 2to3                     | 348 ms                                                 | 277 ms: 1.26x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                         |
| dulwich_log              | 84.3 ms                                                | 69.0 ms: 1.22x faster                                                        |
| nqueens                  | 106 ms                                                 | 86.7 ms: 1.22x faster                                                        |
| sqlglot_optimize         | 69.2 ms                                                | 57.1 ms: 1.21x faster                                                        |
| djangocms                | 38.4 us                                                | 32.3 us: 1.19x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                        |
| genshi_xml               | 66.0 ms                                                | 55.9 ms: 1.18x faster                                                        |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                        |
| sympy_str                | 346 ms                                                 | 293 ms: 1.18x faster                                                         |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                                         |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.18x faster                                                         |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                        |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                        |
| sympy_expand             | 566 ms                                                 | 494 ms: 1.14x faster                                                         |
| json_loads               | 31.2 us                                                | 27.3 us: 1.14x faster                                                        |
| bench_thread_pool        | 986 us                                                 | 864 us: 1.14x faster                                                         |
| xml_etree_iterparse      | 115 ms                                                 | 101 ms: 1.14x faster                                                         |
| mypy2                    | 894 ms                                                 | 785 ms: 1.14x faster                                                         |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                       |
| xml_etree_generate       | 99.4 ms                                                | 87.6 ms: 1.13x faster                                                        |
| xml_etree_parse          | 168 ms                                                 | 148 ms: 1.13x faster                                                         |
| json                     | 5.69 ms                                                | 5.08 ms: 1.12x faster                                                        |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                        |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.11x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.64 sec: 1.08x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                        |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                         |
| pickle_list              | 5.08 us                                                | 5.06 us: 1.00x faster                                                        |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                         |
| regex_dna                | 227 ms                                                 | 229 ms: 1.01x slower                                                         |
| gc_traversal             | 3.62 ms                                                | 3.74 ms: 1.03x slower                                                        |
| async_generators         | 444 ms                                                 | 467 ms: 1.05x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.06x slower                                                        |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.10x slower                                                        |
| pickle                   | 10.7 us                                                | 11.8 us: 1.10x slower                                                        |
| regex_effbot             | 3.63 ms                                                | 4.21 ms: 1.16x slower                                                        |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                                        |
| pickle_dict              | 29.6 us                                                | 35.6 us: 1.20x slower                                                        |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.24x slower                                                        |
| python_startup_no_site   | 5.93 ms                                                | 7.68 ms: 1.30x slower                                                        |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                 |

Benchmark hidden because not significant (2): bench_mp_pool, unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-b8620f7-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.21x