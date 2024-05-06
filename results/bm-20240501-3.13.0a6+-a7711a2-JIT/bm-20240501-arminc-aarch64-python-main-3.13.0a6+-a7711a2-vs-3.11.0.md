# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: a7711a2
- commit date: 2024-05-01
- overall geometric mean: 1.01x slower
- HPT reliability: 97.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 348 ms: 1.16x slower                                     |
| chameleon      | 8.29 ms                                                               | 9.13 ms: 1.10x slower                                    |
| docutils       | 2.92 sec                                                              | 3.41 sec: 1.17x slower                                   |
| html5lib       | 65.3 ms                                                               | 70.3 ms: 1.08x slower                                    |
| Geometric mean | (ref)                                                                 | 1.10x slower                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 511 ms: 1.37x faster                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 616 ms: 1.34x faster                                     |
| async_tree_memoization     | 872 ms                                                                | 661 ms: 1.32x faster                                     |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                     |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.20 sec: 1.28x faster                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 775 ms: 1.19x faster                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 809 ms: 1.18x faster                                     |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 113 ms                                                                | 108 ms: 1.05x faster                                     |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                     |
| float          | 89.6 ms                                                               | 90.3 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                                 | 1.03x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 246 ms: 1.03x slower                                     |
| regex_v8       | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                    |
| regex_effbot   | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                    |
| regex_compile  | 137 ms                                                                | 159 ms: 1.17x slower                                     |
| Geometric mean | (ref)                                                                 | 1.09x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.9 ms: 1.20x faster                                    |
| xml_etree_parse      | 209 ms                                                                | 186 ms: 1.12x faster                                     |
| unpickle_list        | 6.86 us                                                               | 6.48 us: 1.06x faster                                    |
| pickle_pure_python   | 374 us                                                                | 356 us: 1.05x faster                                     |
| xml_etree_iterparse  | 152 ms                                                                | 148 ms: 1.02x faster                                     |
| tomli_loads          | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                   |
| unpickle_pure_python | 278 us                                                                | 277 us: 1.00x faster                                     |
| pickle_dict          | 37.6 us                                                               | 37.7 us: 1.00x slower                                    |
| json_loads           | 30.3 us                                                               | 31.8 us: 1.05x slower                                    |
| pickle_list          | 5.01 us                                                               | 5.26 us: 1.05x slower                                    |
| xml_etree_process    | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                    |
| pickle               | 12.8 us                                                               | 13.5 us: 1.06x slower                                    |
| xml_etree_generate   | 104 ms                                                                | 114 ms: 1.09x slower                                     |
| unpickle             | 16.9 us                                                               | 19.8 us: 1.17x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                    |
| python_startup_no_site | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.44x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                    |
| django_template | 41.8 ms                                                               | 48.5 ms: 1.16x slower                                    |
| genshi_text     | 28.2 ms                                                               | 33.6 ms: 1.19x slower                                    |
| genshi_xml      | 62.2 ms                                                               | 78.3 ms: 1.26x slower                                    |
| Geometric mean  | (ref)                                                                 | 1.14x slower                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 215 us: 3.04x faster                                     |
| generators                 | 64.2 ms                                                               | 38.1 ms: 1.69x faster                                    |
| asyncio_tcp                | 920 ms                                                                | 614 ms: 1.50x faster                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.26 sec: 1.41x faster                                   |
| async_tree_none            | 701 ms                                                                | 511 ms: 1.37x faster                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 616 ms: 1.34x faster                                     |
| async_tree_memoization     | 872 ms                                                                | 661 ms: 1.32x faster                                     |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                     |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.20 sec: 1.28x faster                                   |
| comprehensions             | 29.0 us                                                               | 23.4 us: 1.24x faster                                    |
| json_dumps                 | 15.4 ms                                                               | 12.9 ms: 1.20x faster                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 775 ms: 1.19x faster                                     |
| richards_super             | 70.2 ms                                                               | 59.4 ms: 1.18x faster                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 809 ms: 1.18x faster                                     |
| xml_etree_parse            | 209 ms                                                                | 186 ms: 1.12x faster                                     |
| richards                   | 58.1 ms                                                               | 52.3 ms: 1.11x faster                                    |
| coroutines                 | 33.3 ms                                                               | 30.0 ms: 1.11x faster                                    |
| raytrace                   | 351 ms                                                                | 316 ms: 1.11x faster                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.52 ms: 1.09x faster                                    |
| pathlib                    | 24.8 ms                                                               | 23.3 ms: 1.07x faster                                    |
| unpickle_list              | 6.86 us                                                               | 6.48 us: 1.06x faster                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.89 ms: 1.06x faster                                    |
| pickle_pure_python         | 374 us                                                                | 356 us: 1.05x faster                                     |
| nbody                      | 113 ms                                                                | 108 ms: 1.05x faster                                     |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                     |
| deltablue                  | 4.75 ms                                                               | 4.58 ms: 1.04x faster                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.31 ms: 1.03x faster                                    |
| xml_etree_iterparse        | 152 ms                                                                | 148 ms: 1.02x faster                                     |
| mako                       | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                    |
| tomli_loads                | 2.62 sec                                                              | 2.56 sec: 1.02x faster                                   |
| unpickle_pure_python       | 278 us                                                                | 277 us: 1.00x faster                                     |
| pickle_dict                | 37.6 us                                                               | 37.7 us: 1.00x slower                                    |
| asyncio_websockets         | 656 ms                                                                | 659 ms: 1.01x slower                                     |
| logging_format             | 8.22 us                                                               | 8.27 us: 1.01x slower                                    |
| float                      | 89.6 ms                                                               | 90.3 ms: 1.01x slower                                    |
| logging_silent             | 133 ns                                                                | 134 ns: 1.01x slower                                     |
| crypto_pyaes               | 86.5 ms                                                               | 87.2 ms: 1.01x slower                                    |
| logging_simple             | 7.57 us                                                               | 7.65 us: 1.01x slower                                    |
| json                       | 5.52 ms                                                               | 5.59 ms: 1.01x slower                                    |
| fannkuch                   | 451 ms                                                                | 460 ms: 1.02x slower                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 84.8 ms: 1.02x slower                                    |
| mdp                        | 3.35 sec                                                              | 3.44 sec: 1.03x slower                                   |
| deepcopy_memo              | 49.0 us                                                               | 50.3 us: 1.03x slower                                    |
| pycparser                  | 1.25 sec                                                              | 1.28 sec: 1.03x slower                                   |
| regex_dna                  | 239 ms                                                                | 246 ms: 1.03x slower                                     |
| dask                       | 385 ms                                                                | 397 ms: 1.03x slower                                     |
| meteor_contest             | 115 ms                                                                | 120 ms: 1.04x slower                                     |
| sqlglot_normalize          | 132 ms                                                                | 137 ms: 1.04x slower                                     |
| sympy_str                  | 295 ms                                                                | 306 ms: 1.04x slower                                     |
| regex_v8                   | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                    |
| sympy_sum                  | 168 ms                                                                | 175 ms: 1.04x slower                                     |
| json_loads                 | 30.3 us                                                               | 31.8 us: 1.05x slower                                    |
| pickle_list                | 5.01 us                                                               | 5.26 us: 1.05x slower                                    |
| chaos                      | 78.8 ms                                                               | 82.8 ms: 1.05x slower                                    |
| xml_etree_process          | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.11 us: 1.06x slower                                    |
| deepcopy                   | 435 us                                                                | 460 us: 1.06x slower                                     |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.06x slower                                    |
| thrift                     | 910 us                                                                | 971 us: 1.07x slower                                     |
| sqlglot_optimize           | 63.4 ms                                                               | 68.1 ms: 1.08x slower                                    |
| html5lib                   | 65.3 ms                                                               | 70.3 ms: 1.08x slower                                    |
| sympy_expand               | 482 ms                                                                | 519 ms: 1.08x slower                                     |
| sqlite_synth               | 3.56 us                                                               | 3.85 us: 1.08x slower                                    |
| spectral_norm              | 131 ms                                                                | 142 ms: 1.08x slower                                     |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.09x slower                                     |
| sympy_integrate            | 23.2 ms                                                               | 25.5 ms: 1.10x slower                                    |
| chameleon                  | 8.29 ms                                                               | 9.13 ms: 1.10x slower                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 7.02 ms: 1.12x slower                                    |
| dulwich_log                | 63.2 ms                                                               | 70.7 ms: 1.12x slower                                    |
| scimark_fft                | 402 ms                                                                | 454 ms: 1.13x slower                                     |
| regex_effbot               | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                    |
| go                         | 163 ms                                                                | 186 ms: 1.14x slower                                     |
| pyflate                    | 516 ms                                                                | 598 ms: 1.16x slower                                     |
| 2to3                       | 300 ms                                                                | 348 ms: 1.16x slower                                     |
| django_template            | 41.8 ms                                                               | 48.5 ms: 1.16x slower                                    |
| regex_compile              | 137 ms                                                                | 159 ms: 1.17x slower                                     |
| gc_traversal               | 4.33 ms                                                               | 5.05 ms: 1.17x slower                                    |
| docutils                   | 2.92 sec                                                              | 3.41 sec: 1.17x slower                                   |
| nqueens                    | 102 ms                                                                | 120 ms: 1.17x slower                                     |
| unpickle                   | 16.9 us                                                               | 19.8 us: 1.17x slower                                    |
| coverage                   | 84.1 ms                                                               | 99.2 ms: 1.18x slower                                    |
| hexiom                     | 7.57 ms                                                               | 8.94 ms: 1.18x slower                                    |
| genshi_text                | 28.2 ms                                                               | 33.6 ms: 1.19x slower                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.32 ms: 1.24x slower                                    |
| scimark_sor                | 145 ms                                                                | 181 ms: 1.24x slower                                     |
| genshi_xml                 | 62.2 ms                                                               | 78.3 ms: 1.26x slower                                    |
| telco                      | 7.80 ms                                                               | 9.88 ms: 1.27x slower                                    |
| scimark_lu                 | 140 ms                                                                | 178 ms: 1.27x slower                                     |
| pprint_safe_repr           | 903 ms                                                                | 1.17 sec: 1.30x slower                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.42 sec: 1.30x slower                                   |
| async_generators           | 378 ms                                                                | 501 ms: 1.32x slower                                     |
| python_startup             | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                    |
| python_startup_no_site     | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                    |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                             |

Benchmark hidden because not significant (3): tornado_http, bench_mp_pool, pylint
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 97.92% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x