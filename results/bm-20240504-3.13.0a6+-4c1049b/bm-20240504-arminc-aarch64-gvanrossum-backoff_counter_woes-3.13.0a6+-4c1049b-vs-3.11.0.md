# Results vs. 3.11.0

- fork: gvanrossum
- ref: backoff_counter_woes
- machine: linux-aarch64
- commit hash: 4c1049b
- commit date: 2024-05-04
- overall geometric mean: 1.05x faster
- HPT reliability: 98.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 303 ms: 1.01x slower                                                         |
| chameleon      | 8.29 ms                                                               | 9.33 ms: 1.13x slower                                                        |
| docutils       | 2.92 sec                                                              | 3.11 sec: 1.06x slower                                                       |
| tornado_http   | 140 ms                                                                | 129 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 489 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 589 ms: 1.41x faster                                                         |
| async_tree_memoization     | 872 ms                                                                | 644 ms: 1.36x faster                                                         |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.33x faster                                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                       |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                       |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 787 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 787 ms: 1.17x faster                                                         |
| Geometric mean             | (ref)                                                                 | 1.31x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.04x faster                                                         |
| nbody          | 113 ms                                                                | 111 ms: 1.02x faster                                                         |
| float          | 89.6 ms                                                               | 91.5 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                                         |
| regex_dna      | 239 ms                                                                | 246 ms: 1.03x slower                                                         |
| regex_v8       | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                        |
| regex_effbot   | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                        |
| unpickle_pure_python | 278 us                                                                | 254 us: 1.10x faster                                                         |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.09x faster                                                         |
| pickle_pure_python   | 374 us                                                                | 355 us: 1.05x faster                                                         |
| unpickle_list        | 6.86 us                                                               | 6.67 us: 1.03x faster                                                        |
| xml_etree_iterparse  | 152 ms                                                                | 150 ms: 1.01x faster                                                         |
| pickle_dict          | 37.6 us                                                               | 37.7 us: 1.00x slower                                                        |
| xml_etree_process    | 76.1 ms                                                               | 79.8 ms: 1.05x slower                                                        |
| pickle               | 12.8 us                                                               | 13.5 us: 1.06x slower                                                        |
| pickle_list          | 5.01 us                                                               | 5.31 us: 1.06x slower                                                        |
| json_loads           | 30.3 us                                                               | 32.6 us: 1.07x slower                                                        |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                                         |
| unpickle             | 16.9 us                                                               | 19.8 us: 1.17x slower                                                        |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.42 ms: 1.15x slower                                                        |
| python_startup         | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                        |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml     | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                                        |
| genshi_text    | 28.2 ms                                                               | 27.7 ms: 1.02x faster                                                        |
| mako           | 13.3 ms                                                               | 13.2 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240504-arminc-aarch64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 202 us: 3.24x faster                                                         |
| generators                 | 64.2 ms                                                               | 38.4 ms: 1.67x faster                                                        |
| asyncio_tcp                | 920 ms                                                                | 562 ms: 1.64x faster                                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.22 sec: 1.44x faster                                                       |
| async_tree_none            | 701 ms                                                                | 489 ms: 1.43x faster                                                         |
| comprehensions             | 29.0 us                                                               | 20.3 us: 1.43x faster                                                        |
| async_tree_memoization_tg  | 828 ms                                                                | 589 ms: 1.41x faster                                                         |
| async_tree_memoization     | 872 ms                                                                | 644 ms: 1.36x faster                                                         |
| async_tree_none_tg         | 620 ms                                                                | 465 ms: 1.33x faster                                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                       |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                       |
| deltablue                  | 4.75 ms                                                               | 3.84 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 787 ms: 1.21x faster                                                         |
| chaos                      | 78.8 ms                                                               | 66.2 ms: 1.19x faster                                                        |
| raytrace                   | 351 ms                                                                | 295 ms: 1.19x faster                                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.39 ms: 1.18x faster                                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 787 ms: 1.17x faster                                                         |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.17x faster                                                         |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                        |
| pylint                     | 397 ms                                                                | 342 ms: 1.16x faster                                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.73 ms: 1.16x faster                                                        |
| richards_super             | 70.2 ms                                                               | 62.2 ms: 1.13x faster                                                        |
| coroutines                 | 33.3 ms                                                               | 29.8 ms: 1.12x faster                                                        |
| sympy_integrate            | 23.2 ms                                                               | 21.1 ms: 1.10x faster                                                        |
| unpickle_pure_python       | 278 us                                                                | 254 us: 1.10x faster                                                         |
| sympy_str                  | 295 ms                                                                | 269 ms: 1.09x faster                                                         |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.09x faster                                                         |
| tornado_http               | 140 ms                                                                | 129 ms: 1.09x faster                                                         |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.07x faster                                                        |
| dulwich_log                | 63.2 ms                                                               | 59.2 ms: 1.07x faster                                                        |
| pathlib                    | 24.8 ms                                                               | 23.3 ms: 1.06x faster                                                        |
| hexiom                     | 7.57 ms                                                               | 7.12 ms: 1.06x faster                                                        |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                                         |
| sympy_expand               | 482 ms                                                                | 457 ms: 1.05x faster                                                         |
| bench_mp_pool              | 7.44 ms                                                               | 7.06 ms: 1.05x faster                                                        |
| pickle_pure_python         | 374 us                                                                | 355 us: 1.05x faster                                                         |
| richards                   | 58.1 ms                                                               | 55.7 ms: 1.04x faster                                                        |
| logging_format             | 8.22 us                                                               | 7.93 us: 1.04x faster                                                        |
| pidigits                   | 242 ms                                                                | 234 ms: 1.04x faster                                                         |
| logging_simple             | 7.57 us                                                               | 7.31 us: 1.04x faster                                                        |
| sqlglot_normalize          | 132 ms                                                                | 128 ms: 1.03x faster                                                         |
| nqueens                    | 102 ms                                                                | 99.2 ms: 1.03x faster                                                        |
| dask                       | 385 ms                                                                | 373 ms: 1.03x faster                                                         |
| unpickle_list              | 6.86 us                                                               | 6.67 us: 1.03x faster                                                        |
| genshi_xml                 | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                                        |
| crypto_pyaes               | 86.5 ms                                                               | 84.3 ms: 1.03x faster                                                        |
| scimark_monte_carlo        | 83.2 ms                                                               | 81.3 ms: 1.02x faster                                                        |
| go                         | 163 ms                                                                | 159 ms: 1.02x faster                                                         |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                                         |
| pycparser                  | 1.25 sec                                                              | 1.22 sec: 1.02x faster                                                       |
| sqlglot_optimize           | 63.4 ms                                                               | 62.2 ms: 1.02x faster                                                        |
| genshi_text                | 28.2 ms                                                               | 27.7 ms: 1.02x faster                                                        |
| nbody                      | 113 ms                                                                | 111 ms: 1.02x faster                                                         |
| mdp                        | 3.35 sec                                                              | 3.31 sec: 1.01x faster                                                       |
| xml_etree_iterparse        | 152 ms                                                                | 150 ms: 1.01x faster                                                         |
| scimark_lu                 | 140 ms                                                                | 139 ms: 1.00x faster                                                         |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.00x faster                                                        |
| pickle_dict                | 37.6 us                                                               | 37.7 us: 1.00x slower                                                        |
| asyncio_websockets         | 656 ms                                                                | 659 ms: 1.01x slower                                                         |
| 2to3                       | 300 ms                                                                | 303 ms: 1.01x slower                                                         |
| logging_silent             | 133 ns                                                                | 135 ns: 1.02x slower                                                         |
| float                      | 89.6 ms                                                               | 91.5 ms: 1.02x slower                                                        |
| deepcopy_memo              | 49.0 us                                                               | 50.1 us: 1.02x slower                                                        |
| fannkuch                   | 451 ms                                                                | 464 ms: 1.03x slower                                                         |
| regex_dna                  | 239 ms                                                                | 246 ms: 1.03x slower                                                         |
| gunicorn                   | 1.19 ms                                                               | 1.22 ms: 1.03x slower                                                        |
| deepcopy                   | 435 us                                                                | 449 us: 1.03x slower                                                         |
| pprint_pformat             | 1.85 sec                                                              | 1.92 sec: 1.03x slower                                                       |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.52 ms: 1.04x slower                                                        |
| thrift                     | 910 us                                                                | 945 us: 1.04x slower                                                         |
| pprint_safe_repr           | 903 ms                                                                | 939 ms: 1.04x slower                                                         |
| aiohttp                    | 1.13 ms                                                               | 1.18 ms: 1.04x slower                                                        |
| xml_etree_process          | 76.1 ms                                                               | 79.8 ms: 1.05x slower                                                        |
| deepcopy_reduce            | 3.89 us                                                               | 4.08 us: 1.05x slower                                                        |
| spectral_norm              | 131 ms                                                                | 138 ms: 1.05x slower                                                         |
| json                       | 5.52 ms                                                               | 5.83 ms: 1.06x slower                                                        |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.06x slower                                                        |
| pickle_list                | 5.01 us                                                               | 5.31 us: 1.06x slower                                                        |
| docutils                   | 2.92 sec                                                              | 3.11 sec: 1.06x slower                                                       |
| regex_v8                   | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                        |
| json_loads                 | 30.3 us                                                               | 32.6 us: 1.07x slower                                                        |
| pyflate                    | 516 ms                                                                | 559 ms: 1.08x slower                                                         |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                         |
| scimark_sor                | 145 ms                                                                | 159 ms: 1.10x slower                                                         |
| sqlite_synth               | 3.56 us                                                               | 3.91 us: 1.10x slower                                                        |
| scimark_fft                | 402 ms                                                                | 443 ms: 1.10x slower                                                         |
| chameleon                  | 8.29 ms                                                               | 9.33 ms: 1.13x slower                                                        |
| regex_effbot               | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                        |
| python_startup_no_site     | 7.35 ms                                                               | 8.42 ms: 1.15x slower                                                        |
| flaskblogging              | 4.19 ms                                                               | 4.83 ms: 1.15x slower                                                        |
| unpickle                   | 16.9 us                                                               | 19.8 us: 1.17x slower                                                        |
| gc_traversal               | 4.33 ms                                                               | 5.09 ms: 1.18x slower                                                        |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                         |
| python_startup             | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                        |
| telco                      | 7.80 ms                                                               | 9.78 ms: 1.25x slower                                                        |
| async_generators           | 378 ms                                                                | 484 ms: 1.28x slower                                                         |
| create_gc_cycles           | 1.87 ms                                                               | 2.45 ms: 1.31x slower                                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                                 |

Benchmark hidden because not significant (3): tomli_loads, django_template, html5lib
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x