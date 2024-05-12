# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: linux-aarch64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.02x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                                    |
| chameleon      | 8.29 ms                                                               | 8.99 ms: 1.08x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| html5lib       | 65.3 ms                                                               | 67.1 ms: 1.03x slower                                                   |
| tornado_http   | 140 ms                                                                | 133 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 487 ms: 1.44x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 644 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 624 ms: 1.33x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 789 ms: 1.17x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| float          | 89.6 ms                                                               | 90.2 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 130 ms: 1.05x faster                                                    |
| regex_v8       | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                   |
| regex_dna      | 239 ms                                                                | 254 ms: 1.06x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 252 us: 1.10x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 194 ms: 1.08x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.59 us: 1.04x faster                                                   |
| pickle_pure_python   | 374 us                                                                | 360 us: 1.04x faster                                                    |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                                    |
| tomli_loads          | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                                  |
| pickle_list          | 5.01 us                                                               | 5.20 us: 1.04x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 79.3 ms: 1.04x slower                                                   |
| json_loads           | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| xml_etree_generate   | 104 ms                                                                | 112 ms: 1.07x slower                                                    |
| pickle               | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.55 ms: 1.16x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.5 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 61.0 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (3): genshi_text, mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 196 us: 3.33x faster                                                    |
| generators                 | 64.2 ms                                                               | 39.3 ms: 1.63x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 576 ms: 1.60x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.21 sec: 1.44x faster                                                  |
| async_tree_none            | 701 ms                                                                | 487 ms: 1.44x faster                                                    |
| comprehensions             | 29.0 us                                                               | 20.9 us: 1.39x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 644 ms: 1.36x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 624 ms: 1.33x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| deltablue                  | 4.75 ms                                                               | 3.85 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                                    |
| raytrace                   | 351 ms                                                                | 296 ms: 1.18x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.40 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 789 ms: 1.17x faster                                                    |
| richards_super             | 70.2 ms                                                               | 60.3 ms: 1.16x faster                                                   |
| chaos                      | 78.8 ms                                                               | 67.8 ms: 1.16x faster                                                   |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| pylint                     | 397 ms                                                                | 343 ms: 1.16x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.75 ms: 1.14x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                                   |
| sympy_sum                  | 168 ms                                                                | 149 ms: 1.13x faster                                                    |
| unpickle_pure_python       | 278 us                                                                | 252 us: 1.10x faster                                                    |
| sympy_str                  | 295 ms                                                                | 269 ms: 1.09x faster                                                    |
| richards                   | 58.1 ms                                                               | 53.4 ms: 1.09x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 194 ms: 1.08x faster                                                    |
| sympy_integrate            | 23.2 ms                                                               | 21.6 ms: 1.07x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 23.1 ms: 1.07x faster                                                   |
| hexiom                     | 7.57 ms                                                               | 7.11 ms: 1.06x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.76 us: 1.06x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.15 us: 1.06x faster                                                   |
| bench_thread_pool          | 1.36 ms                                                               | 1.28 ms: 1.06x faster                                                   |
| crypto_pyaes               | 86.5 ms                                                               | 81.9 ms: 1.06x faster                                                   |
| tornado_http               | 140 ms                                                                | 133 ms: 1.05x faster                                                    |
| regex_compile              | 137 ms                                                                | 130 ms: 1.05x faster                                                    |
| sympy_expand               | 482 ms                                                                | 459 ms: 1.05x faster                                                    |
| nqueens                    | 102 ms                                                                | 98.0 ms: 1.05x faster                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 7.14 ms: 1.04x faster                                                   |
| unpickle_list              | 6.86 us                                                               | 6.59 us: 1.04x faster                                                   |
| pickle_pure_python         | 374 us                                                                | 360 us: 1.04x faster                                                    |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| dulwich_log                | 63.2 ms                                                               | 61.4 ms: 1.03x faster                                                   |
| sqlglot_normalize          | 132 ms                                                                | 129 ms: 1.03x faster                                                    |
| pycparser                  | 1.25 sec                                                              | 1.22 sec: 1.02x faster                                                  |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                                    |
| genshi_xml                 | 62.2 ms                                                               | 61.0 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                                    |
| scimark_lu                 | 140 ms                                                                | 138 ms: 1.01x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                                  |
| sqlglot_optimize           | 63.4 ms                                                               | 62.6 ms: 1.01x faster                                                   |
| float                      | 89.6 ms                                                               | 90.2 ms: 1.01x slower                                                   |
| asyncio_websockets         | 656 ms                                                                | 663 ms: 1.01x slower                                                    |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                                    |
| fannkuch                   | 451 ms                                                                | 461 ms: 1.02x slower                                                    |
| json                       | 5.52 ms                                                               | 5.67 ms: 1.03x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 67.1 ms: 1.03x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 1.92 sec: 1.04x slower                                                  |
| pickle_list                | 5.01 us                                                               | 5.20 us: 1.04x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 79.3 ms: 1.04x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 941 ms: 1.04x slower                                                    |
| deepcopy                   | 435 us                                                                | 454 us: 1.04x slower                                                    |
| thrift                     | 910 us                                                                | 952 us: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.58 ms: 1.05x slower                                                   |
| deepcopy_memo              | 49.0 us                                                               | 51.4 us: 1.05x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| regex_dna                  | 239 ms                                                                | 254 ms: 1.06x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.15 us: 1.07x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 112 ms: 1.07x slower                                                    |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| scimark_sor                | 145 ms                                                                | 158 ms: 1.08x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 8.99 ms: 1.08x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.90 us: 1.10x slower                                                   |
| scimark_fft                | 402 ms                                                                | 444 ms: 1.10x slower                                                    |
| pyflate                    | 516 ms                                                                | 581 ms: 1.13x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                   |
| coverage                   | 84.1 ms                                                               | 97.5 ms: 1.16x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 8.55 ms: 1.16x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 4.98 ms: 1.19x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.14 ms: 1.19x slower                                                   |
| python_startup             | 10.2 ms                                                               | 12.5 ms: 1.22x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.40 ms: 1.28x slower                                                   |
| async_generators           | 378 ms                                                                | 489 ms: 1.29x slower                                                    |
| telco                      | 7.80 ms                                                               | 164 ms: 20.99x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                                            |

Benchmark hidden because not significant (10): go, nbody, pickle_dict, genshi_text, dask, mako, mdp, django_template, logging_silent, scimark_monte_carlo
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x