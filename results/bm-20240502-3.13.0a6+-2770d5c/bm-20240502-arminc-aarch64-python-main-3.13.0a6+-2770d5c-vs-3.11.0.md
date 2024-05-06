# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: 2770d5c
- commit date: 2024-05-02
- overall geometric mean: 1.07x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 298 ms: 1.01x faster                                     |
| chameleon      | 8.29 ms                                                               | 9.06 ms: 1.09x slower                                    |
| docutils       | 2.92 sec                                                              | 3.06 sec: 1.05x slower                                   |
| tornado_http   | 140 ms                                                                | 126 ms: 1.11x faster                                     |
| Geometric mean | (ref)                                                                 | 1.01x slower                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 486 ms: 1.44x faster                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 590 ms: 1.40x faster                                     |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                     |
| async_tree_none_tg         | 620 ms                                                                | 462 ms: 1.34x faster                                     |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.19 sec: 1.29x faster                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 783 ms: 1.22x faster                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 769 ms: 1.20x faster                                     |
| Geometric mean             | (ref)                                                                 | 1.32x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 113 ms                                                                | 106 ms: 1.07x faster                                     |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                     |
| float          | 89.6 ms                                                               | 88.7 ms: 1.01x faster                                    |
| Geometric mean | (ref)                                                                 | 1.04x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 127 ms: 1.08x faster                                     |
| regex_dna      | 239 ms                                                                | 248 ms: 1.04x slower                                     |
| regex_v8       | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                    |
| regex_effbot   | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                    |
| Geometric mean | (ref)                                                                 | 1.04x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.8 ms: 1.20x faster                                    |
| xml_etree_parse      | 209 ms                                                                | 186 ms: 1.13x faster                                     |
| unpickle_pure_python | 278 us                                                                | 248 us: 1.12x faster                                     |
| unpickle_list        | 6.86 us                                                               | 6.25 us: 1.10x faster                                    |
| pickle_pure_python   | 374 us                                                                | 350 us: 1.07x faster                                     |
| tomli_loads          | 2.62 sec                                                              | 2.49 sec: 1.05x faster                                   |
| xml_etree_iterparse  | 152 ms                                                                | 146 ms: 1.04x faster                                     |
| pickle_dict          | 37.6 us                                                               | 37.9 us: 1.01x slower                                    |
| pickle               | 12.8 us                                                               | 13.3 us: 1.04x slower                                    |
| xml_etree_process    | 76.1 ms                                                               | 79.4 ms: 1.04x slower                                    |
| json_loads           | 30.3 us                                                               | 31.9 us: 1.05x slower                                    |
| pickle_list          | 5.01 us                                                               | 5.29 us: 1.05x slower                                    |
| xml_etree_generate   | 104 ms                                                                | 111 ms: 1.06x slower                                     |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.17x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.29 ms: 1.13x slower                                    |
| python_startup         | 10.2 ms                                                               | 12.1 ms: 1.19x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.16x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 62.2 ms                                                               | 59.8 ms: 1.04x faster                                    |
| genshi_text     | 28.2 ms                                                               | 27.3 ms: 1.03x faster                                    |
| django_template | 41.8 ms                                                               | 40.5 ms: 1.03x faster                                    |
| mako            | 13.3 ms                                                               | 13.1 ms: 1.01x faster                                    |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 191 us: 3.42x faster                                     |
| asyncio_tcp                | 920 ms                                                                | 530 ms: 1.74x faster                                     |
| generators                 | 64.2 ms                                                               | 37.2 ms: 1.73x faster                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.12 sec: 1.50x faster                                   |
| comprehensions             | 29.0 us                                                               | 19.9 us: 1.45x faster                                    |
| async_tree_none            | 701 ms                                                                | 486 ms: 1.44x faster                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 590 ms: 1.40x faster                                     |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                     |
| async_tree_none_tg         | 620 ms                                                                | 462 ms: 1.34x faster                                     |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.19 sec: 1.29x faster                                   |
| deltablue                  | 4.75 ms                                                               | 3.80 ms: 1.25x faster                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 783 ms: 1.22x faster                                     |
| raytrace                   | 351 ms                                                                | 291 ms: 1.21x faster                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.37 ms: 1.20x faster                                    |
| json_dumps                 | 15.4 ms                                                               | 12.8 ms: 1.20x faster                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 769 ms: 1.20x faster                                     |
| sqlglot_transpile          | 2.00 ms                                                               | 1.68 ms: 1.19x faster                                    |
| chaos                      | 78.8 ms                                                               | 66.5 ms: 1.19x faster                                    |
| pylint                     | 397 ms                                                                | 336 ms: 1.18x faster                                     |
| richards_super             | 70.2 ms                                                               | 59.4 ms: 1.18x faster                                    |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.17x faster                                     |
| coroutines                 | 33.3 ms                                                               | 28.7 ms: 1.16x faster                                    |
| xml_etree_parse            | 209 ms                                                                | 186 ms: 1.13x faster                                     |
| unpickle_pure_python       | 278 us                                                                | 248 us: 1.12x faster                                     |
| sympy_str                  | 295 ms                                                                | 264 ms: 1.12x faster                                     |
| sympy_integrate            | 23.2 ms                                                               | 20.8 ms: 1.12x faster                                    |
| dulwich_log                | 63.2 ms                                                               | 56.7 ms: 1.11x faster                                    |
| tornado_http               | 140 ms                                                                | 126 ms: 1.11x faster                                     |
| richards                   | 58.1 ms                                                               | 52.8 ms: 1.10x faster                                    |
| unpickle_list              | 6.86 us                                                               | 6.25 us: 1.10x faster                                    |
| logging_format             | 8.22 us                                                               | 7.56 us: 1.09x faster                                    |
| pathlib                    | 24.8 ms                                                               | 22.8 ms: 1.09x faster                                    |
| logging_simple             | 7.57 us                                                               | 6.97 us: 1.09x faster                                    |
| regex_compile              | 137 ms                                                                | 127 ms: 1.08x faster                                     |
| hexiom                     | 7.57 ms                                                               | 7.01 ms: 1.08x faster                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.08x faster                                    |
| nqueens                    | 102 ms                                                                | 95.7 ms: 1.07x faster                                    |
| bench_mp_pool              | 7.44 ms                                                               | 6.95 ms: 1.07x faster                                    |
| pickle_pure_python         | 374 us                                                                | 350 us: 1.07x faster                                     |
| sympy_expand               | 482 ms                                                                | 451 ms: 1.07x faster                                     |
| nbody                      | 113 ms                                                                | 106 ms: 1.07x faster                                     |
| sqlglot_normalize          | 132 ms                                                                | 125 ms: 1.06x faster                                     |
| crypto_pyaes               | 86.5 ms                                                               | 82.2 ms: 1.05x faster                                    |
| tomli_loads                | 2.62 sec                                                              | 2.49 sec: 1.05x faster                                   |
| scimark_lu                 | 140 ms                                                                | 134 ms: 1.04x faster                                     |
| genshi_xml                 | 62.2 ms                                                               | 59.8 ms: 1.04x faster                                    |
| xml_etree_iterparse        | 152 ms                                                                | 146 ms: 1.04x faster                                     |
| sqlglot_optimize           | 63.4 ms                                                               | 61.0 ms: 1.04x faster                                    |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                     |
| dask                       | 385 ms                                                                | 372 ms: 1.04x faster                                     |
| genshi_text                | 28.2 ms                                                               | 27.3 ms: 1.03x faster                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 80.6 ms: 1.03x faster                                    |
| django_template            | 41.8 ms                                                               | 40.5 ms: 1.03x faster                                    |
| pycparser                  | 1.25 sec                                                              | 1.21 sec: 1.03x faster                                   |
| go                         | 163 ms                                                                | 159 ms: 1.02x faster                                     |
| mdp                        | 3.35 sec                                                              | 3.29 sec: 1.02x faster                                   |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                     |
| mako                       | 13.3 ms                                                               | 13.1 ms: 1.01x faster                                    |
| float                      | 89.6 ms                                                               | 88.7 ms: 1.01x faster                                    |
| logging_silent             | 133 ns                                                                | 131 ns: 1.01x faster                                     |
| deepcopy_memo              | 49.0 us                                                               | 48.6 us: 1.01x faster                                    |
| 2to3                       | 300 ms                                                                | 298 ms: 1.01x faster                                     |
| fannkuch                   | 451 ms                                                                | 453 ms: 1.00x slower                                     |
| pickle_dict                | 37.6 us                                                               | 37.9 us: 1.01x slower                                    |
| json                       | 5.52 ms                                                               | 5.59 ms: 1.01x slower                                    |
| deepcopy                   | 435 us                                                                | 442 us: 1.01x slower                                     |
| pprint_pformat             | 1.85 sec                                                              | 1.89 sec: 1.02x slower                                   |
| pprint_safe_repr           | 903 ms                                                                | 923 ms: 1.02x slower                                     |
| thrift                     | 910 us                                                                | 936 us: 1.03x slower                                     |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.47 ms: 1.03x slower                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.00 us: 1.03x slower                                    |
| regex_dna                  | 239 ms                                                                | 248 ms: 1.04x slower                                     |
| pickle                     | 12.8 us                                                               | 13.3 us: 1.04x slower                                    |
| xml_etree_process          | 76.1 ms                                                               | 79.4 ms: 1.04x slower                                    |
| docutils                   | 2.92 sec                                                              | 3.06 sec: 1.05x slower                                   |
| json_loads                 | 30.3 us                                                               | 31.9 us: 1.05x slower                                    |
| pickle_list                | 5.01 us                                                               | 5.29 us: 1.05x slower                                    |
| spectral_norm              | 131 ms                                                                | 139 ms: 1.06x slower                                     |
| sqlite_synth               | 3.56 us                                                               | 3.78 us: 1.06x slower                                    |
| xml_etree_generate         | 104 ms                                                                | 111 ms: 1.06x slower                                     |
| scimark_sor                | 145 ms                                                                | 155 ms: 1.06x slower                                     |
| regex_v8                   | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                    |
| pyflate                    | 516 ms                                                                | 555 ms: 1.08x slower                                     |
| scimark_fft                | 402 ms                                                                | 438 ms: 1.09x slower                                     |
| chameleon                  | 8.29 ms                                                               | 9.06 ms: 1.09x slower                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.29 ms: 1.13x slower                                    |
| regex_effbot               | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                    |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.17x slower                                    |
| coverage                   | 84.1 ms                                                               | 98.4 ms: 1.17x slower                                    |
| gc_traversal               | 4.33 ms                                                               | 5.10 ms: 1.18x slower                                    |
| python_startup             | 10.2 ms                                                               | 12.1 ms: 1.19x slower                                    |
| telco                      | 7.80 ms                                                               | 9.38 ms: 1.20x slower                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.31 ms: 1.23x slower                                    |
| async_generators           | 378 ms                                                                | 476 ms: 1.26x slower                                     |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                             |

Benchmark hidden because not significant (2): asyncio_websockets, html5lib
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x