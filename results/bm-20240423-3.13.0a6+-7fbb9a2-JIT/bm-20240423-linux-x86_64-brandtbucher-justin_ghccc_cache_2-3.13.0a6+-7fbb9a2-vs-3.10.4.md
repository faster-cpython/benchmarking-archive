# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache_2
- machine: linux-x86_64
- commit hash: 7fbb9a2
- commit date: 2024-04-23
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 275 ms: 1.27x faster                                                         |
| chameleon      | 9.68 ms                                                | 6.88 ms: 1.41x faster                                                        |
| docutils       | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                       |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                        |
| tornado_http   | 136 ms                                                 | 96.2 ms: 1.42x faster                                                        |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.04x faster                                                         |
| async_tree_memoization  | 870 ms                                                 | 463 ms: 1.88x faster                                                         |
| async_tree_io           | 1.77 sec                                               | 944 ms: 1.87x faster                                                         |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 620 ms: 1.64x faster                                                         |
| Geometric mean          | (ref)                                                  | 1.85x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 77.3 ms: 1.99x faster                                                        |
| float          | 117 ms                                                 | 72.4 ms: 1.62x faster                                                        |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.48x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 139 ms: 1.35x faster                                                         |
| regex_v8       | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                        |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                         |
| regex_effbot   | 3.63 ms                                                | 3.71 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.92 sec: 1.64x faster                                                       |
| pickle_pure_python   | 484 us                                                 | 304 us: 1.59x faster                                                         |
| unpickle_pure_python | 331 us                                                 | 221 us: 1.49x faster                                                         |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                        |
| xml_etree_process    | 79.1 ms                                                | 59.2 ms: 1.34x faster                                                        |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                        |
| json_loads           | 31.2 us                                                | 27.5 us: 1.14x faster                                                        |
| xml_etree_iterparse  | 115 ms                                                 | 103 ms: 1.12x faster                                                         |
| xml_etree_parse      | 168 ms                                                 | 150 ms: 1.12x faster                                                         |
| unpickle_list        | 5.20 us                                                | 5.42 us: 1.04x slower                                                        |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                        |
| pickle_list          | 5.08 us                                                | 5.38 us: 1.06x slower                                                        |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                        |
| pickle_dict          | 29.6 us                                                | 36.8 us: 1.24x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                        |
| python_startup_no_site | 5.93 ms                                                | 7.63 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.1 ms: 1.61x faster                                                        |
| django_template | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                        |
| genshi_text     | 31.8 ms                                                | 24.1 ms: 1.32x faster                                                        |
| genshi_xml      | 66.0 ms                                                | 53.7 ms: 1.23x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.90x faster                                                         |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                        |
| deltablue                | 7.91 ms                                                | 3.67 ms: 2.16x faster                                                        |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.04x faster                                                         |
| nbody                    | 154 ms                                                 | 77.3 ms: 1.99x faster                                                        |
| richards_super           | 94.7 ms                                                | 48.2 ms: 1.97x faster                                                        |
| chaos                    | 115 ms                                                 | 60.8 ms: 1.90x faster                                                        |
| richards                 | 79.3 ms                                                | 42.0 ms: 1.89x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 463 ms: 1.88x faster                                                         |
| async_tree_io            | 1.77 sec                                               | 944 ms: 1.87x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 68.3 ms: 1.87x faster                                                        |
| logging_silent           | 190 ns                                                 | 102 ns: 1.87x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 63.3 ms: 1.87x faster                                                        |
| raytrace                 | 507 ms                                                 | 276 ms: 1.84x faster                                                         |
| asyncio_tcp              | 922 ms                                                 | 504 ms: 1.83x faster                                                         |
| spectral_norm            | 170 ms                                                 | 97.7 ms: 1.74x faster                                                        |
| comprehensions           | 28.8 us                                                | 17.1 us: 1.68x faster                                                        |
| pylint                   | 551 ms                                                 | 331 ms: 1.66x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.66x faster                                                        |
| scimark_sor              | 220 ms                                                 | 132 ms: 1.66x faster                                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 620 ms: 1.64x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 1.92 sec: 1.64x faster                                                       |
| go                       | 240 ms                                                 | 147 ms: 1.63x faster                                                         |
| float                    | 117 ms                                                 | 72.4 ms: 1.62x faster                                                        |
| mako                     | 16.3 ms                                                | 10.1 ms: 1.61x faster                                                        |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.59x faster                                                         |
| pyflate                  | 716 ms                                                 | 450 ms: 1.59x faster                                                         |
| hexiom                   | 10.4 ms                                                | 6.56 ms: 1.58x faster                                                        |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                        |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                        |
| scimark_fft              | 466 ms                                                 | 302 ms: 1.54x faster                                                         |
| fannkuch                 | 532 ms                                                 | 349 ms: 1.52x faster                                                         |
| deepcopy_memo            | 58.5 us                                                | 38.4 us: 1.52x faster                                                        |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.29 ms: 1.51x faster                                                        |
| unpickle_pure_python     | 331 us                                                 | 221 us: 1.49x faster                                                         |
| scimark_lu               | 176 ms                                                 | 124 ms: 1.42x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.84 us: 1.42x faster                                                        |
| pprint_safe_repr         | 1.02 sec                                               | 718 ms: 1.42x faster                                                         |
| tornado_http             | 136 ms                                                 | 96.2 ms: 1.42x faster                                                        |
| chameleon                | 9.68 ms                                                | 6.88 ms: 1.41x faster                                                        |
| pprint_pformat           | 2.10 sec                                               | 1.50 sec: 1.40x faster                                                       |
| logging_format           | 9.09 us                                                | 6.49 us: 1.40x faster                                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                       |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                       |
| django_template          | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                        |
| regex_compile            | 188 ms                                                 | 139 ms: 1.35x faster                                                         |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                        |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                                         |
| xml_etree_process        | 79.1 ms                                                | 59.2 ms: 1.34x faster                                                        |
| deepcopy_reduce          | 4.17 us                                                | 3.16 us: 1.32x faster                                                        |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                        |
| genshi_text              | 31.8 ms                                                | 24.1 ms: 1.32x faster                                                        |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                        |
| thrift                   | 1.07 ms                                                | 822 us: 1.30x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.27x faster                                                         |
| 2to3                     | 348 ms                                                 | 275 ms: 1.27x faster                                                         |
| nqueens                  | 106 ms                                                 | 85.1 ms: 1.24x faster                                                        |
| genshi_xml               | 66.0 ms                                                | 53.7 ms: 1.23x faster                                                        |
| dulwich_log              | 84.3 ms                                                | 69.1 ms: 1.22x faster                                                        |
| sqlglot_optimize         | 69.2 ms                                                | 56.7 ms: 1.22x faster                                                        |
| djangocms                | 38.4 us                                                | 32.0 us: 1.20x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.20 ms: 1.19x faster                                                        |
| sympy_str                | 346 ms                                                 | 290 ms: 1.19x faster                                                         |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.19x faster                                                        |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                                         |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                        |
| dask                     | 441 ms                                                 | 375 ms: 1.18x faster                                                         |
| mypy2                    | 894 ms                                                 | 778 ms: 1.15x faster                                                         |
| sympy_expand             | 566 ms                                                 | 493 ms: 1.15x faster                                                         |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                        |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                        |
| bench_thread_pool        | 986 us                                                 | 862 us: 1.14x faster                                                         |
| docutils                 | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                       |
| json_loads               | 31.2 us                                                | 27.5 us: 1.14x faster                                                        |
| json                     | 5.69 ms                                                | 5.05 ms: 1.13x faster                                                        |
| xml_etree_iterparse      | 115 ms                                                 | 103 ms: 1.12x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                        |
| xml_etree_parse          | 168 ms                                                 | 150 ms: 1.12x faster                                                         |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                         |
| mdp                      | 2.85 sec                                               | 2.63 sec: 1.08x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                        |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                         |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                         |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                         |
| regex_effbot             | 3.63 ms                                                | 3.71 ms: 1.02x slower                                                        |
| gc_traversal             | 3.62 ms                                                | 3.70 ms: 1.02x slower                                                        |
| unpickle_list            | 5.20 us                                                | 5.42 us: 1.04x slower                                                        |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                        |
| async_generators         | 444 ms                                                 | 470 ms: 1.06x slower                                                         |
| pickle_list              | 5.08 us                                                | 5.38 us: 1.06x slower                                                        |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                        |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                        |
| telco                    | 7.27 ms                                                | 8.53 ms: 1.17x slower                                                        |
| coverage                 | 79.4 ms                                                | 97.2 ms: 1.22x slower                                                        |
| pickle_dict              | 29.6 us                                                | 36.8 us: 1.24x slower                                                        |
| python_startup_no_site   | 5.93 ms                                                | 7.63 ms: 1.29x slower                                                        |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                 |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-7fbb9a2-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.21x