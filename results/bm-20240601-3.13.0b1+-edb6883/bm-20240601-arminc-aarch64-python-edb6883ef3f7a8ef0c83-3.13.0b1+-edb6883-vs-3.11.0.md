# Results vs. 3.11.0

- fork: python
- ref: edb6883ef3f7a8ef0c83
- machine: linux-aarch64
- commit hash: edb6883
- commit date: 2024-06-01
- overall geometric mean: 1.04x faster
- HPT reliability: 98.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                                     |
| chameleon      | 8.29 ms                                                               | 8.93 ms: 1.08x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.13 sec: 1.07x slower                                                   |
| html5lib       | 65.3 ms                                                               | 66.9 ms: 1.03x slower                                                    |
| tornado_http   | 140 ms                                                                | 131 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 492 ms: 1.42x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 599 ms: 1.38x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.20 sec: 1.34x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 479 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 783 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 758 ms: 1.22x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                   |
| Geometric mean             | (ref)                                                                 | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 111 ms: 1.01x faster                                                     |
| float          | 89.6 ms                                                               | 92.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 128 ms: 1.06x faster                                                     |
| regex_v8       | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                                    |
| regex_dna      | 239 ms                                                                | 257 ms: 1.07x slower                                                     |
| regex_effbot   | 4.25 ms                                                               | 4.96 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                                    |
| unpickle_pure_python | 278 us                                                                | 251 us: 1.11x faster                                                     |
| xml_etree_parse      | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.56 us: 1.05x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 359 us: 1.04x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| pickle_list          | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| pickle               | 12.8 us                                                               | 13.8 us: 1.08x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.6 us: 1.08x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 82.2 ms: 1.08x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 116 ms: 1.12x slower                                                     |
| unpickle             | 16.9 us                                                               | 20.0 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.61 ms: 1.17x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.1 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 28.2 ms                                                               | 27.6 ms: 1.02x faster                                                    |
| mako           | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240601-arminc-aarch64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 197 us: 3.31x faster                                                     |
| generators                 | 64.2 ms                                                               | 37.6 ms: 1.71x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 585 ms: 1.57x faster                                                     |
| comprehensions             | 29.0 us                                                               | 20.2 us: 1.43x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.23 sec: 1.43x faster                                                   |
| async_tree_none            | 701 ms                                                                | 492 ms: 1.42x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 599 ms: 1.38x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 642 ms: 1.36x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.20 sec: 1.34x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 479 ms: 1.30x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 3.82 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 783 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 758 ms: 1.22x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.21x faster                                                   |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                                     |
| pylint                     | 397 ms                                                                | 339 ms: 1.17x faster                                                     |
| chaos                      | 78.8 ms                                                               | 68.0 ms: 1.16x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.72 ms: 1.16x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.4 ms: 1.15x faster                                                    |
| sympy_sum                  | 168 ms                                                                | 146 ms: 1.15x faster                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.43 ms: 1.15x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                    |
| richards_super             | 70.2 ms                                                               | 61.9 ms: 1.13x faster                                                    |
| unpickle_pure_python       | 278 us                                                                | 251 us: 1.11x faster                                                     |
| sympy_str                  | 295 ms                                                                | 268 ms: 1.10x faster                                                     |
| sympy_integrate            | 23.2 ms                                                               | 21.2 ms: 1.09x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| hexiom                     | 7.57 ms                                                               | 7.03 ms: 1.08x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 23.1 ms: 1.07x faster                                                    |
| tornado_http               | 140 ms                                                                | 131 ms: 1.07x faster                                                     |
| logging_simple             | 7.57 us                                                               | 7.10 us: 1.07x faster                                                    |
| regex_compile              | 137 ms                                                                | 128 ms: 1.06x faster                                                     |
| bench_thread_pool          | 1.36 ms                                                               | 1.27 ms: 1.06x faster                                                    |
| logging_format             | 8.22 us                                                               | 7.76 us: 1.06x faster                                                    |
| dulwich_log                | 63.2 ms                                                               | 59.8 ms: 1.06x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 82.1 ms: 1.05x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.56 us: 1.05x faster                                                    |
| sympy_expand               | 482 ms                                                                | 461 ms: 1.04x faster                                                     |
| richards                   | 58.1 ms                                                               | 55.6 ms: 1.04x faster                                                    |
| pickle_pure_python         | 374 us                                                                | 359 us: 1.04x faster                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 7.16 ms: 1.04x faster                                                    |
| dask                       | 385 ms                                                                | 373 ms: 1.03x faster                                                     |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| nqueens                    | 102 ms                                                                | 99.4 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 132 ms                                                                | 128 ms: 1.03x faster                                                     |
| tomli_loads                | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| genshi_text                | 28.2 ms                                                               | 27.6 ms: 1.02x faster                                                    |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                                     |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| pycparser                  | 1.25 sec                                                              | 1.23 sec: 1.02x faster                                                   |
| nbody                      | 113 ms                                                                | 111 ms: 1.01x faster                                                     |
| mdp                        | 3.35 sec                                                              | 3.31 sec: 1.01x faster                                                   |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                                    |
| scimark_lu                 | 140 ms                                                                | 142 ms: 1.01x slower                                                     |
| fannkuch                   | 451 ms                                                                | 457 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.85 sec                                                              | 1.89 sec: 1.02x slower                                                   |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                                     |
| html5lib                   | 65.3 ms                                                               | 66.9 ms: 1.03x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 928 ms: 1.03x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 50.4 us: 1.03x slower                                                    |
| float                      | 89.6 ms                                                               | 92.1 ms: 1.03x slower                                                    |
| deepcopy                   | 435 us                                                                | 448 us: 1.03x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                                    |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.52 ms: 1.04x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.19 ms: 1.05x slower                                                    |
| gunicorn                   | 1.19 ms                                                               | 1.24 ms: 1.05x slower                                                    |
| mypy2                      | 737 ms                                                                | 772 ms: 1.05x slower                                                     |
| thrift                     | 910 us                                                                | 958 us: 1.05x slower                                                     |
| pickle_list                | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| spectral_norm              | 131 ms                                                                | 140 ms: 1.07x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.16 us: 1.07x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.13 sec: 1.07x slower                                                   |
| regex_dna                  | 239 ms                                                                | 257 ms: 1.07x slower                                                     |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 8.93 ms: 1.08x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.6 us: 1.08x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 82.2 ms: 1.08x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.90 us: 1.10x slower                                                    |
| scimark_sor                | 145 ms                                                                | 160 ms: 1.10x slower                                                     |
| scimark_fft                | 402 ms                                                                | 445 ms: 1.11x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 116 ms: 1.12x slower                                                     |
| pyflate                    | 516 ms                                                                | 581 ms: 1.13x slower                                                     |
| regex_effbot               | 4.25 ms                                                               | 4.96 ms: 1.17x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.90 ms: 1.17x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.61 ms: 1.17x slower                                                    |
| coverage                   | 84.1 ms                                                               | 98.6 ms: 1.17x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.08 ms: 1.17x slower                                                    |
| unpickle                   | 16.9 us                                                               | 20.0 us: 1.18x slower                                                    |
| telco                      | 7.80 ms                                                               | 9.73 ms: 1.25x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.35 ms: 1.25x slower                                                    |
| async_generators           | 378 ms                                                                | 483 ms: 1.28x slower                                                     |
| python_startup             | 10.2 ms                                                               | 13.1 ms: 1.28x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                             |

Benchmark hidden because not significant (8): meteor_contest, sqlglot_optimize, scimark_monte_carlo, asyncio_websockets, logging_silent, django_template, genshi_xml, pickle_dict
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.84% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x