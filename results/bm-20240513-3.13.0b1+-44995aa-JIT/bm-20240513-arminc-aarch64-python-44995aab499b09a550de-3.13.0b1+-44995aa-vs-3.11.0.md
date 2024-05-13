# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: linux-aarch64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.06x slower
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 362 ms: 1.21x slower                                                     |
| chameleon      | 8.29 ms                                                               | 9.14 ms: 1.10x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.55 sec: 1.22x slower                                                   |
| html5lib       | 65.3 ms                                                               | 70.2 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 496 ms: 1.41x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 614 ms: 1.35x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 654 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 806 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 817 ms: 1.13x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 116 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 248 ms: 1.04x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.87 ms: 1.14x slower                                                    |
| regex_compile  | 137 ms                                                                | 167 ms: 1.23x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 187 ms: 1.12x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.65 us: 1.03x faster                                                    |
| unpickle_pure_python | 278 us                                                                | 277 us: 1.01x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.65 sec: 1.01x slower                                                   |
| pickle_dict          | 37.6 us                                                               | 38.2 us: 1.02x slower                                                    |
| pickle_list          | 5.01 us                                                               | 5.20 us: 1.04x slower                                                    |
| pickle_pure_python   | 374 us                                                                | 393 us: 1.05x slower                                                     |
| xml_etree_process    | 76.1 ms                                                               | 80.6 ms: 1.06x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.1 us: 1.06x slower                                                    |
| pickle               | 12.8 us                                                               | 13.7 us: 1.07x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 118 ms: 1.13x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                    |
| python_startup         | 10.2 ms                                                               | 15.1 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 49.5 ms: 1.18x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 33.9 ms: 1.20x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 82.0 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 207 us: 3.16x faster                                                     |
| generators                 | 64.2 ms                                                               | 38.8 ms: 1.66x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 624 ms: 1.48x faster                                                     |
| async_tree_none            | 701 ms                                                                | 496 ms: 1.41x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.27 sec: 1.41x faster                                                   |
| async_tree_memoization_tg  | 828 ms                                                                | 614 ms: 1.35x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 654 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| comprehensions             | 29.0 us                                                               | 23.1 us: 1.26x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 806 ms: 1.19x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 28.8 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 817 ms: 1.13x faster                                                     |
| richards_super             | 70.2 ms                                                               | 62.3 ms: 1.13x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 187 ms: 1.12x faster                                                     |
| raytrace                   | 351 ms                                                                | 327 ms: 1.07x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 23.4 ms: 1.06x faster                                                    |
| richards                   | 58.1 ms                                                               | 55.2 ms: 1.05x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.59 ms: 1.04x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.33 us: 1.03x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.65 us: 1.03x faster                                                    |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 4.63 ms: 1.02x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.32 ms: 1.02x faster                                                    |
| unpickle_pure_python       | 278 us                                                                | 277 us: 1.01x faster                                                     |
| asyncio_websockets         | 656 ms                                                                | 662 ms: 1.01x slower                                                     |
| tomli_loads                | 2.62 sec                                                              | 2.65 sec: 1.01x slower                                                   |
| deepcopy_memo              | 49.0 us                                                               | 49.8 us: 1.02x slower                                                    |
| pickle_dict                | 37.6 us                                                               | 38.2 us: 1.02x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.03 ms: 1.02x slower                                                    |
| json                       | 5.52 ms                                                               | 5.65 ms: 1.02x slower                                                    |
| nbody                      | 113 ms                                                                | 116 ms: 1.03x slower                                                     |
| meteor_contest             | 115 ms                                                                | 119 ms: 1.03x slower                                                     |
| dask                       | 385 ms                                                                | 397 ms: 1.03x slower                                                     |
| regex_dna                  | 239 ms                                                                | 248 ms: 1.04x slower                                                     |
| pickle_list                | 5.01 us                                                               | 5.20 us: 1.04x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.48 sec: 1.04x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 393 us: 1.05x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 87.6 ms: 1.05x slower                                                    |
| logging_silent             | 133 ns                                                                | 140 ns: 1.05x slower                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 7.87 ms: 1.06x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 80.6 ms: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                                    |
| fannkuch                   | 451 ms                                                                | 479 ms: 1.06x slower                                                     |
| thrift                     | 910 us                                                                | 972 us: 1.07x slower                                                     |
| pickle                     | 12.8 us                                                               | 13.7 us: 1.07x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 70.2 ms: 1.08x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 182 ms: 1.08x slower                                                     |
| dulwich_log                | 63.2 ms                                                               | 68.7 ms: 1.09x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.87 us: 1.09x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                   |
| go                         | 163 ms                                                                | 178 ms: 1.09x slower                                                     |
| sympy_str                  | 295 ms                                                                | 324 ms: 1.10x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 9.14 ms: 1.10x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 146 ms: 1.10x slower                                                     |
| gunicorn                   | 1.19 ms                                                               | 1.31 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.97 ms: 1.11x slower                                                    |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.12x slower                                                     |
| sympy_integrate            | 23.2 ms                                                               | 26.0 ms: 1.12x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 71.3 ms: 1.13x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 118 ms: 1.13x slower                                                     |
| chaos                      | 78.8 ms                                                               | 89.2 ms: 1.13x slower                                                    |
| sympy_expand               | 482 ms                                                                | 548 ms: 1.14x slower                                                     |
| scimark_fft                | 402 ms                                                                | 458 ms: 1.14x slower                                                     |
| regex_effbot               | 4.25 ms                                                               | 4.87 ms: 1.14x slower                                                    |
| nqueens                    | 102 ms                                                                | 118 ms: 1.15x slower                                                     |
| deepcopy                   | 435 us                                                                | 502 us: 1.15x slower                                                     |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                    |
| coverage                   | 84.1 ms                                                               | 99.1 ms: 1.18x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.34 ms: 1.18x slower                                                    |
| django_template            | 41.8 ms                                                               | 49.5 ms: 1.18x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 8.97 ms: 1.18x slower                                                    |
| pyflate                    | 516 ms                                                                | 613 ms: 1.19x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.66 us: 1.20x slower                                                    |
| scimark_sor                | 145 ms                                                                | 175 ms: 1.20x slower                                                     |
| genshi_text                | 28.2 ms                                                               | 33.9 ms: 1.20x slower                                                    |
| 2to3                       | 300 ms                                                                | 362 ms: 1.21x slower                                                     |
| flaskblogging              | 4.19 ms                                                               | 5.06 ms: 1.21x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.55 sec: 1.22x slower                                                   |
| regex_compile              | 137 ms                                                                | 167 ms: 1.23x slower                                                     |
| gc_traversal               | 4.33 ms                                                               | 5.30 ms: 1.23x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 1.11 sec: 1.23x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.32 sec: 1.25x slower                                                   |
| mypy2                      | 737 ms                                                                | 946 ms: 1.28x slower                                                     |
| create_gc_cycles           | 1.87 ms                                                               | 2.45 ms: 1.31x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 184 ms: 1.32x slower                                                     |
| genshi_xml                 | 62.2 ms                                                               | 82.0 ms: 1.32x slower                                                    |
| async_generators           | 378 ms                                                                | 514 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.35 ms                                                               | 10.8 ms: 1.47x slower                                                    |
| python_startup             | 10.2 ms                                                               | 15.1 ms: 1.48x slower                                                    |
| telco                      | 7.80 ms                                                               | 167 ms: 21.38x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.06x slower                                                             |

Benchmark hidden because not significant (7): logging_format, xml_etree_iterparse, mako, crypto_pyaes, float, tornado_http, pylint
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.14x