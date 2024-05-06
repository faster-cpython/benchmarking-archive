# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 280cb86
- commit date: 2024-04-25
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 275 ms: 1.27x faster                                                       |
| chameleon      | 9.68 ms                                                | 6.94 ms: 1.40x faster                                                      |
| docutils       | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                     |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                      |
| tornado_http   | 136 ms                                                 | 95.3 ms: 1.43x faster                                                      |
| Geometric mean | (ref)                                                  | 1.30x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                       |
| async_tree_io           | 1.77 sec                                               | 937 ms: 1.89x faster                                                       |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                       |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                       |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 75.3 ms: 2.04x faster                                                      |
| float          | 117 ms                                                 | 72.6 ms: 1.61x faster                                                      |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                  | 1.48x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                       |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                      |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                       |
| regex_effbot   | 3.63 ms                                                | 3.76 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.90 sec: 1.65x faster                                                     |
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 223 us: 1.48x faster                                                       |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                      |
| xml_etree_process    | 79.1 ms                                                | 59.7 ms: 1.32x faster                                                      |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                      |
| xml_etree_parse      | 168 ms                                                 | 148 ms: 1.13x faster                                                       |
| xml_etree_iterparse  | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                      |
| unpickle_list        | 5.20 us                                                | 5.14 us: 1.01x faster                                                      |
| pickle_list          | 5.08 us                                                | 5.10 us: 1.00x slower                                                      |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                      |
| pickle               | 10.7 us                                                | 11.5 us: 1.08x slower                                                      |
| pickle_dict          | 29.6 us                                                | 34.6 us: 1.17x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.17x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| python_startup_no_site | 5.93 ms                                                | 7.71 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.00x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.0 ms: 1.63x faster                                                      |
| django_template | 48.2 ms                                                | 35.9 ms: 1.34x faster                                                      |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                      |
| genshi_xml      | 66.0 ms                                                | 54.2 ms: 1.22x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 116 us: 4.70x faster                                                       |
| generators               | 80.1 ms                                                | 29.9 ms: 2.68x faster                                                      |
| deltablue                | 7.91 ms                                                | 3.63 ms: 2.18x faster                                                      |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                       |
| nbody                    | 154 ms                                                 | 75.3 ms: 2.04x faster                                                      |
| richards_super           | 94.7 ms                                                | 48.0 ms: 1.97x faster                                                      |
| chaos                    | 115 ms                                                 | 59.3 ms: 1.95x faster                                                      |
| scimark_monte_carlo      | 118 ms                                                 | 61.9 ms: 1.91x faster                                                      |
| richards                 | 79.3 ms                                                | 41.9 ms: 1.89x faster                                                      |
| async_tree_io            | 1.77 sec                                               | 937 ms: 1.89x faster                                                       |
| crypto_pyaes             | 128 ms                                                 | 67.7 ms: 1.89x faster                                                      |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                       |
| raytrace                 | 507 ms                                                 | 271 ms: 1.87x faster                                                       |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                       |
| asyncio_tcp              | 922 ms                                                 | 516 ms: 1.79x faster                                                       |
| scimark_sor              | 220 ms                                                 | 128 ms: 1.72x faster                                                       |
| spectral_norm            | 170 ms                                                 | 99.7 ms: 1.70x faster                                                      |
| comprehensions           | 28.8 us                                                | 17.1 us: 1.68x faster                                                      |
| pylint                   | 551 ms                                                 | 332 ms: 1.66x faster                                                       |
| pyflate                  | 716 ms                                                 | 432 ms: 1.66x faster                                                       |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.66x faster                                                      |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                       |
| tomli_loads              | 3.14 sec                                               | 1.90 sec: 1.65x faster                                                     |
| go                       | 240 ms                                                 | 147 ms: 1.64x faster                                                       |
| mako                     | 16.3 ms                                                | 10.0 ms: 1.63x faster                                                      |
| hexiom                   | 10.4 ms                                                | 6.40 ms: 1.62x faster                                                      |
| float                    | 117 ms                                                 | 72.6 ms: 1.61x faster                                                      |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                                       |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                      |
| fannkuch                 | 532 ms                                                 | 345 ms: 1.54x faster                                                       |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                      |
| scimark_fft              | 466 ms                                                 | 308 ms: 1.51x faster                                                       |
| deepcopy_memo            | 58.5 us                                                | 39.2 us: 1.49x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 223 us: 1.48x faster                                                       |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.38 ms: 1.48x faster                                                      |
| tornado_http             | 136 ms                                                 | 95.3 ms: 1.43x faster                                                      |
| logging_simple           | 8.30 us                                                | 5.82 us: 1.43x faster                                                      |
| pprint_pformat           | 2.10 sec                                               | 1.48 sec: 1.42x faster                                                     |
| pprint_safe_repr         | 1.02 sec                                               | 724 ms: 1.41x faster                                                       |
| scimark_lu               | 176 ms                                                 | 125 ms: 1.41x faster                                                       |
| logging_format           | 9.09 us                                                | 6.50 us: 1.40x faster                                                      |
| chameleon                | 9.68 ms                                                | 6.94 ms: 1.40x faster                                                      |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                     |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.35x faster                                                     |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                       |
| django_template          | 48.2 ms                                                | 35.9 ms: 1.34x faster                                                      |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                      |
| xml_etree_process        | 79.1 ms                                                | 59.7 ms: 1.32x faster                                                      |
| deepcopy                 | 479 us                                                 | 363 us: 1.32x faster                                                       |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                                       |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                      |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                                      |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                      |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.27x faster                                                       |
| 2to3                     | 348 ms                                                 | 275 ms: 1.27x faster                                                       |
| nqueens                  | 106 ms                                                 | 86.0 ms: 1.23x faster                                                      |
| dulwich_log              | 84.3 ms                                                | 68.8 ms: 1.22x faster                                                      |
| genshi_xml               | 66.0 ms                                                | 54.2 ms: 1.22x faster                                                      |
| sqlglot_optimize         | 69.2 ms                                                | 56.7 ms: 1.22x faster                                                      |
| djangocms                | 38.4 us                                                | 32.0 us: 1.20x faster                                                      |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                      |
| sympy_str                | 346 ms                                                 | 291 ms: 1.19x faster                                                       |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.19x faster                                                       |
| gunicorn                 | 1.53 ms                                                | 1.29 ms: 1.18x faster                                                      |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.18x faster                                                      |
| dask                     | 441 ms                                                 | 373 ms: 1.18x faster                                                       |
| mypy2                    | 894 ms                                                 | 779 ms: 1.15x faster                                                       |
| bench_thread_pool        | 986 us                                                 | 860 us: 1.15x faster                                                       |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                      |
| sympy_expand             | 566 ms                                                 | 494 ms: 1.14x faster                                                       |
| xml_etree_parse          | 168 ms                                                 | 148 ms: 1.13x faster                                                       |
| xml_etree_iterparse      | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                      |
| pathlib                  | 20.5 ms                                                | 18.1 ms: 1.13x faster                                                      |
| docutils                 | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                     |
| json                     | 5.69 ms                                                | 5.15 ms: 1.11x faster                                                      |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.09x faster                                                       |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                      |
| sqlite_synth             | 3.02 us                                                | 2.82 us: 1.07x faster                                                      |
| mdp                      | 2.85 sec                                               | 2.69 sec: 1.06x faster                                                     |
| unpickle_list            | 5.20 us                                                | 5.14 us: 1.01x faster                                                      |
| pickle_list              | 5.08 us                                                | 5.10 us: 1.00x slower                                                      |
| asyncio_websockets       | 559 ms                                                 | 565 ms: 1.01x slower                                                       |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                       |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                       |
| regex_effbot             | 3.63 ms                                                | 3.76 ms: 1.04x slower                                                      |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                      |
| async_generators         | 444 ms                                                 | 466 ms: 1.05x slower                                                       |
| pickle                   | 10.7 us                                                | 11.5 us: 1.08x slower                                                      |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                      |
| gc_traversal             | 3.62 ms                                                | 4.06 ms: 1.12x slower                                                      |
| pickle_dict              | 29.6 us                                                | 34.6 us: 1.17x slower                                                      |
| telco                    | 7.27 ms                                                | 8.57 ms: 1.18x slower                                                      |
| coverage                 | 79.4 ms                                                | 97.2 ms: 1.22x slower                                                      |
| python_startup_no_site   | 5.93 ms                                                | 7.71 ms: 1.30x slower                                                      |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                               |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240425-3.13.0a6+-280cb86-JIT/bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.22x