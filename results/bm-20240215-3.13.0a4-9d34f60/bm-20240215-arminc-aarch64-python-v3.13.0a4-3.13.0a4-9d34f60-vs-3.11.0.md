# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: linux-aarch64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.05x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| chameleon      | 8.29 ms                                                               | 8.93 ms: 1.08x slower                                        |
| tornado_http   | 140 ms                                                                | 133 ms: 1.05x faster                                         |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                 |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 564 ms: 1.24x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 737 ms: 1.18x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 728 ms: 1.14x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.42 sec: 1.13x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 567 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 880 ms: 1.09x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.43 sec: 1.08x faster                                       |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 887 ms: 1.04x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 106 ms: 1.07x faster                                         |
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| float          | 89.6 ms                                                               | 93.1 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 125 ms: 1.09x faster                                         |
| regex_v8       | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                        |
| regex_dna      | 239 ms                                                                | 253 ms: 1.06x slower                                         |
| regex_effbot   | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                        |
| unpickle_pure_python | 278 us                                                                | 255 us: 1.09x faster                                         |
| pickle_pure_python   | 374 us                                                                | 351 us: 1.07x faster                                         |
| unpickle_list        | 6.86 us                                                               | 6.46 us: 1.06x faster                                        |
| xml_etree_parse      | 209 ms                                                                | 198 ms: 1.06x faster                                         |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                       |
| xml_etree_process    | 76.1 ms                                                               | 79.1 ms: 1.04x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.22 us: 1.04x slower                                        |
| pickle               | 12.8 us                                                               | 13.5 us: 1.06x slower                                        |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                         |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                 |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 12.1 ms: 1.19x slower                                        |
| python_startup_no_site | 7.35 ms                                                               | 10.5 ms: 1.43x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.31x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 62.2 ms                                                               | 59.7 ms: 1.04x faster                                        |
| genshi_text     | 28.2 ms                                                               | 27.1 ms: 1.04x faster                                        |
| django_template | 41.8 ms                                                               | 40.3 ms: 1.04x faster                                        |
| mako            | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240215-arminc-aarch64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 133 us: 4.93x faster                                         |
| generators                 | 64.2 ms                                                               | 36.2 ms: 1.78x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 553 ms: 1.66x faster                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.20 sec: 1.45x faster                                       |
| comprehensions             | 29.0 us                                                               | 20.3 us: 1.43x faster                                        |
| async_tree_none            | 701 ms                                                                | 564 ms: 1.24x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.36 ms: 1.21x faster                                        |
| sympy_sum                  | 168 ms                                                                | 139 ms: 1.21x faster                                         |
| pylint                     | 397 ms                                                                | 334 ms: 1.19x faster                                         |
| raytrace                   | 351 ms                                                                | 295 ms: 1.19x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 737 ms: 1.18x faster                                         |
| deltablue                  | 4.75 ms                                                               | 4.03 ms: 1.18x faster                                        |
| chaos                      | 78.8 ms                                                               | 67.1 ms: 1.18x faster                                        |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                        |
| sqlglot_transpile          | 2.00 ms                                                               | 1.72 ms: 1.16x faster                                        |
| richards_super             | 70.2 ms                                                               | 60.6 ms: 1.16x faster                                        |
| sympy_str                  | 295 ms                                                                | 257 ms: 1.14x faster                                         |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                        |
| async_tree_memoization_tg  | 828 ms                                                                | 728 ms: 1.14x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.42 sec: 1.13x faster                                       |
| sympy_integrate            | 23.2 ms                                                               | 20.7 ms: 1.12x faster                                        |
| crypto_pyaes               | 86.5 ms                                                               | 78.8 ms: 1.10x faster                                        |
| async_tree_none_tg         | 620 ms                                                                | 567 ms: 1.09x faster                                         |
| unpickle_pure_python       | 278 us                                                                | 255 us: 1.09x faster                                         |
| regex_compile              | 137 ms                                                                | 125 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 880 ms: 1.09x faster                                         |
| hexiom                     | 7.57 ms                                                               | 6.98 ms: 1.08x faster                                        |
| async_tree_io_tg           | 1.54 sec                                                              | 1.43 sec: 1.08x faster                                       |
| sympy_expand               | 482 ms                                                                | 448 ms: 1.08x faster                                         |
| richards                   | 58.1 ms                                                               | 54.2 ms: 1.07x faster                                        |
| bench_mp_pool              | 7.44 ms                                                               | 6.96 ms: 1.07x faster                                        |
| pickle_pure_python         | 374 us                                                                | 351 us: 1.07x faster                                         |
| nbody                      | 113 ms                                                                | 106 ms: 1.07x faster                                         |
| dulwich_log                | 63.2 ms                                                               | 59.4 ms: 1.06x faster                                        |
| unpickle_list              | 6.86 us                                                               | 6.46 us: 1.06x faster                                        |
| nqueens                    | 102 ms                                                                | 96.6 ms: 1.06x faster                                        |
| sqlglot_normalize          | 132 ms                                                                | 125 ms: 1.06x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 198 ms: 1.06x faster                                         |
| logging_silent             | 133 ns                                                                | 126 ns: 1.05x faster                                         |
| tornado_http               | 140 ms                                                                | 133 ms: 1.05x faster                                         |
| pathlib                    | 24.8 ms                                                               | 23.7 ms: 1.05x faster                                        |
| bench_thread_pool          | 1.36 ms                                                               | 1.30 ms: 1.04x faster                                        |
| genshi_xml                 | 62.2 ms                                                               | 59.7 ms: 1.04x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.26 us: 1.04x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 887 ms: 1.04x faster                                         |
| genshi_text                | 28.2 ms                                                               | 27.1 ms: 1.04x faster                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 61.0 ms: 1.04x faster                                        |
| logging_format             | 8.22 us                                                               | 7.92 us: 1.04x faster                                        |
| django_template            | 41.8 ms                                                               | 40.3 ms: 1.04x faster                                        |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| scimark_lu                 | 140 ms                                                                | 138 ms: 1.02x faster                                         |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                         |
| tomli_loads                | 2.62 sec                                                              | 2.58 sec: 1.01x faster                                       |
| deepcopy_memo              | 49.0 us                                                               | 48.5 us: 1.01x faster                                        |
| meteor_contest             | 115 ms                                                                | 114 ms: 1.01x faster                                         |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| mdp                        | 3.35 sec                                                              | 3.34 sec: 1.00x faster                                       |
| asyncio_websockets         | 656 ms                                                                | 660 ms: 1.01x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 3.94 us: 1.01x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 4.39 ms: 1.01x slower                                        |
| thrift                     | 910 us                                                                | 926 us: 1.02x slower                                         |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| fannkuch                   | 451 ms                                                                | 461 ms: 1.02x slower                                         |
| pycparser                  | 1.25 sec                                                              | 1.28 sec: 1.03x slower                                       |
| json                       | 5.52 ms                                                               | 5.69 ms: 1.03x slower                                        |
| spectral_norm              | 131 ms                                                                | 135 ms: 1.03x slower                                         |
| regex_v8                   | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.53 ms: 1.04x slower                                        |
| float                      | 89.6 ms                                                               | 93.1 ms: 1.04x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 79.1 ms: 1.04x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.22 us: 1.04x slower                                        |
| create_gc_cycles           | 1.87 ms                                                               | 1.96 ms: 1.05x slower                                        |
| aiohttp                    | 1.13 ms                                                               | 1.19 ms: 1.05x slower                                        |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.06x slower                                        |
| regex_dna                  | 239 ms                                                                | 253 ms: 1.06x slower                                         |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| chameleon                  | 8.29 ms                                                               | 8.93 ms: 1.08x slower                                        |
| sqlite_synth               | 3.56 us                                                               | 3.84 us: 1.08x slower                                        |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                         |
| scimark_fft                | 402 ms                                                                | 442 ms: 1.10x slower                                         |
| flaskblogging              | 4.19 ms                                                               | 4.76 ms: 1.13x slower                                        |
| scimark_sor                | 145 ms                                                                | 166 ms: 1.14x slower                                         |
| regex_effbot               | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                        |
| pyflate                    | 516 ms                                                                | 597 ms: 1.16x slower                                         |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                        |
| python_startup             | 10.2 ms                                                               | 12.1 ms: 1.19x slower                                        |
| coverage                   | 84.1 ms                                                               | 102 ms: 1.21x slower                                         |
| telco                      | 7.80 ms                                                               | 9.57 ms: 1.23x slower                                        |
| mypy2                      | 737 ms                                                                | 915 ms: 1.24x slower                                         |
| async_generators           | 378 ms                                                                | 487 ms: 1.29x slower                                         |
| python_startup_no_site     | 7.35 ms                                                               | 10.5 ms: 1.43x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (8): docutils, deepcopy, pprint_safe_repr, pickle_dict, pprint_pformat, scimark_monte_carlo, html5lib, gunicorn
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x