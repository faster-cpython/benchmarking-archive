# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-aarch64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.03x slower
- HPT reliability: 99.74%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 360 ms: 1.20x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.19 ms: 1.11x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.58 sec: 1.23x slower                                                  |
| html5lib       | 65.3 ms                                                               | 71.3 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 630 ms: 1.32x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 685 ms: 1.27x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.27 sec: 1.26x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 491 ms: 1.26x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 788 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 822 ms: 1.16x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| nbody          | 113 ms                                                                | 115 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                   |
| regex_dna      | 239 ms                                                                | 251 ms: 1.05x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                                   |
| regex_compile  | 137 ms                                                                | 174 ms: 1.27x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| xml_etree_parse      | 209 ms                                                                | 196 ms: 1.07x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.43 us: 1.07x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 275 us: 1.01x faster                                                    |
| tomli_loads          | 2.62 sec                                                              | 2.66 sec: 1.02x slower                                                  |
| pickle_list          | 5.01 us                                                               | 5.27 us: 1.05x slower                                                   |
| json_loads           | 30.3 us                                                               | 32.0 us: 1.06x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 81.0 ms: 1.06x slower                                                   |
| pickle               | 12.8 us                                                               | 13.7 us: 1.07x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 405 us: 1.08x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 115 ms: 1.11x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 10.7 ms: 1.46x slower                                                   |
| python_startup         | 10.2 ms                                                               | 15.2 ms: 1.49x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.47x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                   |
| django_template | 41.8 ms                                                               | 50.4 ms: 1.21x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 34.8 ms: 1.23x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 81.7 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 212 us: 3.07x faster                                                    |
| generators                 | 64.2 ms                                                               | 39.9 ms: 1.61x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 611 ms: 1.51x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.23 sec: 1.43x faster                                                  |
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 630 ms: 1.32x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 685 ms: 1.27x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.27 sec: 1.26x faster                                                  |
| comprehensions             | 29.0 us                                                               | 22.9 us: 1.26x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 491 ms: 1.26x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 788 ms: 1.17x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 822 ms: 1.16x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 21.9 ms: 1.13x faster                                                   |
| richards_super             | 70.2 ms                                                               | 62.4 ms: 1.12x faster                                                   |
| raytrace                   | 351 ms                                                                | 325 ms: 1.08x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 196 ms: 1.07x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.43 us: 1.07x faster                                                   |
| richards                   | 58.1 ms                                                               | 54.7 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.57 ms: 1.05x faster                                                   |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.38 us: 1.02x faster                                                   |
| unpickle_pure_python       | 278 us                                                                | 275 us: 1.01x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.98 ms: 1.01x faster                                                   |
| asyncio_websockets         | 656 ms                                                                | 663 ms: 1.01x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 49.7 us: 1.01x slower                                                   |
| tomli_loads                | 2.62 sec                                                              | 2.66 sec: 1.02x slower                                                  |
| nbody                      | 113 ms                                                                | 115 ms: 1.02x slower                                                    |
| json                       | 5.52 ms                                                               | 5.62 ms: 1.02x slower                                                   |
| meteor_contest             | 115 ms                                                                | 118 ms: 1.02x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.43 sec: 1.02x slower                                                  |
| crypto_pyaes               | 86.5 ms                                                               | 89.5 ms: 1.03x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                   |
| logging_silent             | 133 ns                                                                | 138 ns: 1.04x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.27 us: 1.05x slower                                                   |
| regex_dna                  | 239 ms                                                                | 251 ms: 1.05x slower                                                    |
| fannkuch                   | 451 ms                                                                | 475 ms: 1.05x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.0 us: 1.06x slower                                                   |
| thrift                     | 910 us                                                                | 962 us: 1.06x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 88.6 ms: 1.06x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 81.0 ms: 1.06x slower                                                   |
| pylint                     | 397 ms                                                                | 423 ms: 1.06x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.7 us: 1.07x slower                                                   |
| sqlglot_normalize          | 132 ms                                                                | 143 ms: 1.08x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 405 us: 1.08x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                  |
| html5lib                   | 65.3 ms                                                               | 71.3 ms: 1.09x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.89 us: 1.09x slower                                                   |
| sqlglot_optimize           | 63.4 ms                                                               | 69.5 ms: 1.10x slower                                                   |
| sympy_str                  | 295 ms                                                                | 323 ms: 1.10x slower                                                    |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.95 ms: 1.11x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 9.19 ms: 1.11x slower                                                   |
| sympy_sum                  | 168 ms                                                                | 187 ms: 1.11x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 115 ms: 1.11x slower                                                    |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.11x slower                                                    |
| chaos                      | 78.8 ms                                                               | 88.2 ms: 1.12x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 70.8 ms: 1.12x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.41 ms: 1.13x slower                                                   |
| sympy_expand               | 482 ms                                                                | 548 ms: 1.14x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.4 ms: 1.14x slower                                                   |
| deepcopy                   | 435 us                                                                | 499 us: 1.15x slower                                                    |
| scimark_fft                | 402 ms                                                                | 462 ms: 1.15x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| nqueens                    | 102 ms                                                                | 120 ms: 1.17x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.96 ms: 1.18x slower                                                   |
| hexiom                     | 7.57 ms                                                               | 8.96 ms: 1.18x slower                                                   |
| coverage                   | 84.1 ms                                                               | 99.5 ms: 1.18x slower                                                   |
| scimark_sor                | 145 ms                                                                | 173 ms: 1.19x slower                                                    |
| pyflate                    | 516 ms                                                                | 616 ms: 1.19x slower                                                    |
| 2to3                       | 300 ms                                                                | 360 ms: 1.20x slower                                                    |
| django_template            | 41.8 ms                                                               | 50.4 ms: 1.21x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.25 ms: 1.21x slower                                                   |
| deepcopy_reduce            | 3.89 us                                                               | 4.74 us: 1.22x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.58 sec: 1.23x slower                                                  |
| genshi_text                | 28.2 ms                                                               | 34.8 ms: 1.23x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.11 sec: 1.23x slower                                                  |
| pprint_pformat             | 1.85 sec                                                              | 2.30 sec: 1.24x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 2.36 ms: 1.26x slower                                                   |
| regex_compile              | 137 ms                                                                | 174 ms: 1.27x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 181 ms: 1.29x slower                                                    |
| telco                      | 7.80 ms                                                               | 10.2 ms: 1.31x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 81.7 ms: 1.31x slower                                                   |
| async_generators           | 378 ms                                                                | 505 ms: 1.33x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 10.7 ms: 1.46x slower                                                   |
| python_startup             | 10.2 ms                                                               | 15.2 ms: 1.49x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.03x slower                                                            |

Benchmark hidden because not significant (8): deltablue, logging_format, bench_thread_pool, xml_etree_iterparse, float, tornado_http, pickle_dict, dask
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.74% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.14x