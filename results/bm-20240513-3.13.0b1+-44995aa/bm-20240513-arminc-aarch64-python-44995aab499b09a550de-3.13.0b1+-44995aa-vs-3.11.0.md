# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: linux-aarch64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.02x faster
- HPT reliability: 99.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 302 ms: 1.01x slower                                                     |
| chameleon      | 8.29 ms                                                               | 9.02 ms: 1.09x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.13 sec: 1.07x slower                                                   |
| html5lib       | 65.3 ms                                                               | 68.4 ms: 1.05x slower                                                    |
| tornado_http   | 140 ms                                                                | 131 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 643 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 626 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 791 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 794 ms: 1.16x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 112 ms: 1.01x faster                                                     |
| float          | 89.6 ms                                                               | 90.5 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 128 ms: 1.06x faster                                                     |
| regex_dna      | 239 ms                                                                | 256 ms: 1.07x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                    |
| unpickle_pure_python | 278 us                                                                | 251 us: 1.11x faster                                                     |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.10x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.46 us: 1.06x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 361 us: 1.03x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| pickle_list          | 5.01 us                                                               | 5.12 us: 1.02x slower                                                    |
| pickle               | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 81.0 ms: 1.07x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                             |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.47 ms: 1.15x slower                                                    |
| python_startup         | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 62.2 ms                                                               | 61.0 ms: 1.02x faster                                                    |
| django_template | 41.8 ms                                                               | 41.3 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                             |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 197 us: 3.31x faster                                                     |
| generators                 | 64.2 ms                                                               | 37.6 ms: 1.71x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 568 ms: 1.62x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.22 sec: 1.44x faster                                                   |
| comprehensions             | 29.0 us                                                               | 20.2 us: 1.43x faster                                                    |
| async_tree_none            | 701 ms                                                                | 491 ms: 1.43x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 643 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 626 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.31x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| deltablue                  | 4.75 ms                                                               | 3.88 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 791 ms: 1.21x faster                                                     |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                                     |
| pylint                     | 397 ms                                                                | 340 ms: 1.17x faster                                                     |
| sqlglot_transpile          | 2.00 ms                                                               | 1.72 ms: 1.16x faster                                                    |
| chaos                      | 78.8 ms                                                               | 67.9 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 794 ms: 1.16x faster                                                     |
| sympy_sum                  | 168 ms                                                                | 145 ms: 1.16x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.45 ms: 1.14x faster                                                    |
| richards_super             | 70.2 ms                                                               | 62.4 ms: 1.12x faster                                                    |
| unpickle_pure_python       | 278 us                                                                | 251 us: 1.11x faster                                                     |
| sympy_integrate            | 23.2 ms                                                               | 21.0 ms: 1.10x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.10x faster                                                     |
| sympy_str                  | 295 ms                                                                | 270 ms: 1.09x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 22.9 ms: 1.08x faster                                                    |
| hexiom                     | 7.57 ms                                                               | 7.01 ms: 1.08x faster                                                    |
| dulwich_log                | 63.2 ms                                                               | 58.7 ms: 1.08x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.27 ms: 1.07x faster                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 81.2 ms: 1.07x faster                                                    |
| tornado_http               | 140 ms                                                                | 131 ms: 1.07x faster                                                     |
| logging_simple             | 7.57 us                                                               | 7.12 us: 1.06x faster                                                    |
| regex_compile              | 137 ms                                                                | 128 ms: 1.06x faster                                                     |
| unpickle_list              | 6.86 us                                                               | 6.46 us: 1.06x faster                                                    |
| richards                   | 58.1 ms                                                               | 54.9 ms: 1.06x faster                                                    |
| logging_format             | 8.22 us                                                               | 7.88 us: 1.04x faster                                                    |
| sympy_expand               | 482 ms                                                                | 463 ms: 1.04x faster                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 7.16 ms: 1.04x faster                                                    |
| sqlglot_normalize          | 132 ms                                                                | 128 ms: 1.04x faster                                                     |
| nqueens                    | 102 ms                                                                | 99.0 ms: 1.04x faster                                                    |
| pickle_pure_python         | 374 us                                                                | 361 us: 1.03x faster                                                     |
| tomli_loads                | 2.62 sec                                                              | 2.54 sec: 1.03x faster                                                   |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| dask                       | 385 ms                                                                | 377 ms: 1.02x faster                                                     |
| genshi_xml                 | 62.2 ms                                                               | 61.0 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                                     |
| pycparser                  | 1.25 sec                                                              | 1.23 sec: 1.02x faster                                                   |
| scimark_lu                 | 140 ms                                                                | 138 ms: 1.02x faster                                                     |
| django_template            | 41.8 ms                                                               | 41.3 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 82.3 ms: 1.01x faster                                                    |
| nbody                      | 113 ms                                                                | 112 ms: 1.01x faster                                                     |
| 2to3                       | 300 ms                                                                | 302 ms: 1.01x slower                                                     |
| float                      | 89.6 ms                                                               | 90.5 ms: 1.01x slower                                                    |
| asyncio_websockets         | 656 ms                                                                | 663 ms: 1.01x slower                                                     |
| deepcopy                   | 435 us                                                                | 443 us: 1.02x slower                                                     |
| pickle_list                | 5.01 us                                                               | 5.12 us: 1.02x slower                                                    |
| fannkuch                   | 451 ms                                                                | 463 ms: 1.03x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 50.4 us: 1.03x slower                                                    |
| mypy2                      | 737 ms                                                                | 762 ms: 1.03x slower                                                     |
| json                       | 5.52 ms                                                               | 5.73 ms: 1.04x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.04 us: 1.04x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 1.93 sec: 1.04x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.57 ms: 1.05x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 68.4 ms: 1.05x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.19 ms: 1.05x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 953 ms: 1.06x slower                                                     |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.06x slower                                                    |
| thrift                     | 910 us                                                                | 967 us: 1.06x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 81.0 ms: 1.07x slower                                                    |
| regex_dna                  | 239 ms                                                                | 256 ms: 1.07x slower                                                     |
| spectral_norm              | 131 ms                                                                | 140 ms: 1.07x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.13 sec: 1.07x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.6 us: 1.08x slower                                                    |
| pyflate                    | 516 ms                                                                | 557 ms: 1.08x slower                                                     |
| scimark_sor                | 145 ms                                                                | 158 ms: 1.09x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 9.02 ms: 1.09x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| sqlite_synth               | 3.56 us                                                               | 3.88 us: 1.09x slower                                                    |
| scimark_fft                | 402 ms                                                                | 446 ms: 1.11x slower                                                     |
| python_startup_no_site     | 7.35 ms                                                               | 8.47 ms: 1.15x slower                                                    |
| flaskblogging              | 4.19 ms                                                               | 4.86 ms: 1.16x slower                                                    |
| coverage                   | 84.1 ms                                                               | 97.5 ms: 1.16x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.13 ms: 1.19x slower                                                    |
| python_startup             | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.40 ms: 1.28x slower                                                    |
| async_generators           | 378 ms                                                                | 488 ms: 1.29x slower                                                     |
| telco                      | 7.80 ms                                                               | 164 ms: 21.00x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                                             |

Benchmark hidden because not significant (9): sqlglot_optimize, genshi_text, meteor_contest, go, mako, mdp, pickle_dict, logging_silent, gunicorn
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.58% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x