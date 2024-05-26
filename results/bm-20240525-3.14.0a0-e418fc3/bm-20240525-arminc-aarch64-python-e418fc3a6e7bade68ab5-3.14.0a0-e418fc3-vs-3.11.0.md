# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-aarch64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.05x faster
- HPT reliability: 99.68%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.16 ms: 1.10x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| tornado_http   | 140 ms                                                                | 130 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 490 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 600 ms: 1.38x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 647 ms: 1.35x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.20 sec: 1.34x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 467 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 756 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 784 ms: 1.22x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                  |
| Geometric mean             | (ref)                                                                 | 1.31x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| float          | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                                    |
| regex_dna      | 239 ms                                                                | 250 ms: 1.04x slower                                                    |
| regex_v8       | 29.1 ms                                                               | 30.9 ms: 1.06x slower                                                   |
| regex_effbot   | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 252 us: 1.11x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 190 ms: 1.10x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.59 us: 1.04x faster                                                   |
| pickle_pure_python   | 374 us                                                                | 361 us: 1.04x faster                                                    |
| tomli_loads          | 2.62 sec                                                              | 2.53 sec: 1.03x faster                                                  |
| pickle_dict          | 37.6 us                                                               | 37.3 us: 1.01x faster                                                   |
| pickle_list          | 5.01 us                                                               | 5.24 us: 1.04x slower                                                   |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                                   |
| pickle               | 12.8 us                                                               | 13.6 us: 1.07x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 81.2 ms: 1.07x slower                                                   |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.41 ms: 1.14x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.6 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                                   |
| genshi_text    | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 200 us: 3.27x faster                                                    |
| generators                 | 64.2 ms                                                               | 37.6 ms: 1.71x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 573 ms: 1.61x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.21 sec: 1.45x faster                                                  |
| async_tree_none            | 701 ms                                                                | 490 ms: 1.43x faster                                                    |
| comprehensions             | 29.0 us                                                               | 20.4 us: 1.42x faster                                                   |
| async_tree_memoization_tg  | 828 ms                                                                | 600 ms: 1.38x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 647 ms: 1.35x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.20 sec: 1.34x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 467 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 756 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 784 ms: 1.22x faster                                                    |
| deltablue                  | 4.75 ms                                                               | 3.90 ms: 1.22x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                  |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.40 ms: 1.17x faster                                                   |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.16x faster                                                    |
| pylint                     | 397 ms                                                                | 342 ms: 1.16x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                   |
| richards_super             | 70.2 ms                                                               | 60.4 ms: 1.16x faster                                                   |
| pathlib                    | 24.8 ms                                                               | 21.4 ms: 1.16x faster                                                   |
| chaos                      | 78.8 ms                                                               | 67.9 ms: 1.16x faster                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 1.73 ms: 1.16x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                   |
| unpickle_pure_python       | 278 us                                                                | 252 us: 1.11x faster                                                    |
| sympy_str                  | 295 ms                                                                | 268 ms: 1.10x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 190 ms: 1.10x faster                                                    |
| sympy_integrate            | 23.2 ms                                                               | 21.3 ms: 1.09x faster                                                   |
| richards                   | 58.1 ms                                                               | 53.7 ms: 1.08x faster                                                   |
| tornado_http               | 140 ms                                                                | 130 ms: 1.07x faster                                                    |
| hexiom                     | 7.57 ms                                                               | 7.07 ms: 1.07x faster                                                   |
| bench_thread_pool          | 1.36 ms                                                               | 1.27 ms: 1.07x faster                                                   |
| dulwich_log                | 63.2 ms                                                               | 59.4 ms: 1.06x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.11 us: 1.06x faster                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 7.02 ms: 1.06x faster                                                   |
| logging_format             | 8.22 us                                                               | 7.78 us: 1.06x faster                                                   |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 82.0 ms: 1.05x faster                                                   |
| nqueens                    | 102 ms                                                                | 98.0 ms: 1.05x faster                                                   |
| sympy_expand               | 482 ms                                                                | 461 ms: 1.05x faster                                                    |
| dask                       | 385 ms                                                                | 368 ms: 1.05x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.59 us: 1.04x faster                                                   |
| pickle_pure_python         | 374 us                                                                | 361 us: 1.04x faster                                                    |
| sqlglot_normalize          | 132 ms                                                                | 128 ms: 1.04x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.53 sec: 1.03x faster                                                  |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                    |
| meteor_contest             | 115 ms                                                                | 112 ms: 1.03x faster                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 81.1 ms: 1.03x faster                                                   |
| genshi_xml                 | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                                   |
| scimark_lu                 | 140 ms                                                                | 137 ms: 1.02x faster                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 62.1 ms: 1.02x faster                                                   |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                                    |
| pycparser                  | 1.25 sec                                                              | 1.23 sec: 1.02x faster                                                  |
| mdp                        | 3.35 sec                                                              | 3.32 sec: 1.01x faster                                                  |
| genshi_text                | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                                   |
| pickle_dict                | 37.6 us                                                               | 37.3 us: 1.01x faster                                                   |
| logging_silent             | 133 ns                                                                | 134 ns: 1.01x slower                                                    |
| asyncio_websockets         | 656 ms                                                                | 666 ms: 1.02x slower                                                    |
| fannkuch                   | 451 ms                                                                | 460 ms: 1.02x slower                                                    |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 50.1 us: 1.02x slower                                                   |
| deepcopy                   | 435 us                                                                | 445 us: 1.02x slower                                                    |
| float                      | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 1.91 sec: 1.03x slower                                                  |
| json                       | 5.52 ms                                                               | 5.68 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 930 ms: 1.03x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.02 us: 1.03x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.24 us: 1.04x slower                                                   |
| regex_dna                  | 239 ms                                                                | 250 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.65 ms: 1.06x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                  |
| regex_v8                   | 29.1 ms                                                               | 30.9 ms: 1.06x slower                                                   |
| thrift                     | 910 us                                                                | 967 us: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                                   |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.07x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 81.2 ms: 1.07x slower                                                   |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.07x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.84 us: 1.08x slower                                                   |
| pyflate                    | 516 ms                                                                | 557 ms: 1.08x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                    |
| scimark_sor                | 145 ms                                                                | 159 ms: 1.10x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 9.16 ms: 1.10x slower                                                   |
| scimark_fft                | 402 ms                                                                | 446 ms: 1.11x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.74 ms: 1.13x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 8.41 ms: 1.14x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                                   |
| coverage                   | 84.1 ms                                                               | 97.9 ms: 1.17x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.22 ms: 1.21x slower                                                   |
| python_startup             | 10.2 ms                                                               | 12.6 ms: 1.24x slower                                                   |
| telco                      | 7.80 ms                                                               | 9.85 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.39 ms: 1.28x slower                                                   |
| async_generators           | 378 ms                                                                | 483 ms: 1.28x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                            |

Benchmark hidden because not significant (5): django_template, mako, nbody, html5lib, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.68% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x