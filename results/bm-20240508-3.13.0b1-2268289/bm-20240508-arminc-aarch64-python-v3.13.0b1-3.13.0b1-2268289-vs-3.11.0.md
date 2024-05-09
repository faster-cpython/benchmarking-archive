# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b1
- machine: linux-aarch64
- commit hash: 2268289
- commit date: 2024-05-08
- overall geometric mean: 1.01x faster
- HPT reliability: 95.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| chameleon      | 8.29 ms                                                               | 9.23 ms: 1.11x slower                                        |
| docutils       | 2.92 sec                                                              | 3.12 sec: 1.07x slower                                       |
| html5lib       | 65.3 ms                                                               | 66.6 ms: 1.02x slower                                        |
| tornado_http   | 140 ms                                                                | 130 ms: 1.07x faster                                         |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.33x faster                                       |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.31x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                       |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 799 ms: 1.20x faster                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 795 ms: 1.16x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                         |
| nbody          | 113 ms                                                                | 110 ms: 1.02x faster                                         |
| float          | 89.6 ms                                                               | 90.7 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 130 ms: 1.05x faster                                         |
| regex_dna      | 239 ms                                                                | 257 ms: 1.07x slower                                         |
| regex_v8       | 29.1 ms                                                               | 31.5 ms: 1.08x slower                                        |
| regex_effbot   | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                        |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                        |
| unpickle_pure_python | 278 us                                                                | 255 us: 1.09x faster                                         |
| unpickle_list        | 6.86 us                                                               | 6.31 us: 1.09x faster                                        |
| xml_etree_parse      | 209 ms                                                                | 199 ms: 1.05x faster                                         |
| pickle_pure_python   | 374 us                                                                | 363 us: 1.03x faster                                         |
| xml_etree_iterparse  | 152 ms                                                                | 150 ms: 1.01x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                       |
| pickle_dict          | 37.6 us                                                               | 38.0 us: 1.01x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.26 us: 1.05x slower                                        |
| json_loads           | 30.3 us                                                               | 32.3 us: 1.07x slower                                        |
| pickle               | 12.8 us                                                               | 13.7 us: 1.07x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 82.2 ms: 1.08x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 118 ms: 1.14x slower                                         |
| unpickle             | 16.9 us                                                               | 19.5 us: 1.16x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.49 ms: 1.16x slower                                        |
| python_startup         | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| django_template | 41.8 ms                                                               | 42.6 ms: 1.02x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.00x faster                                                 |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240508-arminc-aarch64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 203 us: 3.21x faster                                         |
| generators                 | 64.2 ms                                                               | 37.3 ms: 1.72x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 545 ms: 1.69x faster                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.17 sec: 1.47x faster                                       |
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                         |
| comprehensions             | 29.0 us                                                               | 20.3 us: 1.42x faster                                        |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.33x faster                                       |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.31x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                       |
| deltablue                  | 4.75 ms                                                               | 3.90 ms: 1.22x faster                                        |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 799 ms: 1.20x faster                                         |
| chaos                      | 78.8 ms                                                               | 66.5 ms: 1.19x faster                                        |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.42 ms: 1.16x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 795 ms: 1.16x faster                                         |
| pylint                     | 397 ms                                                                | 344 ms: 1.16x faster                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.73 ms: 1.15x faster                                        |
| sympy_sum                  | 168 ms                                                                | 146 ms: 1.15x faster                                         |
| json_dumps                 | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                        |
| coroutines                 | 33.3 ms                                                               | 29.7 ms: 1.12x faster                                        |
| richards_super             | 70.2 ms                                                               | 62.8 ms: 1.12x faster                                        |
| unpickle_pure_python       | 278 us                                                                | 255 us: 1.09x faster                                         |
| sympy_str                  | 295 ms                                                                | 270 ms: 1.09x faster                                         |
| unpickle_list              | 6.86 us                                                               | 6.31 us: 1.09x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 21.4 ms: 1.08x faster                                        |
| pathlib                    | 24.8 ms                                                               | 23.1 ms: 1.07x faster                                        |
| hexiom                     | 7.57 ms                                                               | 7.07 ms: 1.07x faster                                        |
| tornado_http               | 140 ms                                                                | 130 ms: 1.07x faster                                         |
| dulwich_log                | 63.2 ms                                                               | 59.5 ms: 1.06x faster                                        |
| bench_thread_pool          | 1.36 ms                                                               | 1.28 ms: 1.06x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.15 us: 1.06x faster                                        |
| bench_mp_pool              | 7.44 ms                                                               | 7.04 ms: 1.06x faster                                        |
| logging_format             | 8.22 us                                                               | 7.78 us: 1.06x faster                                        |
| xml_etree_parse            | 209 ms                                                                | 199 ms: 1.05x faster                                         |
| regex_compile              | 137 ms                                                                | 130 ms: 1.05x faster                                         |
| crypto_pyaes               | 86.5 ms                                                               | 82.4 ms: 1.05x faster                                        |
| richards                   | 58.1 ms                                                               | 56.3 ms: 1.03x faster                                        |
| pickle_pure_python         | 374 us                                                                | 363 us: 1.03x faster                                         |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                         |
| sqlglot_normalize          | 132 ms                                                                | 129 ms: 1.03x faster                                         |
| sympy_expand               | 482 ms                                                                | 470 ms: 1.02x faster                                         |
| nbody                      | 113 ms                                                                | 110 ms: 1.02x faster                                         |
| dask                       | 385 ms                                                                | 378 ms: 1.02x faster                                         |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                         |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                         |
| nqueens                    | 102 ms                                                                | 101 ms: 1.01x faster                                         |
| xml_etree_iterparse        | 152 ms                                                                | 150 ms: 1.01x faster                                         |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| mdp                        | 3.35 sec                                                              | 3.34 sec: 1.01x faster                                       |
| scimark_lu                 | 140 ms                                                                | 139 ms: 1.00x faster                                         |
| tomli_loads                | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                       |
| pickle_dict                | 37.6 us                                                               | 38.0 us: 1.01x slower                                        |
| float                      | 89.6 ms                                                               | 90.7 ms: 1.01x slower                                        |
| asyncio_websockets         | 656 ms                                                                | 666 ms: 1.02x slower                                         |
| django_template            | 41.8 ms                                                               | 42.6 ms: 1.02x slower                                        |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| html5lib                   | 65.3 ms                                                               | 66.6 ms: 1.02x slower                                        |
| json                       | 5.52 ms                                                               | 5.65 ms: 1.02x slower                                        |
| fannkuch                   | 451 ms                                                                | 465 ms: 1.03x slower                                         |
| deepcopy_memo              | 49.0 us                                                               | 51.0 us: 1.04x slower                                        |
| thrift                     | 910 us                                                                | 946 us: 1.04x slower                                         |
| deepcopy                   | 435 us                                                                | 453 us: 1.04x slower                                         |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.56 ms: 1.04x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 1.94 sec: 1.05x slower                                       |
| mypy2                      | 737 ms                                                                | 771 ms: 1.05x slower                                         |
| pickle_list                | 5.01 us                                                               | 5.26 us: 1.05x slower                                        |
| pprint_safe_repr           | 903 ms                                                                | 948 ms: 1.05x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 4.09 us: 1.05x slower                                        |
| aiohttp                    | 1.13 ms                                                               | 1.20 ms: 1.06x slower                                        |
| spectral_norm              | 131 ms                                                                | 139 ms: 1.06x slower                                         |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                        |
| docutils                   | 2.92 sec                                                              | 3.12 sec: 1.07x slower                                       |
| pickle                     | 12.8 us                                                               | 13.7 us: 1.07x slower                                        |
| regex_dna                  | 239 ms                                                                | 257 ms: 1.07x slower                                         |
| xml_etree_process          | 76.1 ms                                                               | 82.2 ms: 1.08x slower                                        |
| regex_v8                   | 29.1 ms                                                               | 31.5 ms: 1.08x slower                                        |
| sqlite_synth               | 3.56 us                                                               | 3.89 us: 1.09x slower                                        |
| scimark_sor                | 145 ms                                                                | 160 ms: 1.10x slower                                         |
| scimark_fft                | 402 ms                                                                | 442 ms: 1.10x slower                                         |
| chameleon                  | 8.29 ms                                                               | 9.23 ms: 1.11x slower                                        |
| xml_etree_generate         | 104 ms                                                                | 118 ms: 1.14x slower                                         |
| pyflate                    | 516 ms                                                                | 595 ms: 1.15x slower                                         |
| flaskblogging              | 4.19 ms                                                               | 4.84 ms: 1.16x slower                                        |
| python_startup_no_site     | 7.35 ms                                                               | 8.49 ms: 1.16x slower                                        |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                        |
| regex_effbot               | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                        |
| coverage                   | 84.1 ms                                                               | 98.6 ms: 1.17x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 5.09 ms: 1.18x slower                                        |
| python_startup             | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                        |
| async_generators           | 378 ms                                                                | 488 ms: 1.29x slower                                         |
| create_gc_cycles           | 1.87 ms                                                               | 2.43 ms: 1.30x slower                                        |
| telco                      | 7.80 ms                                                               | 167 ms: 21.46x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (7): genshi_xml, pycparser, genshi_text, scimark_monte_carlo, sqlglot_optimize, logging_silent, gunicorn
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 95.37% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x