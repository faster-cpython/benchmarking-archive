# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_preserve_most
- machine: linux-x86_64
- commit hash: 377ec17
- commit date: 2024-04-18
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                         |
| chameleon      | 9.68 ms                                                | 6.92 ms: 1.40x faster                                                        |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                       |
| html5lib       | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                        |
| tornado_http   | 136 ms                                                 | 96.0 ms: 1.42x faster                                                        |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 354 ms: 2.06x faster                                                         |
| async_tree_io           | 1.77 sec                                               | 923 ms: 1.92x faster                                                         |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                                         |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 609 ms: 1.67x faster                                                         |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 95.1 ms: 1.61x faster                                                        |
| float          | 117 ms                                                 | 76.6 ms: 1.53x faster                                                        |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 142 ms: 1.33x faster                                                         |
| regex_v8       | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                        |
| regex_dna      | 227 ms                                                 | 228 ms: 1.01x slower                                                         |
| regex_effbot   | 3.63 ms                                                | 3.78 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 304 us: 1.59x faster                                                         |
| tomli_loads          | 3.14 sec                                               | 1.99 sec: 1.58x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 231 us: 1.43x faster                                                         |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                        |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                        |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                        |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                        |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                         |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                         |
| unpickle_list        | 5.20 us                                                | 5.00 us: 1.04x faster                                                        |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                        |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                        |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                        |
| pickle_dict          | 29.6 us                                                | 35.7 us: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.9 ms: 1.33x faster                                                        |
| python_startup_no_site | 5.93 ms                                                | 7.55 ms: 1.27x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.6 ms: 1.55x faster                                                        |
| django_template | 48.2 ms                                                | 35.9 ms: 1.34x faster                                                        |
| genshi_text     | 31.8 ms                                                | 24.0 ms: 1.32x faster                                                        |
| genshi_xml      | 66.0 ms                                                | 53.9 ms: 1.23x faster                                                        |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.78x faster                                                         |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                        |
| deltablue                | 7.91 ms                                                | 3.62 ms: 2.19x faster                                                        |
| async_tree_none          | 728 ms                                                 | 354 ms: 2.06x faster                                                         |
| richards_super           | 94.7 ms                                                | 48.4 ms: 1.96x faster                                                        |
| async_tree_io            | 1.77 sec                                               | 923 ms: 1.92x faster                                                         |
| raytrace                 | 507 ms                                                 | 269 ms: 1.89x faster                                                         |
| richards                 | 79.3 ms                                                | 42.1 ms: 1.88x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                                         |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                         |
| chaos                    | 115 ms                                                 | 62.3 ms: 1.85x faster                                                        |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                         |
| scimark_monte_carlo      | 118 ms                                                 | 67.8 ms: 1.74x faster                                                        |
| crypto_pyaes             | 128 ms                                                 | 74.1 ms: 1.72x faster                                                        |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 609 ms: 1.67x faster                                                         |
| scimark_sor              | 220 ms                                                 | 133 ms: 1.66x faster                                                         |
| pylint                   | 551 ms                                                 | 334 ms: 1.65x faster                                                         |
| comprehensions           | 28.8 us                                                | 17.4 us: 1.65x faster                                                        |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                                        |
| nbody                    | 154 ms                                                 | 95.1 ms: 1.61x faster                                                        |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.59x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 1.99 sec: 1.58x faster                                                       |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                        |
| go                       | 240 ms                                                 | 153 ms: 1.57x faster                                                         |
| pyflate                  | 716 ms                                                 | 463 ms: 1.55x faster                                                         |
| mako                     | 16.3 ms                                                | 10.6 ms: 1.55x faster                                                        |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                        |
| float                    | 117 ms                                                 | 76.6 ms: 1.53x faster                                                        |
| deepcopy_memo            | 58.5 us                                                | 38.3 us: 1.53x faster                                                        |
| hexiom                   | 10.4 ms                                                | 6.86 ms: 1.52x faster                                                        |
| spectral_norm            | 170 ms                                                 | 119 ms: 1.43x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 231 us: 1.43x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.81 us: 1.43x faster                                                        |
| logging_format           | 9.09 us                                                | 6.38 us: 1.42x faster                                                        |
| tornado_http             | 136 ms                                                 | 96.0 ms: 1.42x faster                                                        |
| chameleon                | 9.68 ms                                                | 6.92 ms: 1.40x faster                                                        |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                       |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                                       |
| pprint_safe_repr         | 1.02 sec                                               | 748 ms: 1.36x faster                                                         |
| fannkuch                 | 532 ms                                                 | 392 ms: 1.36x faster                                                         |
| scimark_lu               | 176 ms                                                 | 131 ms: 1.34x faster                                                         |
| deepcopy                 | 479 us                                                 | 356 us: 1.34x faster                                                         |
| django_template          | 48.2 ms                                                | 35.9 ms: 1.34x faster                                                        |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                        |
| python_startup           | 14.6 ms                                                | 10.9 ms: 1.33x faster                                                        |
| regex_compile            | 188 ms                                                 | 142 ms: 1.33x faster                                                         |
| deepcopy_reduce          | 4.17 us                                                | 3.14 us: 1.33x faster                                                        |
| genshi_text              | 31.8 ms                                                | 24.0 ms: 1.32x faster                                                        |
| html5lib                 | 88.9 ms                                                | 67.2 ms: 1.32x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                        |
| scimark_fft              | 466 ms                                                 | 353 ms: 1.32x faster                                                         |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                       |
| thrift                   | 1.07 ms                                                | 826 us: 1.30x faster                                                         |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                         |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.25x faster                                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.19 ms: 1.25x faster                                                        |
| genshi_xml               | 66.0 ms                                                | 53.9 ms: 1.23x faster                                                        |
| dulwich_log              | 84.3 ms                                                | 69.3 ms: 1.22x faster                                                        |
| sqlglot_optimize         | 69.2 ms                                                | 57.6 ms: 1.20x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.20 ms: 1.19x faster                                                        |
| djangocms                | 38.4 us                                                | 32.4 us: 1.19x faster                                                        |
| nqueens                  | 106 ms                                                 | 89.6 ms: 1.18x faster                                                        |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                        |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                        |
| dask                     | 441 ms                                                 | 375 ms: 1.17x faster                                                         |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                         |
| sympy_str                | 346 ms                                                 | 297 ms: 1.16x faster                                                         |
| bench_thread_pool        | 986 us                                                 | 855 us: 1.15x faster                                                         |
| mypy2                    | 894 ms                                                 | 781 ms: 1.14x faster                                                         |
| pathlib                  | 20.5 ms                                                | 17.9 ms: 1.14x faster                                                        |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                        |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                       |
| sympy_expand             | 566 ms                                                 | 498 ms: 1.14x faster                                                         |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                        |
| json                     | 5.69 ms                                                | 5.15 ms: 1.11x faster                                                        |
| regex_v8                 | 27.8 ms                                                | 25.3 ms: 1.10x faster                                                        |
| mdp                      | 2.85 sec                                               | 2.62 sec: 1.09x faster                                                       |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                         |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                         |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                         |
| unpickle_list            | 5.20 us                                                | 5.00 us: 1.04x faster                                                        |
| sqlite_synth             | 3.02 us                                                | 2.91 us: 1.04x faster                                                        |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                         |
| regex_dna                | 227 ms                                                 | 228 ms: 1.01x slower                                                         |
| pickle_list              | 5.08 us                                                | 5.15 us: 1.01x slower                                                        |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                         |
| regex_effbot             | 3.63 ms                                                | 3.78 ms: 1.04x slower                                                        |
| async_generators         | 444 ms                                                 | 462 ms: 1.04x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                        |
| gc_traversal             | 3.62 ms                                                | 3.89 ms: 1.07x slower                                                        |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                        |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                        |
| telco                    | 7.27 ms                                                | 8.64 ms: 1.19x slower                                                        |
| pickle_dict              | 29.6 us                                                | 35.7 us: 1.21x slower                                                        |
| coverage                 | 79.4 ms                                                | 98.4 ms: 1.24x slower                                                        |
| python_startup_no_site   | 5.93 ms                                                | 7.55 ms: 1.27x slower                                                        |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                 |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240418-3.13.0a6+-377ec17-JIT/bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.18x