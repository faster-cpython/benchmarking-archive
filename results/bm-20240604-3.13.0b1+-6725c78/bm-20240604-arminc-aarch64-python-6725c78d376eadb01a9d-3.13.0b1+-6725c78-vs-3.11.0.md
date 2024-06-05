# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: linux-aarch64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.05x faster
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 304 ms: 1.01x slower                                                     |
| chameleon      | 8.29 ms                                                               | 8.99 ms: 1.09x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.07 sec: 1.05x slower                                                   |
| tornado_http   | 140 ms                                                                | 127 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 487 ms: 1.44x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.19 sec: 1.35x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 647 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 781 ms: 1.22x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 763 ms: 1.21x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| float          | 89.6 ms                                                               | 91.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| regex_dna      | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 190 ms: 1.10x faster                                                     |
| unpickle_pure_python | 278 us                                                                | 253 us: 1.10x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.48 us: 1.06x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 360 us: 1.04x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| pickle_list          | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| pickle               | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 81.7 ms: 1.07x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 114 ms: 1.10x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                             |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.55 ms: 1.16x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                                    |
| genshi_text    | 28.2 ms                                                               | 28.0 ms: 1.01x faster                                                    |
| mako           | 13.3 ms                                                               | 13.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 194 us: 3.37x faster                                                     |
| generators                 | 64.2 ms                                                               | 37.1 ms: 1.73x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 574 ms: 1.60x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.20 sec: 1.45x faster                                                   |
| async_tree_none            | 701 ms                                                                | 487 ms: 1.44x faster                                                     |
| comprehensions             | 29.0 us                                                               | 20.4 us: 1.42x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.19 sec: 1.35x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 647 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 3.85 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 781 ms: 1.22x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 763 ms: 1.21x faster                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.39 ms: 1.18x faster                                                    |
| raytrace                   | 351 ms                                                                | 298 ms: 1.18x faster                                                     |
| pylint                     | 397 ms                                                                | 338 ms: 1.17x faster                                                     |
| sympy_sum                  | 168 ms                                                                | 145 ms: 1.16x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                                    |
| chaos                      | 78.8 ms                                                               | 68.7 ms: 1.15x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.74 ms: 1.15x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                                    |
| richards_super             | 70.2 ms                                                               | 62.3 ms: 1.13x faster                                                    |
| sympy_str                  | 295 ms                                                                | 266 ms: 1.11x faster                                                     |
| xml_etree_parse            | 209 ms                                                                | 190 ms: 1.10x faster                                                     |
| unpickle_pure_python       | 278 us                                                                | 253 us: 1.10x faster                                                     |
| sympy_integrate            | 23.2 ms                                                               | 21.1 ms: 1.10x faster                                                    |
| tornado_http               | 140 ms                                                                | 127 ms: 1.10x faster                                                     |
| logging_simple             | 7.57 us                                                               | 7.01 us: 1.08x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.07x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 23.1 ms: 1.07x faster                                                    |
| hexiom                     | 7.57 ms                                                               | 7.10 ms: 1.07x faster                                                    |
| logging_format             | 8.22 us                                                               | 7.73 us: 1.06x faster                                                    |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| dulwich_log                | 63.2 ms                                                               | 59.7 ms: 1.06x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.48 us: 1.06x faster                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 7.04 ms: 1.06x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 82.0 ms: 1.06x faster                                                    |
| sympy_expand               | 482 ms                                                                | 461 ms: 1.04x faster                                                     |
| dask                       | 385 ms                                                                | 369 ms: 1.04x faster                                                     |
| sqlglot_normalize          | 132 ms                                                                | 127 ms: 1.04x faster                                                     |
| pickle_pure_python         | 374 us                                                                | 360 us: 1.04x faster                                                     |
| richards                   | 58.1 ms                                                               | 55.9 ms: 1.04x faster                                                    |
| nqueens                    | 102 ms                                                                | 98.8 ms: 1.04x faster                                                    |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| pycparser                  | 1.25 sec                                                              | 1.21 sec: 1.03x faster                                                   |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                                     |
| genshi_xml                 | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 82.5 ms: 1.01x faster                                                    |
| genshi_text                | 28.2 ms                                                               | 28.0 ms: 1.01x faster                                                    |
| mdp                        | 3.35 sec                                                              | 3.34 sec: 1.01x faster                                                   |
| scimark_lu                 | 140 ms                                                                | 140 ms: 1.00x slower                                                     |
| asyncio_websockets         | 656 ms                                                                | 661 ms: 1.01x slower                                                     |
| mako                       | 13.3 ms                                                               | 13.4 ms: 1.01x slower                                                    |
| 2to3                       | 300 ms                                                                | 304 ms: 1.01x slower                                                     |
| json                       | 5.52 ms                                                               | 5.60 ms: 1.01x slower                                                    |
| logging_silent             | 133 ns                                                                | 135 ns: 1.02x slower                                                     |
| float                      | 89.6 ms                                                               | 91.1 ms: 1.02x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 1.90 sec: 1.02x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 926 ms: 1.03x slower                                                     |
| deepcopy                   | 435 us                                                                | 448 us: 1.03x slower                                                     |
| mypy2                      | 737 ms                                                                | 764 ms: 1.04x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 50.8 us: 1.04x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.18 ms: 1.04x slower                                                    |
| regex_dna                  | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.56 ms: 1.04x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.06 us: 1.05x slower                                                    |
| thrift                     | 910 us                                                                | 951 us: 1.05x slower                                                     |
| gunicorn                   | 1.19 ms                                                               | 1.24 ms: 1.05x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.07 sec: 1.05x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.7 ms: 1.06x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 81.7 ms: 1.07x slower                                                    |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                                     |
| pyflate                    | 516 ms                                                                | 559 ms: 1.08x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 8.99 ms: 1.09x slower                                                    |
| scimark_sor                | 145 ms                                                                | 158 ms: 1.09x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.10x slower                                                     |
| sqlite_synth               | 3.56 us                                                               | 3.91 us: 1.10x slower                                                    |
| scimark_fft                | 402 ms                                                                | 444 ms: 1.10x slower                                                     |
| regex_effbot               | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.83 ms: 1.15x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.55 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| coverage                   | 84.1 ms                                                               | 98.3 ms: 1.17x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.22 ms: 1.21x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.31 ms: 1.23x slower                                                    |
| telco                      | 7.80 ms                                                               | 9.87 ms: 1.26x slower                                                    |
| python_startup             | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| async_generators           | 378 ms                                                                | 493 ms: 1.30x slower                                                     |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                             |

Benchmark hidden because not significant (6): sqlglot_optimize, nbody, fannkuch, pickle_dict, django_template, html5lib
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.79% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x