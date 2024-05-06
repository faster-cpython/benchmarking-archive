# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 19f3205
- commit date: 2024-04-26
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                       |
| chameleon      | 9.68 ms                                                | 6.99 ms: 1.39x faster                                                      |
| docutils       | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                     |
| html5lib       | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                      |
| tornado_http   | 136 ms                                                 | 96.2 ms: 1.42x faster                                                      |
| Geometric mean | (ref)                                                  | 1.29x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                                       |
| async_tree_io           | 1.77 sec                                               | 928 ms: 1.91x faster                                                       |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                       |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 615 ms: 1.65x faster                                                       |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 77.8 ms: 1.97x faster                                                      |
| float          | 117 ms                                                 | 72.7 ms: 1.61x faster                                                      |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                  | 1.47x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 139 ms: 1.36x faster                                                       |
| regex_v8       | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                      |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                       |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                  | 1.09x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.92 sec: 1.63x faster                                                     |
| pickle_pure_python   | 484 us                                                 | 306 us: 1.59x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 226 us: 1.46x faster                                                       |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                      |
| xml_etree_process    | 79.1 ms                                                | 60.3 ms: 1.31x faster                                                      |
| xml_etree_generate   | 99.4 ms                                                | 87.6 ms: 1.14x faster                                                      |
| xml_etree_iterparse  | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| xml_etree_parse      | 168 ms                                                 | 149 ms: 1.13x faster                                                       |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                      |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                      |
| unpickle_list        | 5.20 us                                                | 5.26 us: 1.01x slower                                                      |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                      |
| pickle               | 10.7 us                                                | 11.7 us: 1.09x slower                                                      |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| python_startup_no_site | 5.93 ms                                                | 7.69 ms: 1.30x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.1 ms: 1.62x faster                                                      |
| django_template | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                      |
| genshi_text     | 31.8 ms                                                | 24.4 ms: 1.31x faster                                                      |
| genshi_xml      | 66.0 ms                                                | 53.9 ms: 1.22x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.65x faster                                                       |
| generators               | 80.1 ms                                                | 30.3 ms: 2.65x faster                                                      |
| deltablue                | 7.91 ms                                                | 3.67 ms: 2.16x faster                                                      |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                                       |
| nbody                    | 154 ms                                                 | 77.8 ms: 1.97x faster                                                      |
| richards_super           | 94.7 ms                                                | 48.4 ms: 1.96x faster                                                      |
| chaos                    | 115 ms                                                 | 60.3 ms: 1.91x faster                                                      |
| async_tree_io            | 1.77 sec                                               | 928 ms: 1.91x faster                                                       |
| richards                 | 79.3 ms                                                | 41.9 ms: 1.89x faster                                                      |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                       |
| crypto_pyaes             | 128 ms                                                 | 68.3 ms: 1.87x faster                                                      |
| raytrace                 | 507 ms                                                 | 273 ms: 1.86x faster                                                       |
| scimark_monte_carlo      | 118 ms                                                 | 63.6 ms: 1.86x faster                                                      |
| logging_silent           | 190 ns                                                 | 103 ns: 1.84x faster                                                       |
| asyncio_tcp              | 922 ms                                                 | 516 ms: 1.79x faster                                                       |
| spectral_norm            | 170 ms                                                 | 97.9 ms: 1.74x faster                                                      |
| scimark_sor              | 220 ms                                                 | 130 ms: 1.69x faster                                                       |
| comprehensions           | 28.8 us                                                | 17.2 us: 1.68x faster                                                      |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 615 ms: 1.65x faster                                                       |
| pylint                   | 551 ms                                                 | 334 ms: 1.65x faster                                                       |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                                      |
| tomli_loads              | 3.14 sec                                               | 1.92 sec: 1.63x faster                                                     |
| mako                     | 16.3 ms                                                | 10.1 ms: 1.62x faster                                                      |
| float                    | 117 ms                                                 | 72.7 ms: 1.61x faster                                                      |
| go                       | 240 ms                                                 | 149 ms: 1.61x faster                                                       |
| pyflate                  | 716 ms                                                 | 448 ms: 1.60x faster                                                       |
| hexiom                   | 10.4 ms                                                | 6.53 ms: 1.59x faster                                                      |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.59x faster                                                       |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.57x faster                                                      |
| scimark_fft              | 466 ms                                                 | 303 ms: 1.54x faster                                                       |
| coroutines               | 35.1 ms                                                | 22.9 ms: 1.53x faster                                                      |
| fannkuch                 | 532 ms                                                 | 353 ms: 1.51x faster                                                       |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.33 ms: 1.49x faster                                                      |
| deepcopy_memo            | 58.5 us                                                | 39.1 us: 1.49x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 226 us: 1.46x faster                                                       |
| logging_simple           | 8.30 us                                                | 5.80 us: 1.43x faster                                                      |
| pprint_pformat           | 2.10 sec                                               | 1.47 sec: 1.43x faster                                                     |
| tornado_http             | 136 ms                                                 | 96.2 ms: 1.42x faster                                                      |
| logging_format           | 9.09 us                                                | 6.47 us: 1.40x faster                                                      |
| pprint_safe_repr         | 1.02 sec                                               | 728 ms: 1.40x faster                                                       |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                     |
| scimark_lu               | 176 ms                                                 | 127 ms: 1.39x faster                                                       |
| chameleon                | 9.68 ms                                                | 6.99 ms: 1.39x faster                                                      |
| regex_compile            | 188 ms                                                 | 139 ms: 1.36x faster                                                       |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                                     |
| django_template          | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                      |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                      |
| deepcopy                 | 479 us                                                 | 362 us: 1.32x faster                                                       |
| xml_etree_process        | 79.1 ms                                                | 60.3 ms: 1.31x faster                                                      |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                      |
| genshi_text              | 31.8 ms                                                | 24.4 ms: 1.31x faster                                                      |
| thrift                   | 1.07 ms                                                | 825 us: 1.30x faster                                                       |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                      |
| html5lib                 | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                      |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                       |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                       |
| nqueens                  | 106 ms                                                 | 85.7 ms: 1.24x faster                                                      |
| genshi_xml               | 66.0 ms                                                | 53.9 ms: 1.22x faster                                                      |
| dulwich_log              | 84.3 ms                                                | 69.2 ms: 1.22x faster                                                      |
| sqlglot_optimize         | 69.2 ms                                                | 57.1 ms: 1.21x faster                                                      |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                      |
| djangocms                | 38.4 us                                                | 32.6 us: 1.18x faster                                                      |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                                       |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                      |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.18x faster                                                       |
| sympy_str                | 346 ms                                                 | 294 ms: 1.18x faster                                                       |
| sympy_integrate          | 25.8 ms                                                | 22.0 ms: 1.17x faster                                                      |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                      |
| bench_thread_pool        | 986 us                                                 | 866 us: 1.14x faster                                                       |
| sympy_expand             | 566 ms                                                 | 497 ms: 1.14x faster                                                       |
| mypy2                    | 894 ms                                                 | 787 ms: 1.14x faster                                                       |
| xml_etree_generate       | 99.4 ms                                                | 87.6 ms: 1.14x faster                                                      |
| xml_etree_iterparse      | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| xml_etree_parse          | 168 ms                                                 | 149 ms: 1.13x faster                                                       |
| json                     | 5.69 ms                                                | 5.04 ms: 1.13x faster                                                      |
| docutils                 | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                     |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                      |
| regex_v8                 | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                      |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                      |
| mdp                      | 2.85 sec                                               | 2.77 sec: 1.03x faster                                                     |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                       |
| bench_mp_pool            | 24.0 ms                                                | 24.1 ms: 1.00x slower                                                      |
| pickle_list              | 5.08 us                                                | 5.12 us: 1.01x slower                                                      |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                       |
| unpickle_list            | 5.20 us                                                | 5.26 us: 1.01x slower                                                      |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                       |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                      |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                      |
| async_generators         | 444 ms                                                 | 467 ms: 1.05x slower                                                       |
| gc_traversal             | 3.62 ms                                                | 3.87 ms: 1.07x slower                                                      |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                      |
| pickle                   | 10.7 us                                                | 11.7 us: 1.09x slower                                                      |
| telco                    | 7.27 ms                                                | 8.63 ms: 1.19x slower                                                      |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                                      |
| coverage                 | 79.4 ms                                                | 97.4 ms: 1.23x slower                                                      |
| python_startup_no_site   | 5.93 ms                                                | 7.69 ms: 1.30x slower                                                      |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                               |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-19f3205-JIT/bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.22x