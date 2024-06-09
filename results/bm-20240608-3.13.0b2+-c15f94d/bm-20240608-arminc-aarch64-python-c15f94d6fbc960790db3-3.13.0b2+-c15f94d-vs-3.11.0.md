# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-aarch64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.05x faster
- HPT reliability: 99.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 306 ms: 1.02x slower                                                     |
| chameleon      | 8.29 ms                                                               | 8.94 ms: 1.08x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                   |
| tornado_http   | 140 ms                                                                | 126 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 490 ms: 1.43x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.32x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 761 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.28 sec: 1.20x faster                                                   |
| Geometric mean             | (ref)                                                                 | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| float          | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| regex_dna      | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 30.5 ms: 1.05x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.5 ms: 1.14x faster                                                    |
| unpickle_pure_python | 278 us                                                                | 253 us: 1.10x faster                                                     |
| xml_etree_parse      | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.47 us: 1.06x faster                                                    |
| tomli_loads          | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 148 ms: 1.02x faster                                                     |
| pickle_pure_python   | 374 us                                                                | 368 us: 1.02x faster                                                     |
| pickle_dict          | 37.6 us                                                               | 38.0 us: 1.01x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.0 us: 1.05x slower                                                    |
| pickle               | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| pickle_list          | 5.01 us                                                               | 5.35 us: 1.07x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 81.7 ms: 1.07x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 117 ms: 1.12x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.71 ms: 1.19x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 28.2 ms                                                               | 27.6 ms: 1.02x faster                                                    |
| django_template | 41.8 ms                                                               | 42.7 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                             |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 192 us: 3.40x faster                                                     |
| generators                 | 64.2 ms                                                               | 37.4 ms: 1.72x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 586 ms: 1.57x faster                                                     |
| comprehensions             | 29.0 us                                                               | 20.1 us: 1.44x faster                                                    |
| async_tree_none            | 701 ms                                                                | 490 ms: 1.43x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.24 sec: 1.42x faster                                                   |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.21 sec: 1.32x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 474 ms: 1.31x faster                                                     |
| deltablue                  | 4.75 ms                                                               | 3.85 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 761 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 792 ms: 1.21x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.28 sec: 1.20x faster                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.40 ms: 1.18x faster                                                    |
| pylint                     | 397 ms                                                                | 338 ms: 1.17x faster                                                     |
| raytrace                   | 351 ms                                                                | 299 ms: 1.17x faster                                                     |
| sympy_sum                  | 168 ms                                                                | 143 ms: 1.17x faster                                                     |
| chaos                      | 78.8 ms                                                               | 67.8 ms: 1.16x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.75 ms: 1.14x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.5 ms: 1.14x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                                    |
| richards_super             | 70.2 ms                                                               | 62.2 ms: 1.13x faster                                                    |
| tornado_http               | 140 ms                                                                | 126 ms: 1.11x faster                                                     |
| sympy_integrate            | 23.2 ms                                                               | 21.0 ms: 1.10x faster                                                    |
| sympy_str                  | 295 ms                                                                | 268 ms: 1.10x faster                                                     |
| unpickle_pure_python       | 278 us                                                                | 253 us: 1.10x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 22.6 ms: 1.10x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 194 ms: 1.08x faster                                                     |
| hexiom                     | 7.57 ms                                                               | 7.06 ms: 1.07x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.06 us: 1.07x faster                                                    |
| logging_format             | 8.22 us                                                               | 7.75 us: 1.06x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.47 us: 1.06x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 81.6 ms: 1.06x faster                                                    |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                                     |
| bench_thread_pool          | 1.36 ms                                                               | 1.28 ms: 1.06x faster                                                    |
| richards                   | 58.1 ms                                                               | 55.4 ms: 1.05x faster                                                    |
| sympy_expand               | 482 ms                                                                | 462 ms: 1.04x faster                                                     |
| sqlglot_normalize          | 132 ms                                                                | 127 ms: 1.04x faster                                                     |
| dulwich_log                | 63.2 ms                                                               | 61.0 ms: 1.04x faster                                                    |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                     |
| dask                       | 385 ms                                                                | 373 ms: 1.03x faster                                                     |
| tomli_loads                | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 7.22 ms: 1.03x faster                                                    |
| nqueens                    | 102 ms                                                                | 99.7 ms: 1.03x faster                                                    |
| pycparser                  | 1.25 sec                                                              | 1.21 sec: 1.03x faster                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 148 ms: 1.02x faster                                                     |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                                     |
| sqlglot_optimize           | 63.4 ms                                                               | 62.0 ms: 1.02x faster                                                    |
| genshi_text                | 28.2 ms                                                               | 27.6 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 81.6 ms: 1.02x faster                                                    |
| pickle_pure_python         | 374 us                                                                | 368 us: 1.02x faster                                                     |
| go                         | 163 ms                                                                | 161 ms: 1.01x faster                                                     |
| mdp                        | 3.35 sec                                                              | 3.31 sec: 1.01x faster                                                   |
| fannkuch                   | 451 ms                                                                | 447 ms: 1.01x faster                                                     |
| scimark_lu                 | 140 ms                                                                | 141 ms: 1.01x slower                                                     |
| pickle_dict                | 37.6 us                                                               | 38.0 us: 1.01x slower                                                    |
| 2to3                       | 300 ms                                                                | 306 ms: 1.02x slower                                                     |
| json                       | 5.52 ms                                                               | 5.64 ms: 1.02x slower                                                    |
| django_template            | 41.8 ms                                                               | 42.7 ms: 1.02x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 50.1 us: 1.02x slower                                                    |
| float                      | 89.6 ms                                                               | 91.9 ms: 1.03x slower                                                    |
| deepcopy                   | 435 us                                                                | 448 us: 1.03x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.00 us: 1.03x slower                                                    |
| mypy2                      | 737 ms                                                                | 759 ms: 1.03x slower                                                     |
| pprint_pformat             | 1.85 sec                                                              | 1.93 sec: 1.04x slower                                                   |
| regex_dna                  | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| pprint_safe_repr           | 903 ms                                                                | 943 ms: 1.04x slower                                                     |
| gunicorn                   | 1.19 ms                                                               | 1.24 ms: 1.04x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.5 ms: 1.05x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.0 us: 1.05x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.09 sec: 1.06x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.66 ms: 1.06x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| thrift                     | 910 us                                                                | 967 us: 1.06x slower                                                     |
| pickle_list                | 5.01 us                                                               | 5.35 us: 1.07x slower                                                    |
| pyflate                    | 516 ms                                                                | 554 ms: 1.07x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 81.7 ms: 1.07x slower                                                    |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.07x slower                                                     |
| aiohttp                    | 1.13 ms                                                               | 1.22 ms: 1.08x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 8.94 ms: 1.08x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.91 us: 1.10x slower                                                    |
| scimark_fft                | 402 ms                                                                | 446 ms: 1.11x slower                                                     |
| scimark_sor                | 145 ms                                                                | 161 ms: 1.11x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 117 ms: 1.12x slower                                                     |
| regex_effbot               | 4.25 ms                                                               | 4.89 ms: 1.15x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.87 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.04 ms: 1.16x slower                                                    |
| coverage                   | 84.1 ms                                                               | 98.0 ms: 1.17x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.71 ms: 1.19x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.34 ms: 1.25x slower                                                    |
| telco                      | 7.80 ms                                                               | 9.86 ms: 1.26x slower                                                    |
| async_generators           | 378 ms                                                                | 486 ms: 1.28x slower                                                     |
| python_startup             | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                             |

Benchmark hidden because not significant (6): genshi_xml, logging_silent, nbody, asyncio_websockets, html5lib, mako
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.66% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x