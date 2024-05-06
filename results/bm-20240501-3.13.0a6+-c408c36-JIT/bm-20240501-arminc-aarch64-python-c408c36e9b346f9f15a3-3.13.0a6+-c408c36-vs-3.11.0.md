# Results vs. 3.11.0

- fork: python
- ref: c408c36e9b346f9f15a3
- machine: linux-aarch64
- commit hash: c408c36
- commit date: 2024-05-01
- overall geometric mean: 1.01x slower
- HPT reliability: 98.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 348 ms: 1.16x slower                                                     |
| chameleon      | 8.29 ms                                                               | 9.37 ms: 1.13x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.40 sec: 1.16x slower                                                   |
| html5lib       | 65.3 ms                                                               | 70.4 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.10x slower                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 613 ms: 1.35x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 659 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.32x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.24 sec: 1.29x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.20 sec: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 773 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 804 ms: 1.19x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 107 ms: 1.05x faster                                                     |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                                     |
| float          | 89.6 ms                                                               | 89.2 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 247 ms: 1.03x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                    |
| regex_compile  | 137 ms                                                                | 160 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.8 ms: 1.20x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 188 ms: 1.11x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.31 us: 1.09x faster                                                    |
| pickle_pure_python   | 374 us                                                                | 354 us: 1.06x faster                                                     |
| xml_etree_iterparse  | 152 ms                                                                | 147 ms: 1.03x faster                                                     |
| tomli_loads          | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 276 us: 1.01x faster                                                     |
| pickle_dict          | 37.6 us                                                               | 37.8 us: 1.00x slower                                                    |
| pickle_list          | 5.01 us                                                               | 5.23 us: 1.04x slower                                                    |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| json_loads           | 30.3 us                                                               | 31.9 us: 1.05x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                                    |
| python_startup_no_site | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.45x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.8 ms: 1.04x faster                                                    |
| django_template | 41.8 ms                                                               | 48.3 ms: 1.16x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 33.8 ms: 1.20x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 79.5 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 213 us: 3.07x faster                                                     |
| generators                 | 64.2 ms                                                               | 38.1 ms: 1.69x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 622 ms: 1.48x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.27 sec: 1.40x faster                                                   |
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 613 ms: 1.35x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 659 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 472 ms: 1.32x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.24 sec: 1.29x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.20 sec: 1.28x faster                                                   |
| comprehensions             | 29.0 us                                                               | 23.5 us: 1.23x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 12.8 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 773 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 804 ms: 1.19x faster                                                     |
| richards_super             | 70.2 ms                                                               | 59.3 ms: 1.18x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 188 ms: 1.11x faster                                                     |
| coroutines                 | 33.3 ms                                                               | 29.9 ms: 1.11x faster                                                    |
| richards                   | 58.1 ms                                                               | 52.5 ms: 1.11x faster                                                    |
| raytrace                   | 351 ms                                                                | 317 ms: 1.11x faster                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.51 ms: 1.09x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.31 us: 1.09x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 23.3 ms: 1.06x faster                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 1.88 ms: 1.06x faster                                                    |
| pickle_pure_python         | 374 us                                                                | 354 us: 1.06x faster                                                     |
| nbody                      | 113 ms                                                                | 107 ms: 1.05x faster                                                     |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                                     |
| mako                       | 13.3 ms                                                               | 12.8 ms: 1.04x faster                                                    |
| deltablue                  | 4.75 ms                                                               | 4.59 ms: 1.04x faster                                                    |
| xml_etree_iterparse        | 152 ms                                                                | 147 ms: 1.03x faster                                                     |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                                   |
| unpickle_pure_python       | 278 us                                                                | 276 us: 1.01x faster                                                     |
| float                      | 89.6 ms                                                               | 89.2 ms: 1.00x faster                                                    |
| asyncio_websockets         | 656 ms                                                                | 658 ms: 1.00x slower                                                     |
| pickle_dict                | 37.6 us                                                               | 37.8 us: 1.00x slower                                                    |
| logging_simple             | 7.57 us                                                               | 7.61 us: 1.01x slower                                                    |
| logging_silent             | 133 ns                                                                | 133 ns: 1.01x slower                                                     |
| crypto_pyaes               | 86.5 ms                                                               | 87.5 ms: 1.01x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 84.4 ms: 1.01x slower                                                    |
| logging_format             | 8.22 us                                                               | 8.34 us: 1.01x slower                                                    |
| fannkuch                   | 451 ms                                                                | 461 ms: 1.02x slower                                                     |
| mdp                        | 3.35 sec                                                              | 3.43 sec: 1.02x slower                                                   |
| dask                       | 385 ms                                                                | 394 ms: 1.02x slower                                                     |
| json                       | 5.52 ms                                                               | 5.66 ms: 1.03x slower                                                    |
| meteor_contest             | 115 ms                                                                | 119 ms: 1.03x slower                                                     |
| pycparser                  | 1.25 sec                                                              | 1.28 sec: 1.03x slower                                                   |
| regex_dna                  | 239 ms                                                                | 247 ms: 1.03x slower                                                     |
| sqlglot_normalize          | 132 ms                                                                | 137 ms: 1.04x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 50.8 us: 1.04x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 174 ms: 1.04x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| chaos                      | 78.8 ms                                                               | 82.1 ms: 1.04x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.23 us: 1.04x slower                                                    |
| sympy_str                  | 295 ms                                                                | 307 ms: 1.04x slower                                                     |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| json_loads                 | 30.3 us                                                               | 31.9 us: 1.05x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 80.3 ms: 1.06x slower                                                    |
| deepcopy                   | 435 us                                                                | 461 us: 1.06x slower                                                     |
| sqlite_synth               | 3.56 us                                                               | 3.81 us: 1.07x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 68.0 ms: 1.07x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 70.4 ms: 1.08x slower                                                    |
| sympy_expand               | 482 ms                                                                | 520 ms: 1.08x slower                                                     |
| thrift                     | 910 us                                                                | 985 us: 1.08x slower                                                     |
| deepcopy_reduce            | 3.89 us                                                               | 4.22 us: 1.09x slower                                                    |
| spectral_norm              | 131 ms                                                                | 143 ms: 1.09x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| sympy_integrate            | 23.2 ms                                                               | 25.5 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.96 ms: 1.11x slower                                                    |
| dulwich_log                | 63.2 ms                                                               | 70.5 ms: 1.12x slower                                                    |
| scimark_fft                | 402 ms                                                                | 453 ms: 1.13x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 9.37 ms: 1.13x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                    |
| go                         | 163 ms                                                                | 187 ms: 1.15x slower                                                     |
| pyflate                    | 516 ms                                                                | 592 ms: 1.15x slower                                                     |
| django_template            | 41.8 ms                                                               | 48.3 ms: 1.16x slower                                                    |
| 2to3                       | 300 ms                                                                | 348 ms: 1.16x slower                                                     |
| docutils                   | 2.92 sec                                                              | 3.40 sec: 1.16x slower                                                   |
| gc_traversal               | 4.33 ms                                                               | 5.05 ms: 1.17x slower                                                    |
| bench_mp_pool              | 7.44 ms                                                               | 8.69 ms: 1.17x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| regex_compile              | 137 ms                                                                | 160 ms: 1.17x slower                                                     |
| nqueens                    | 102 ms                                                                | 120 ms: 1.17x slower                                                     |
| coverage                   | 84.1 ms                                                               | 99.2 ms: 1.18x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 8.94 ms: 1.18x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 33.8 ms: 1.20x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.30 ms: 1.23x slower                                                    |
| scimark_sor                | 145 ms                                                                | 183 ms: 1.26x slower                                                     |
| genshi_xml                 | 62.2 ms                                                               | 79.5 ms: 1.28x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 181 ms: 1.29x slower                                                     |
| pprint_safe_repr           | 903 ms                                                                | 1.18 sec: 1.31x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.43 sec: 1.31x slower                                                   |
| telco                      | 7.80 ms                                                               | 10.3 ms: 1.32x slower                                                    |
| async_generators           | 378 ms                                                                | 510 ms: 1.35x slower                                                     |
| python_startup             | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (2): tornado_http, pylint
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.18% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x