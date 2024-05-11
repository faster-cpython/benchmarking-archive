# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: linux-aarch64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.05x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| chameleon      | 8.29 ms                                                               | 8.86 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                 |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 573 ms: 1.22x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 737 ms: 1.18x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 731 ms: 1.13x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.44 sec: 1.12x faster                                       |
| async_tree_io_tg           | 1.54 sec                                                              | 1.43 sec: 1.08x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 577 ms: 1.07x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 893 ms: 1.07x faster                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 890 ms: 1.04x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.11x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 103 ms: 1.09x faster                                         |
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| float          | 89.6 ms                                                               | 93.1 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 126 ms: 1.08x faster                                         |
| regex_v8       | 29.1 ms                                                               | 30.4 ms: 1.05x slower                                        |
| regex_dna      | 239 ms                                                                | 251 ms: 1.05x slower                                         |
| regex_effbot   | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                        |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.8 ms: 1.21x faster                                        |
| unpickle_list        | 6.86 us                                                               | 6.25 us: 1.10x faster                                        |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.09x faster                                         |
| unpickle_pure_python | 278 us                                                                | 256 us: 1.09x faster                                         |
| pickle_pure_python   | 374 us                                                                | 349 us: 1.07x faster                                         |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                       |
| pickle               | 12.8 us                                                               | 13.3 us: 1.04x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.26 us: 1.05x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 80.4 ms: 1.06x slower                                        |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 118 ms: 1.14x slower                                         |
| unpickle             | 16.9 us                                                               | 19.3 us: 1.15x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 12.2 ms: 1.20x slower                                        |
| python_startup_no_site | 7.35 ms                                                               | 10.5 ms: 1.43x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.31x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 40.5 ms: 1.03x faster                                        |
| genshi_xml      | 62.2 ms                                                               | 60.5 ms: 1.03x faster                                        |
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                        |
| genshi_text     | 28.2 ms                                                               | 27.8 ms: 1.01x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240312-arminc-aarch64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 133 us: 4.90x faster                                         |
| generators                 | 64.2 ms                                                               | 35.9 ms: 1.79x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 559 ms: 1.65x faster                                         |
| comprehensions             | 29.0 us                                                               | 19.9 us: 1.46x faster                                        |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.22 sec: 1.44x faster                                       |
| async_tree_none            | 701 ms                                                                | 573 ms: 1.22x faster                                         |
| json_dumps                 | 15.4 ms                                                               | 12.8 ms: 1.21x faster                                        |
| sympy_sum                  | 168 ms                                                                | 140 ms: 1.20x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.37 ms: 1.20x faster                                        |
| richards_super             | 70.2 ms                                                               | 59.1 ms: 1.19x faster                                        |
| deltablue                  | 4.75 ms                                                               | 4.00 ms: 1.19x faster                                        |
| pylint                     | 397 ms                                                                | 335 ms: 1.19x faster                                         |
| raytrace                   | 351 ms                                                                | 296 ms: 1.18x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 737 ms: 1.18x faster                                         |
| chaos                      | 78.8 ms                                                               | 67.6 ms: 1.17x faster                                        |
| coroutines                 | 33.3 ms                                                               | 28.8 ms: 1.16x faster                                        |
| sqlglot_transpile          | 2.00 ms                                                               | 1.75 ms: 1.14x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 20.4 ms: 1.13x faster                                        |
| async_tree_memoization_tg  | 828 ms                                                                | 731 ms: 1.13x faster                                         |
| sympy_str                  | 295 ms                                                                | 260 ms: 1.13x faster                                         |
| richards                   | 58.1 ms                                                               | 51.8 ms: 1.12x faster                                        |
| async_tree_io              | 1.61 sec                                                              | 1.44 sec: 1.12x faster                                       |
| unpickle_list              | 6.86 us                                                               | 6.25 us: 1.10x faster                                        |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.09x faster                                         |
| hexiom                     | 7.57 ms                                                               | 6.92 ms: 1.09x faster                                        |
| crypto_pyaes               | 86.5 ms                                                               | 79.2 ms: 1.09x faster                                        |
| nbody                      | 113 ms                                                                | 103 ms: 1.09x faster                                         |
| unpickle_pure_python       | 278 us                                                                | 256 us: 1.09x faster                                         |
| regex_compile              | 137 ms                                                                | 126 ms: 1.08x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.43 sec: 1.08x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 577 ms: 1.07x faster                                         |
| pickle_pure_python         | 374 us                                                                | 349 us: 1.07x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 893 ms: 1.07x faster                                         |
| sympy_expand               | 482 ms                                                                | 451 ms: 1.07x faster                                         |
| nqueens                    | 102 ms                                                                | 96.0 ms: 1.07x faster                                        |
| bench_mp_pool              | 7.44 ms                                                               | 7.02 ms: 1.06x faster                                        |
| dulwich_log                | 63.2 ms                                                               | 59.7 ms: 1.06x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.18 us: 1.05x faster                                        |
| sqlglot_normalize          | 132 ms                                                                | 126 ms: 1.05x faster                                         |
| bench_thread_pool          | 1.36 ms                                                               | 1.29 ms: 1.05x faster                                        |
| logging_format             | 8.22 us                                                               | 7.83 us: 1.05x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 890 ms: 1.04x faster                                         |
| sqlglot_optimize           | 63.4 ms                                                               | 61.2 ms: 1.04x faster                                        |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| django_template            | 41.8 ms                                                               | 40.5 ms: 1.03x faster                                        |
| genshi_xml                 | 62.2 ms                                                               | 60.5 ms: 1.03x faster                                        |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                        |
| pathlib                    | 24.8 ms                                                               | 24.2 ms: 1.03x faster                                        |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| scimark_lu                 | 140 ms                                                                | 137 ms: 1.02x faster                                         |
| logging_silent             | 133 ns                                                                | 130 ns: 1.02x faster                                         |
| deepcopy_memo              | 49.0 us                                                               | 48.2 us: 1.02x faster                                        |
| genshi_text                | 28.2 ms                                                               | 27.8 ms: 1.01x faster                                        |
| scimark_monte_carlo        | 83.2 ms                                                               | 82.1 ms: 1.01x faster                                        |
| deepcopy                   | 435 us                                                                | 431 us: 1.01x faster                                         |
| go                         | 163 ms                                                                | 161 ms: 1.01x faster                                         |
| tomli_loads                | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                       |
| mdp                        | 3.35 sec                                                              | 3.32 sec: 1.01x faster                                       |
| asyncio_websockets         | 656 ms                                                                | 664 ms: 1.01x slower                                         |
| fannkuch                   | 451 ms                                                                | 459 ms: 1.02x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 3.95 us: 1.02x slower                                        |
| thrift                     | 910 us                                                                | 929 us: 1.02x slower                                         |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                         |
| pycparser                  | 1.25 sec                                                              | 1.28 sec: 1.03x slower                                       |
| gc_traversal               | 4.33 ms                                                               | 4.45 ms: 1.03x slower                                        |
| spectral_norm              | 131 ms                                                                | 135 ms: 1.03x slower                                         |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.51 ms: 1.04x slower                                        |
| gunicorn                   | 1.19 ms                                                               | 1.23 ms: 1.04x slower                                        |
| pickle                     | 12.8 us                                                               | 13.3 us: 1.04x slower                                        |
| aiohttp                    | 1.13 ms                                                               | 1.18 ms: 1.04x slower                                        |
| float                      | 89.6 ms                                                               | 93.1 ms: 1.04x slower                                        |
| regex_v8                   | 29.1 ms                                                               | 30.4 ms: 1.05x slower                                        |
| regex_dna                  | 239 ms                                                                | 251 ms: 1.05x slower                                         |
| pickle_list                | 5.01 us                                                               | 5.26 us: 1.05x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 80.4 ms: 1.06x slower                                        |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                        |
| create_gc_cycles           | 1.87 ms                                                               | 1.99 ms: 1.06x slower                                        |
| chameleon                  | 8.29 ms                                                               | 8.86 ms: 1.07x slower                                        |
| sqlite_synth               | 3.56 us                                                               | 3.88 us: 1.09x slower                                        |
| scimark_fft                | 402 ms                                                                | 441 ms: 1.10x slower                                         |
| flaskblogging              | 4.19 ms                                                               | 4.74 ms: 1.13x slower                                        |
| scimark_sor                | 145 ms                                                                | 165 ms: 1.13x slower                                         |
| xml_etree_generate         | 104 ms                                                                | 118 ms: 1.14x slower                                         |
| pyflate                    | 516 ms                                                                | 591 ms: 1.15x slower                                         |
| unpickle                   | 16.9 us                                                               | 19.3 us: 1.15x slower                                        |
| regex_effbot               | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                        |
| python_startup             | 10.2 ms                                                               | 12.2 ms: 1.20x slower                                        |
| coverage                   | 84.1 ms                                                               | 102 ms: 1.21x slower                                         |
| mypy2                      | 737 ms                                                                | 917 ms: 1.25x slower                                         |
| async_generators           | 378 ms                                                                | 487 ms: 1.29x slower                                         |
| telco                      | 7.80 ms                                                               | 10.2 ms: 1.31x slower                                        |
| python_startup_no_site     | 7.35 ms                                                               | 10.5 ms: 1.43x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (8): tornado_http, dask, docutils, pprint_safe_repr, pickle_dict, pprint_pformat, meteor_contest, html5lib
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x