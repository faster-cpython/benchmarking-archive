# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 9759712
- commit date: 2024-04-17
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                       |
| chameleon      | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                      |
| docutils       | 3.30 sec                                               | 2.91 sec: 1.13x faster                                                     |
| html5lib       | 88.9 ms                                                | 67.9 ms: 1.31x faster                                                      |
| tornado_http   | 136 ms                                                 | 96.2 ms: 1.42x faster                                                      |
| Geometric mean | (ref)                                                  | 1.29x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                       |
| async_tree_io           | 1.77 sec                                               | 922 ms: 1.92x faster                                                       |
| async_tree_memoization  | 870 ms                                                 | 467 ms: 1.86x faster                                                       |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 616 ms: 1.65x faster                                                       |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 77.1 ms: 1.99x faster                                                      |
| float          | 117 ms                                                 | 72.9 ms: 1.61x faster                                                      |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                  | 1.48x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                       |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                      |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                       |
| regex_effbot   | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.93 sec: 1.63x faster                                                     |
| pickle_pure_python   | 484 us                                                 | 304 us: 1.59x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 224 us: 1.48x faster                                                       |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                      |
| xml_etree_process    | 79.1 ms                                                | 59.5 ms: 1.33x faster                                                      |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                      |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                      |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                       |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.04x faster                                                       |
| pickle_list          | 5.08 us                                                | 4.91 us: 1.04x faster                                                      |
| unpickle_list        | 5.20 us                                                | 5.12 us: 1.02x faster                                                      |
| unpickle             | 14.4 us                                                | 15.3 us: 1.06x slower                                                      |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                      |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| python_startup_no_site | 5.93 ms                                                | 7.66 ms: 1.29x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.1 ms: 1.61x faster                                                      |
| django_template | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                      |
| genshi_text     | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                      |
| genshi_xml      | 66.0 ms                                                | 54.2 ms: 1.22x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 112 us: 4.87x faster                                                       |
| generators               | 80.1 ms                                                | 29.6 ms: 2.70x faster                                                      |
| deltablue                | 7.91 ms                                                | 3.67 ms: 2.16x faster                                                      |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                       |
| nbody                    | 154 ms                                                 | 77.1 ms: 1.99x faster                                                      |
| richards_super           | 94.7 ms                                                | 48.5 ms: 1.95x faster                                                      |
| chaos                    | 115 ms                                                 | 60.2 ms: 1.92x faster                                                      |
| async_tree_io            | 1.77 sec                                               | 922 ms: 1.92x faster                                                       |
| raytrace                 | 507 ms                                                 | 270 ms: 1.88x faster                                                       |
| crypto_pyaes             | 128 ms                                                 | 68.5 ms: 1.87x faster                                                      |
| scimark_monte_carlo      | 118 ms                                                 | 63.4 ms: 1.86x faster                                                      |
| async_tree_memoization   | 870 ms                                                 | 467 ms: 1.86x faster                                                       |
| richards                 | 79.3 ms                                                | 42.9 ms: 1.85x faster                                                      |
| logging_silent           | 190 ns                                                 | 103 ns: 1.84x faster                                                       |
| asyncio_tcp              | 922 ms                                                 | 512 ms: 1.80x faster                                                       |
| scimark_sor              | 220 ms                                                 | 126 ms: 1.74x faster                                                       |
| spectral_norm            | 170 ms                                                 | 99.8 ms: 1.70x faster                                                      |
| comprehensions           | 28.8 us                                                | 17.2 us: 1.68x faster                                                      |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.66x faster                                                      |
| pylint                   | 551 ms                                                 | 334 ms: 1.65x faster                                                       |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 616 ms: 1.65x faster                                                       |
| go                       | 240 ms                                                 | 147 ms: 1.64x faster                                                       |
| tomli_loads              | 3.14 sec                                               | 1.93 sec: 1.63x faster                                                     |
| pyflate                  | 716 ms                                                 | 441 ms: 1.62x faster                                                       |
| mako                     | 16.3 ms                                                | 10.1 ms: 1.61x faster                                                      |
| float                    | 117 ms                                                 | 72.9 ms: 1.61x faster                                                      |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.59x faster                                                       |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                      |
| hexiom                   | 10.4 ms                                                | 6.71 ms: 1.55x faster                                                      |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.55x faster                                                      |
| scimark_fft              | 466 ms                                                 | 304 ms: 1.53x faster                                                       |
| fannkuch                 | 532 ms                                                 | 350 ms: 1.52x faster                                                       |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.34 ms: 1.49x faster                                                      |
| deepcopy_memo            | 58.5 us                                                | 39.3 us: 1.49x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 224 us: 1.48x faster                                                       |
| logging_simple           | 8.30 us                                                | 5.74 us: 1.45x faster                                                      |
| logging_format           | 9.09 us                                                | 6.37 us: 1.43x faster                                                      |
| pprint_pformat           | 2.10 sec                                               | 1.48 sec: 1.43x faster                                                     |
| scimark_lu               | 176 ms                                                 | 124 ms: 1.42x faster                                                       |
| tornado_http             | 136 ms                                                 | 96.2 ms: 1.42x faster                                                      |
| pprint_safe_repr         | 1.02 sec                                               | 722 ms: 1.41x faster                                                       |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                     |
| chameleon                | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                      |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                      |
| django_template          | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                      |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                       |
| deepcopy                 | 479 us                                                 | 359 us: 1.34x faster                                                       |
| xml_etree_process        | 79.1 ms                                                | 59.5 ms: 1.33x faster                                                      |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                      |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| html5lib                 | 88.9 ms                                                | 67.9 ms: 1.31x faster                                                      |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                      |
| thrift                   | 1.07 ms                                                | 825 us: 1.30x faster                                                       |
| pycparser                | 1.58 sec                                               | 1.22 sec: 1.30x faster                                                     |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.27x faster                                                       |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                       |
| djangocms                | 38.4 us                                                | 31.5 us: 1.22x faster                                                      |
| dulwich_log              | 84.3 ms                                                | 69.1 ms: 1.22x faster                                                      |
| genshi_xml               | 66.0 ms                                                | 54.2 ms: 1.22x faster                                                      |
| sqlglot_optimize         | 69.2 ms                                                | 57.3 ms: 1.21x faster                                                      |
| nqueens                  | 106 ms                                                 | 88.2 ms: 1.20x faster                                                      |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                      |
| dask                     | 441 ms                                                 | 375 ms: 1.18x faster                                                       |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.17x faster                                                      |
| sympy_integrate          | 25.8 ms                                                | 22.0 ms: 1.17x faster                                                      |
| sympy_str                | 346 ms                                                 | 295 ms: 1.17x faster                                                       |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                       |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                                      |
| mypy2                    | 894 ms                                                 | 782 ms: 1.14x faster                                                       |
| bench_thread_pool        | 986 us                                                 | 864 us: 1.14x faster                                                       |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                      |
| sympy_expand             | 566 ms                                                 | 496 ms: 1.14x faster                                                       |
| docutils                 | 3.30 sec                                               | 2.91 sec: 1.13x faster                                                     |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                      |
| json                     | 5.69 ms                                                | 5.08 ms: 1.12x faster                                                      |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                       |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                       |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                      |
| sqlite_synth             | 3.02 us                                                | 2.87 us: 1.06x faster                                                      |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.04x faster                                                       |
| pickle_list              | 5.08 us                                                | 4.91 us: 1.04x faster                                                      |
| mdp                      | 2.85 sec                                               | 2.75 sec: 1.03x faster                                                     |
| unpickle_list            | 5.20 us                                                | 5.12 us: 1.02x faster                                                      |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                       |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                       |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                       |
| regex_effbot             | 3.63 ms                                                | 3.77 ms: 1.04x slower                                                      |
| async_generators         | 444 ms                                                 | 471 ms: 1.06x slower                                                       |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.06x slower                                                      |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                      |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                      |
| gc_traversal             | 3.62 ms                                                | 4.00 ms: 1.10x slower                                                      |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                                      |
| telco                    | 7.27 ms                                                | 8.52 ms: 1.17x slower                                                      |
| coverage                 | 79.4 ms                                                | 97.8 ms: 1.23x slower                                                      |
| python_startup_no_site   | 5.93 ms                                                | 7.66 ms: 1.29x slower                                                      |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                               |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240417-3.13.0a6+-9759712-JIT/bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.22x