# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: linux-aarch64
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.02x slower
- HPT reliability: 98.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 356 ms: 1.19x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.53 sec: 1.21x slower                                                 |
| html5lib       | 65.3 ms                                                               | 70.7 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 494 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 828 ms                                                                | 609 ms: 1.36x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 665 ms: 1.31x faster                                                   |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                                 |
| async_tree_none_tg         | 620 ms                                                                | 479 ms: 1.30x faster                                                   |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 765 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 799 ms: 1.20x faster                                                   |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                   |
| float          | 89.6 ms                                                               | 90.1 ms: 1.01x slower                                                  |
| nbody          | 113 ms                                                                | 117 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                                  |
| regex_dna      | 239 ms                                                                | 258 ms: 1.08x slower                                                   |
| regex_effbot   | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                  |
| regex_compile  | 137 ms                                                                | 176 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                  |
| xml_etree_parse      | 209 ms                                                                | 189 ms: 1.11x faster                                                   |
| unpickle_list        | 6.86 us                                                               | 6.67 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 152 ms                                                                | 148 ms: 1.03x faster                                                   |
| unpickle_pure_python | 278 us                                                                | 275 us: 1.01x faster                                                   |
| tomli_loads          | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                                 |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                                  |
| pickle_list          | 5.01 us                                                               | 5.27 us: 1.05x slower                                                  |
| xml_etree_process    | 76.1 ms                                                               | 80.0 ms: 1.05x slower                                                  |
| json_loads           | 30.3 us                                                               | 32.4 us: 1.07x slower                                                  |
| xml_etree_generate   | 104 ms                                                                | 112 ms: 1.08x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 413 us: 1.10x slower                                                   |
| unpickle             | 16.9 us                                                               | 19.3 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.68 ms: 1.18x slower                                                  |
| python_startup         | 10.2 ms                                                               | 12.8 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                  |
| django_template | 41.8 ms                                                               | 49.1 ms: 1.18x slower                                                  |
| genshi_text     | 28.2 ms                                                               | 34.0 ms: 1.21x slower                                                  |
| genshi_xml      | 62.2 ms                                                               | 81.1 ms: 1.30x slower                                                  |
| Geometric mean  | (ref)                                                                 | 1.16x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240610-arminc-aarch64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 208 us: 3.15x faster                                                   |
| generators                 | 64.2 ms                                                               | 38.2 ms: 1.68x faster                                                  |
| asyncio_tcp                | 920 ms                                                                | 630 ms: 1.46x faster                                                   |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.24 sec: 1.42x faster                                                 |
| async_tree_none            | 701 ms                                                                | 494 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 828 ms                                                                | 609 ms: 1.36x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 665 ms: 1.31x faster                                                   |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                                 |
| async_tree_none_tg         | 620 ms                                                                | 479 ms: 1.30x faster                                                   |
| comprehensions             | 29.0 us                                                               | 23.1 us: 1.26x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 765 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 799 ms: 1.20x faster                                                   |
| json_dumps                 | 15.4 ms                                                               | 13.2 ms: 1.17x faster                                                  |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                  |
| richards_super             | 70.2 ms                                                               | 62.1 ms: 1.13x faster                                                  |
| pathlib                    | 24.8 ms                                                               | 22.2 ms: 1.11x faster                                                  |
| xml_etree_parse            | 209 ms                                                                | 189 ms: 1.11x faster                                                   |
| raytrace                   | 351 ms                                                                | 325 ms: 1.08x faster                                                   |
| richards                   | 58.1 ms                                                               | 55.4 ms: 1.05x faster                                                  |
| logging_format             | 8.22 us                                                               | 7.89 us: 1.04x faster                                                  |
| sqlglot_parse              | 1.65 ms                                                               | 1.59 ms: 1.04x faster                                                  |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                   |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                  |
| deltablue                  | 4.75 ms                                                               | 4.61 ms: 1.03x faster                                                  |
| unpickle_list              | 6.86 us                                                               | 6.67 us: 1.03x faster                                                  |
| xml_etree_iterparse        | 152 ms                                                                | 148 ms: 1.03x faster                                                   |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 278 us                                                                | 275 us: 1.01x faster                                                   |
| tomli_loads                | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                                 |
| float                      | 89.6 ms                                                               | 90.1 ms: 1.01x slower                                                  |
| asyncio_websockets         | 656 ms                                                                | 662 ms: 1.01x slower                                                   |
| meteor_contest             | 115 ms                                                                | 117 ms: 1.01x slower                                                   |
| sqlglot_transpile          | 2.00 ms                                                               | 2.03 ms: 1.02x slower                                                  |
| mdp                        | 3.35 sec                                                              | 3.42 sec: 1.02x slower                                                 |
| crypto_pyaes               | 86.5 ms                                                               | 88.8 ms: 1.03x slower                                                  |
| regex_v8                   | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                                  |
| nbody                      | 113 ms                                                                | 117 ms: 1.03x slower                                                   |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                                  |
| thrift                     | 910 us                                                                | 944 us: 1.04x slower                                                   |
| logging_silent             | 133 ns                                                                | 139 ns: 1.05x slower                                                   |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                                  |
| pickle_list                | 5.01 us                                                               | 5.27 us: 1.05x slower                                                  |
| xml_etree_process          | 76.1 ms                                                               | 80.0 ms: 1.05x slower                                                  |
| fannkuch                   | 451 ms                                                                | 476 ms: 1.06x slower                                                   |
| pylint                     | 397 ms                                                                | 421 ms: 1.06x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.4 us: 1.07x slower                                                  |
| sqlglot_normalize          | 132 ms                                                                | 142 ms: 1.07x slower                                                   |
| regex_dna                  | 239 ms                                                                | 258 ms: 1.08x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.01 ms: 1.08x slower                                                  |
| xml_etree_generate         | 104 ms                                                                | 112 ms: 1.08x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 70.7 ms: 1.08x slower                                                  |
| pycparser                  | 1.25 sec                                                              | 1.35 sec: 1.08x slower                                                 |
| sympy_str                  | 295 ms                                                                | 319 ms: 1.08x slower                                                   |
| scimark_monte_carlo        | 83.2 ms                                                               | 90.6 ms: 1.09x slower                                                  |
| sqlglot_optimize           | 63.4 ms                                                               | 69.1 ms: 1.09x slower                                                  |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.92 us: 1.10x slower                                                  |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.94 ms: 1.10x slower                                                  |
| pickle_pure_python         | 374 us                                                                | 413 us: 1.10x slower                                                   |
| sympy_expand               | 482 ms                                                                | 534 ms: 1.11x slower                                                   |
| spectral_norm              | 131 ms                                                                | 146 ms: 1.11x slower                                                   |
| sympy_sum                  | 168 ms                                                                | 187 ms: 1.11x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 70.6 ms: 1.12x slower                                                  |
| chaos                      | 78.8 ms                                                               | 88.2 ms: 1.12x slower                                                  |
| sympy_integrate            | 23.2 ms                                                               | 25.9 ms: 1.12x slower                                                  |
| deepcopy                   | 435 us                                                                | 490 us: 1.13x slower                                                   |
| nqueens                    | 102 ms                                                                | 116 ms: 1.13x slower                                                   |
| scimark_fft                | 402 ms                                                                | 460 ms: 1.14x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.3 us: 1.15x slower                                                  |
| pyflate                    | 516 ms                                                                | 598 ms: 1.16x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.94 ms: 1.16x slower                                                  |
| django_template            | 41.8 ms                                                               | 49.1 ms: 1.18x slower                                                  |
| python_startup_no_site     | 7.35 ms                                                               | 8.68 ms: 1.18x slower                                                  |
| hexiom                     | 7.57 ms                                                               | 8.96 ms: 1.18x slower                                                  |
| 2to3                       | 300 ms                                                                | 356 ms: 1.19x slower                                                   |
| deepcopy_reduce            | 3.89 us                                                               | 4.65 us: 1.20x slower                                                  |
| gc_traversal               | 4.33 ms                                                               | 5.18 ms: 1.20x slower                                                  |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                   |
| genshi_text                | 28.2 ms                                                               | 34.0 ms: 1.21x slower                                                  |
| docutils                   | 2.92 sec                                                              | 3.53 sec: 1.21x slower                                                 |
| scimark_sor                | 145 ms                                                                | 176 ms: 1.21x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.12 sec: 1.24x slower                                                 |
| pprint_pformat             | 1.85 sec                                                              | 2.32 sec: 1.25x slower                                                 |
| python_startup             | 10.2 ms                                                               | 12.8 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 2.35 ms: 1.25x slower                                                  |
| telco                      | 7.80 ms                                                               | 9.98 ms: 1.28x slower                                                  |
| regex_compile              | 137 ms                                                                | 176 ms: 1.29x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 81.1 ms: 1.30x slower                                                  |
| scimark_lu                 | 140 ms                                                                | 183 ms: 1.31x slower                                                   |
| async_generators           | 378 ms                                                                | 512 ms: 1.35x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.02x slower                                                           |

Benchmark hidden because not significant (5): logging_simple, tornado_http, deepcopy_memo, pickle_dict, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.92% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x