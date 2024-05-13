# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: linux-aarch64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 360 ms: 1.20x slower                                                     |
| chameleon      | 8.29 ms                                                               | 10.3 ms: 1.25x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                   |
| html5lib       | 65.3 ms                                                               | 75.0 ms: 1.15x slower                                                    |
| tornado_http   | 140 ms                                                                | 136 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 625 ms: 1.33x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 673 ms: 1.30x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 486 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.25 sec: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 813 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 820 ms: 1.12x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 237 ms: 1.02x faster                                                     |
| float          | 89.6 ms                                                               | 116 ms: 1.30x slower                                                     |
| nbody          | 113 ms                                                                | 150 ms: 1.33x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.19x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 255 ms: 1.07x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                    |
| regex_compile  | 137 ms                                                                | 173 ms: 1.27x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 193 ms: 1.08x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.73 us: 1.02x faster                                                    |
| pickle_list          | 5.01 us                                                               | 5.27 us: 1.05x slower                                                    |
| xml_etree_iterparse  | 152 ms                                                                | 161 ms: 1.06x slower                                                     |
| json_loads           | 30.3 us                                                               | 32.3 us: 1.07x slower                                                    |
| pickle               | 12.8 us                                                               | 13.8 us: 1.08x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 89.8 ms: 1.18x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 128 ms: 1.23x slower                                                     |
| tomli_loads          | 2.62 sec                                                              | 3.25 sec: 1.24x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 470 us: 1.26x slower                                                     |
| unpickle_pure_python | 278 us                                                                | 367 us: 1.32x slower                                                     |
| Geometric mean       | (ref)                                                                 | 1.10x slower                                                             |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.51 ms: 1.16x slower                                                    |
| python_startup         | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 51.0 ms: 1.22x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 77.7 ms: 1.25x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 37.0 ms: 1.31x slower                                                    |
| mako            | 13.3 ms                                                               | 17.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240513-arminc-aarch64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 227 us: 2.88x faster                                                     |
| generators                 | 64.2 ms                                                               | 39.5 ms: 1.62x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 581 ms: 1.59x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.17 sec: 1.47x faster                                                   |
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 625 ms: 1.33x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 673 ms: 1.30x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 486 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.25 sec: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 813 ms: 1.17x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 820 ms: 1.12x faster                                                     |
| coroutines                 | 33.3 ms                                                               | 30.7 ms: 1.08x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 193 ms: 1.08x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 23.9 ms: 1.04x faster                                                    |
| tornado_http               | 140 ms                                                                | 136 ms: 1.03x faster                                                     |
| pidigits                   | 242 ms                                                                | 237 ms: 1.02x faster                                                     |
| unpickle_list              | 6.86 us                                                               | 6.73 us: 1.02x faster                                                    |
| raytrace                   | 351 ms                                                                | 348 ms: 1.01x faster                                                     |
| asyncio_websockets         | 656 ms                                                                | 662 ms: 1.01x slower                                                     |
| sympy_sum                  | 168 ms                                                                | 173 ms: 1.03x slower                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 7.77 ms: 1.04x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.27 us: 1.05x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 66.4 ms: 1.05x slower                                                    |
| xml_etree_iterparse        | 152 ms                                                                | 161 ms: 1.06x slower                                                     |
| json                       | 5.52 ms                                                               | 5.88 ms: 1.06x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                                    |
| regex_dna                  | 239 ms                                                                | 255 ms: 1.07x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 31.2 ms: 1.07x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.61 sec: 1.08x slower                                                   |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                    |
| thrift                     | 910 us                                                                | 986 us: 1.08x slower                                                     |
| sympy_str                  | 295 ms                                                                | 320 ms: 1.08x slower                                                     |
| sympy_expand               | 482 ms                                                                | 525 ms: 1.09x slower                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.80 ms: 1.09x slower                                                    |
| richards_super             | 70.2 ms                                                               | 76.9 ms: 1.09x slower                                                    |
| comprehensions             | 29.0 us                                                               | 32.0 us: 1.10x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.38 sec: 1.11x slower                                                   |
| deltablue                  | 4.75 ms                                                               | 5.32 ms: 1.12x slower                                                    |
| gunicorn                   | 1.19 ms                                                               | 1.33 ms: 1.12x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.25 ms: 1.12x slower                                                    |
| chaos                      | 78.8 ms                                                               | 89.5 ms: 1.14x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.4 ms: 1.14x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 4.06 us: 1.14x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 152 ms: 1.15x slower                                                     |
| html5lib                   | 65.3 ms                                                               | 75.0 ms: 1.15x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.31 ms: 1.15x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.51 ms: 1.16x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 73.7 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| meteor_contest             | 115 ms                                                                | 136 ms: 1.18x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 89.8 ms: 1.18x slower                                                    |
| mypy2                      | 737 ms                                                                | 873 ms: 1.18x slower                                                     |
| richards                   | 58.1 ms                                                               | 69.6 ms: 1.20x slower                                                    |
| 2to3                       | 300 ms                                                                | 360 ms: 1.20x slower                                                     |
| flaskblogging              | 4.19 ms                                                               | 5.07 ms: 1.21x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                   |
| coverage                   | 84.1 ms                                                               | 102 ms: 1.21x slower                                                     |
| crypto_pyaes               | 86.5 ms                                                               | 106 ms: 1.22x slower                                                     |
| django_template            | 41.8 ms                                                               | 51.0 ms: 1.22x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.32 ms: 1.23x slower                                                    |
| python_startup             | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                    |
| go                         | 163 ms                                                                | 201 ms: 1.23x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 128 ms: 1.23x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.83 us: 1.24x slower                                                    |
| tomli_loads                | 2.62 sec                                                              | 3.25 sec: 1.24x slower                                                   |
| chameleon                  | 8.29 ms                                                               | 10.3 ms: 1.25x slower                                                    |
| genshi_xml                 | 62.2 ms                                                               | 77.7 ms: 1.25x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 470 us: 1.26x slower                                                     |
| regex_compile              | 137 ms                                                                | 173 ms: 1.27x slower                                                     |
| create_gc_cycles           | 1.87 ms                                                               | 2.39 ms: 1.28x slower                                                    |
| deepcopy                   | 435 us                                                                | 558 us: 1.28x slower                                                     |
| float                      | 89.6 ms                                                               | 116 ms: 1.30x slower                                                     |
| nqueens                    | 102 ms                                                                | 134 ms: 1.31x slower                                                     |
| genshi_text                | 28.2 ms                                                               | 37.0 ms: 1.31x slower                                                    |
| unpickle_pure_python       | 278 us                                                                | 367 us: 1.32x slower                                                     |
| mako                       | 13.3 ms                                                               | 17.5 ms: 1.32x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 2.45 sec: 1.32x slower                                                   |
| fannkuch                   | 451 ms                                                                | 599 ms: 1.33x slower                                                     |
| pprint_safe_repr           | 903 ms                                                                | 1.20 sec: 1.33x slower                                                   |
| nbody                      | 113 ms                                                                | 150 ms: 1.33x slower                                                     |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 8.47 ms: 1.35x slower                                                    |
| async_generators           | 378 ms                                                                | 524 ms: 1.39x slower                                                     |
| scimark_sor                | 145 ms                                                                | 202 ms: 1.39x slower                                                     |
| scimark_fft                | 402 ms                                                                | 561 ms: 1.39x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 119 ms: 1.43x slower                                                     |
| pyflate                    | 516 ms                                                                | 759 ms: 1.47x slower                                                     |
| spectral_norm              | 131 ms                                                                | 194 ms: 1.48x slower                                                     |
| logging_silent             | 133 ns                                                                | 199 ns: 1.50x slower                                                     |
| hexiom                     | 7.57 ms                                                               | 11.4 ms: 1.51x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 213 ms: 1.52x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 75.9 us: 1.55x slower                                                    |
| telco                      | 7.80 ms                                                               | 165 ms: 21.18x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.13x slower                                                             |

Benchmark hidden because not significant (6): pylint, logging_simple, dask, bench_thread_pool, pickle_dict, logging_format
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.05x