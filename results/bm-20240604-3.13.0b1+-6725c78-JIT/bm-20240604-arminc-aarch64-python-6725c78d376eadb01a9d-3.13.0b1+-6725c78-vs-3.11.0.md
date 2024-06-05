# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: linux-aarch64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.04x slower
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 365 ms: 1.22x slower                                                     |
| chameleon      | 8.29 ms                                                               | 9.29 ms: 1.12x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.62 sec: 1.24x slower                                                   |
| html5lib       | 65.3 ms                                                               | 71.7 ms: 1.10x slower                                                    |
| tornado_http   | 140 ms                                                                | 150 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 504 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 623 ms: 1.33x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 666 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 489 ms: 1.27x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 817 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 801 ms: 1.15x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.04x faster                                                     |
| nbody          | 113 ms                                                                | 114 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                    |
| regex_dna      | 239 ms                                                                | 260 ms: 1.09x slower                                                     |
| regex_effbot   | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                    |
| regex_compile  | 137 ms                                                                | 176 ms: 1.29x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|--------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps         | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                    |
| xml_etree_parse    | 209 ms                                                                | 190 ms: 1.10x faster                                                     |
| unpickle_list      | 6.86 us                                                               | 6.63 us: 1.03x faster                                                    |
| pickle_list        | 5.01 us                                                               | 5.28 us: 1.05x slower                                                    |
| json_loads         | 30.3 us                                                               | 32.0 us: 1.06x slower                                                    |
| pickle_pure_python | 374 us                                                                | 396 us: 1.06x slower                                                     |
| pickle             | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| xml_etree_process  | 76.1 ms                                                               | 83.1 ms: 1.09x slower                                                    |
| xml_etree_generate | 104 ms                                                                | 117 ms: 1.12x slower                                                     |
| unpickle           | 16.9 us                                                               | 20.0 us: 1.19x slower                                                    |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                                             |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, tomli_loads, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 11.2 ms: 1.52x slower                                                    |
| python_startup         | 10.2 ms                                                               | 15.9 ms: 1.56x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.54x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                    |
| django_template | 41.8 ms                                                               | 49.8 ms: 1.19x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 34.3 ms: 1.22x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 83.0 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 207 us: 3.15x faster                                                     |
| generators                 | 64.2 ms                                                               | 39.5 ms: 1.63x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 645 ms: 1.43x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.28 sec: 1.40x faster                                                   |
| async_tree_none            | 701 ms                                                                | 504 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 623 ms: 1.33x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 666 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 489 ms: 1.27x faster                                                     |
| comprehensions             | 29.0 us                                                               | 23.1 us: 1.26x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                                   |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 817 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 801 ms: 1.15x faster                                                     |
| coroutines                 | 33.3 ms                                                               | 29.1 ms: 1.14x faster                                                    |
| richards_super             | 70.2 ms                                                               | 63.0 ms: 1.11x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 190 ms: 1.10x faster                                                     |
| raytrace                   | 351 ms                                                                | 318 ms: 1.10x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 23.3 ms: 1.06x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.27 us: 1.04x faster                                                    |
| pidigits                   | 242 ms                                                                | 234 ms: 1.04x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 4.58 ms: 1.04x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.63 us: 1.03x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.60 ms: 1.03x faster                                                    |
| richards                   | 58.1 ms                                                               | 56.5 ms: 1.03x faster                                                    |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                    |
| logging_format             | 8.22 us                                                               | 8.02 us: 1.02x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 87.1 ms: 1.01x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 49.4 us: 1.01x slower                                                    |
| asyncio_websockets         | 656 ms                                                                | 661 ms: 1.01x slower                                                     |
| meteor_contest             | 115 ms                                                                | 117 ms: 1.01x slower                                                     |
| nbody                      | 113 ms                                                                | 114 ms: 1.01x slower                                                     |
| mdp                        | 3.35 sec                                                              | 3.44 sec: 1.03x slower                                                   |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                                    |
| fannkuch                   | 451 ms                                                                | 469 ms: 1.04x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                    |
| logging_silent             | 133 ns                                                                | 138 ns: 1.04x slower                                                     |
| dask                       | 385 ms                                                                | 403 ms: 1.05x slower                                                     |
| pickle_list                | 5.01 us                                                               | 5.28 us: 1.05x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.0 us: 1.06x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 396 us: 1.06x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 88.1 ms: 1.06x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| thrift                     | 910 us                                                                | 971 us: 1.07x slower                                                     |
| tornado_http               | 140 ms                                                                | 150 ms: 1.07x slower                                                     |
| sqlglot_normalize          | 132 ms                                                                | 142 ms: 1.07x slower                                                     |
| pycparser                  | 1.25 sec                                                              | 1.34 sec: 1.08x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.87 us: 1.09x slower                                                    |
| regex_dna                  | 239 ms                                                                | 260 ms: 1.09x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 83.1 ms: 1.09x slower                                                    |
| chaos                      | 78.8 ms                                                               | 86.1 ms: 1.09x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 69.3 ms: 1.09x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 71.7 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.95 ms: 1.11x slower                                                    |
| go                         | 163 ms                                                                | 180 ms: 1.11x slower                                                     |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.11x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 9.29 ms: 1.12x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 117 ms: 1.12x slower                                                     |
| sympy_str                  | 295 ms                                                                | 332 ms: 1.13x slower                                                     |
| nqueens                    | 102 ms                                                                | 116 ms: 1.13x slower                                                     |
| sympy_sum                  | 168 ms                                                                | 191 ms: 1.14x slower                                                     |
| deepcopy                   | 435 us                                                                | 497 us: 1.14x slower                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 8.50 ms: 1.14x slower                                                    |
| scimark_fft                | 402 ms                                                                | 460 ms: 1.14x slower                                                     |
| sympy_integrate            | 23.2 ms                                                               | 26.7 ms: 1.15x slower                                                    |
| gunicorn                   | 1.19 ms                                                               | 1.37 ms: 1.15x slower                                                    |
| pyflate                    | 516 ms                                                                | 599 ms: 1.16x slower                                                     |
| regex_effbot               | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                    |
| sympy_expand               | 482 ms                                                                | 561 ms: 1.16x slower                                                     |
| coverage                   | 84.1 ms                                                               | 98.4 ms: 1.17x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 8.91 ms: 1.18x slower                                                    |
| unpickle                   | 16.9 us                                                               | 20.0 us: 1.19x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.35 ms: 1.19x slower                                                    |
| scimark_sor                | 145 ms                                                                | 173 ms: 1.19x slower                                                     |
| django_template            | 41.8 ms                                                               | 49.8 ms: 1.19x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.64 us: 1.19x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.19 ms: 1.20x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 34.3 ms: 1.22x slower                                                    |
| 2to3                       | 300 ms                                                                | 365 ms: 1.22x slower                                                     |
| pprint_safe_repr           | 903 ms                                                                | 1.10 sec: 1.22x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 77.4 ms: 1.22x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.62 sec: 1.24x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.32 sec: 1.25x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 5.25 ms: 1.25x slower                                                    |
| mypy2                      | 737 ms                                                                | 938 ms: 1.27x slower                                                     |
| regex_compile              | 137 ms                                                                | 176 ms: 1.29x slower                                                     |
| create_gc_cycles           | 1.87 ms                                                               | 2.42 ms: 1.30x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 183 ms: 1.30x slower                                                     |
| telco                      | 7.80 ms                                                               | 10.3 ms: 1.32x slower                                                    |
| genshi_xml                 | 62.2 ms                                                               | 83.0 ms: 1.33x slower                                                    |
| async_generators           | 378 ms                                                                | 509 ms: 1.35x slower                                                     |
| python_startup_no_site     | 7.35 ms                                                               | 11.2 ms: 1.52x slower                                                    |
| python_startup             | 10.2 ms                                                               | 15.9 ms: 1.56x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.04x slower                                                             |

Benchmark hidden because not significant (8): xml_etree_iterparse, unpickle_pure_python, float, bench_thread_pool, tomli_loads, sqlglot_transpile, pickle_dict, pylint
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.82% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x