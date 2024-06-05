# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: linux-aarch64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 357 ms: 1.19x slower                                                     |
| chameleon      | 8.29 ms                                                               | 10.3 ms: 1.24x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.60 sec: 1.23x slower                                                   |
| html5lib       | 65.3 ms                                                               | 73.8 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 522 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 637 ms: 1.30x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 685 ms: 1.27x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.27 sec: 1.26x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 505 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 827 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 807 ms: 1.14x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| float          | 89.6 ms                                                               | 119 ms: 1.32x slower                                                     |
| nbody          | 113 ms                                                                | 152 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.20x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.8 ms: 1.06x slower                                                    |
| regex_dna      | 239 ms                                                                | 258 ms: 1.08x slower                                                     |
| regex_effbot   | 4.25 ms                                                               | 4.92 ms: 1.16x slower                                                    |
| regex_compile  | 137 ms                                                                | 172 ms: 1.26x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 14.0 ms: 1.10x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.68 us: 1.03x faster                                                    |
| pickle_dict          | 37.6 us                                                               | 37.9 us: 1.01x slower                                                    |
| pickle               | 12.8 us                                                               | 13.5 us: 1.05x slower                                                    |
| pickle_list          | 5.01 us                                                               | 5.31 us: 1.06x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.1 us: 1.06x slower                                                    |
| xml_etree_iterparse  | 152 ms                                                                | 162 ms: 1.06x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.9 us: 1.18x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 90.9 ms: 1.19x slower                                                    |
| tomli_loads          | 2.62 sec                                                              | 3.23 sec: 1.23x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 467 us: 1.25x slower                                                     |
| xml_etree_generate   | 104 ms                                                                | 130 ms: 1.25x slower                                                     |
| unpickle_pure_python | 278 us                                                                | 364 us: 1.31x slower                                                     |
| Geometric mean       | (ref)                                                                 | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.77 ms: 1.19x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.2 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 51.1 ms: 1.22x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 78.6 ms: 1.26x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 36.8 ms: 1.31x slower                                                    |
| mako            | 13.3 ms                                                               | 17.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240604-arminc-aarch64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 227 us: 2.87x faster                                                     |
| generators                 | 64.2 ms                                                               | 40.7 ms: 1.58x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 602 ms: 1.53x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.27 sec: 1.41x faster                                                   |
| async_tree_none            | 701 ms                                                                | 522 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 637 ms: 1.30x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 685 ms: 1.27x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.27 sec: 1.26x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 505 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 827 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 807 ms: 1.14x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 14.0 ms: 1.10x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 30.3 ms: 1.10x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 23.4 ms: 1.06x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.68 us: 1.03x faster                                                    |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| logging_simple             | 7.57 us                                                               | 7.43 us: 1.02x faster                                                    |
| raytrace                   | 351 ms                                                                | 347 ms: 1.01x faster                                                     |
| asyncio_websockets         | 656 ms                                                                | 661 ms: 1.01x slower                                                     |
| pickle_dict                | 37.6 us                                                               | 37.9 us: 1.01x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 176 ms: 1.05x slower                                                     |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.05x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 66.7 ms: 1.06x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.31 us: 1.06x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.8 ms: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                                    |
| xml_etree_iterparse        | 152 ms                                                                | 162 ms: 1.06x slower                                                     |
| thrift                     | 910 us                                                                | 969 us: 1.07x slower                                                     |
| json                       | 5.52 ms                                                               | 5.89 ms: 1.07x slower                                                    |
| richards_super             | 70.2 ms                                                               | 75.4 ms: 1.07x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.61 sec: 1.08x slower                                                   |
| regex_dna                  | 239 ms                                                                | 258 ms: 1.08x slower                                                     |
| sympy_str                  | 295 ms                                                                | 318 ms: 1.08x slower                                                     |
| sympy_expand               | 482 ms                                                                | 523 ms: 1.09x slower                                                     |
| comprehensions             | 29.0 us                                                               | 31.5 us: 1.09x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.38 sec: 1.10x slower                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.83 ms: 1.11x slower                                                    |
| deltablue                  | 4.75 ms                                                               | 5.31 ms: 1.12x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.25 ms: 1.13x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 73.8 ms: 1.13x slower                                                    |
| chaos                      | 78.8 ms                                                               | 89.3 ms: 1.13x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 4.04 us: 1.13x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 151 ms: 1.14x slower                                                     |
| sympy_integrate            | 23.2 ms                                                               | 26.6 ms: 1.15x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 73.0 ms: 1.15x slower                                                    |
| gunicorn                   | 1.19 ms                                                               | 1.37 ms: 1.15x slower                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 8.58 ms: 1.15x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.31 ms: 1.16x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.92 ms: 1.16x slower                                                    |
| meteor_contest             | 115 ms                                                                | 135 ms: 1.17x slower                                                     |
| mypy2                      | 737 ms                                                                | 866 ms: 1.18x slower                                                     |
| unpickle                   | 16.9 us                                                               | 19.9 us: 1.18x slower                                                    |
| coverage                   | 84.1 ms                                                               | 99.3 ms: 1.18x slower                                                    |
| richards                   | 58.1 ms                                                               | 68.9 ms: 1.19x slower                                                    |
| 2to3                       | 300 ms                                                                | 357 ms: 1.19x slower                                                     |
| python_startup_no_site     | 7.35 ms                                                               | 8.77 ms: 1.19x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 90.9 ms: 1.19x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.21 ms: 1.20x slower                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 106 ms: 1.22x slower                                                     |
| django_template            | 41.8 ms                                                               | 51.1 ms: 1.22x slower                                                    |
| go                         | 163 ms                                                                | 199 ms: 1.22x slower                                                     |
| docutils                   | 2.92 sec                                                              | 3.60 sec: 1.23x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 5.17 ms: 1.23x slower                                                    |
| tomli_loads                | 2.62 sec                                                              | 3.23 sec: 1.23x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 10.3 ms: 1.24x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 467 us: 1.25x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 130 ms: 1.25x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.88 us: 1.26x slower                                                    |
| regex_compile              | 137 ms                                                                | 172 ms: 1.26x slower                                                     |
| genshi_xml                 | 62.2 ms                                                               | 78.6 ms: 1.26x slower                                                    |
| fannkuch                   | 451 ms                                                                | 574 ms: 1.27x slower                                                     |
| deepcopy                   | 435 us                                                                | 555 us: 1.27x slower                                                     |
| create_gc_cycles           | 1.87 ms                                                               | 2.41 ms: 1.29x slower                                                    |
| python_startup             | 10.2 ms                                                               | 13.2 ms: 1.29x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 36.8 ms: 1.31x slower                                                    |
| unpickle_pure_python       | 278 us                                                                | 364 us: 1.31x slower                                                     |
| nqueens                    | 102 ms                                                                | 134 ms: 1.31x slower                                                     |
| mako                       | 13.3 ms                                                               | 17.5 ms: 1.32x slower                                                    |
| float                      | 89.6 ms                                                               | 119 ms: 1.32x slower                                                     |
| pprint_pformat             | 1.85 sec                                                              | 2.47 sec: 1.33x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 8.41 ms: 1.34x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 1.21 sec: 1.34x slower                                                   |
| nbody                      | 113 ms                                                                | 152 ms: 1.35x slower                                                     |
| async_generators           | 378 ms                                                                | 517 ms: 1.37x slower                                                     |
| scimark_sor                | 145 ms                                                                | 200 ms: 1.38x slower                                                     |
| scimark_fft                | 402 ms                                                                | 558 ms: 1.39x slower                                                     |
| telco                      | 7.80 ms                                                               | 10.9 ms: 1.39x slower                                                    |
| pyflate                    | 516 ms                                                                | 738 ms: 1.43x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 120 ms: 1.45x slower                                                     |
| spectral_norm              | 131 ms                                                                | 191 ms: 1.46x slower                                                     |
| hexiom                     | 7.57 ms                                                               | 11.3 ms: 1.49x slower                                                    |
| logging_silent             | 133 ns                                                                | 199 ns: 1.50x slower                                                     |
| scimark_lu                 | 140 ms                                                                | 215 ms: 1.53x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 75.8 us: 1.55x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                             |

Benchmark hidden because not significant (5): tornado_http, logging_format, pylint, bench_thread_pool, dask
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.05x