# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: linux-aarch64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.11x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 354 ms: 1.18x slower                                                    |
| chameleon      | 8.29 ms                                                               | 9.96 ms: 1.20x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| html5lib       | 65.3 ms                                                               | 74.8 ms: 1.15x slower                                                   |
| tornado_http   | 140 ms                                                                | 136 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 517 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 629 ms: 1.32x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 670 ms: 1.30x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 478 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 816 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 802 ms: 1.15x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| nbody          | 113 ms                                                                | 138 ms: 1.23x slower                                                    |
| float          | 89.6 ms                                                               | 114 ms: 1.27x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                   |
| regex_dna      | 239 ms                                                                | 261 ms: 1.09x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.96 ms: 1.17x slower                                                   |
| regex_compile  | 137 ms                                                                | 167 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 14.0 ms: 1.10x faster                                                   |
| xml_etree_parse      | 209 ms                                                                | 197 ms: 1.06x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.51 us: 1.05x faster                                                   |
| pickle_list          | 5.01 us                                                               | 5.23 us: 1.04x slower                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.6 us: 1.08x slower                                                   |
| pickle               | 12.8 us                                                               | 13.9 us: 1.08x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 88.5 ms: 1.16x slower                                                   |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| tomli_loads          | 2.62 sec                                                              | 3.08 sec: 1.18x slower                                                  |
| xml_etree_generate   | 104 ms                                                                | 125 ms: 1.20x slower                                                    |
| pickle_pure_python   | 374 us                                                                | 449 us: 1.20x slower                                                    |
| unpickle_pure_python | 278 us                                                                | 349 us: 1.25x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.08x slower                                                            |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.47 ms: 1.15x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 49.9 ms: 1.19x slower                                                   |
| mako            | 13.3 ms                                                               | 16.5 ms: 1.24x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 77.7 ms: 1.25x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 36.6 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240511-arminc-aarch64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 227 us: 2.87x faster                                                    |
| generators                 | 64.2 ms                                                               | 39.7 ms: 1.62x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 575 ms: 1.60x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.24 sec: 1.43x faster                                                  |
| async_tree_none            | 701 ms                                                                | 517 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 629 ms: 1.32x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 670 ms: 1.30x faster                                                    |
| async_tree_none_tg         | 620 ms                                                                | 478 ms: 1.30x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.26 sec: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 816 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 802 ms: 1.15x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 14.0 ms: 1.10x faster                                                   |
| coroutines                 | 33.3 ms                                                               | 30.4 ms: 1.09x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 197 ms: 1.06x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.51 us: 1.05x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.28 us: 1.04x faster                                                   |
| tornado_http               | 140 ms                                                                | 136 ms: 1.03x faster                                                    |
| raytrace                   | 351 ms                                                                | 342 ms: 1.02x faster                                                    |
| pidigits                   | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 24.3 ms: 1.02x faster                                                   |
| asyncio_websockets         | 656 ms                                                                | 662 ms: 1.01x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 172 ms: 1.02x slower                                                    |
| richards_super             | 70.2 ms                                                               | 71.9 ms: 1.02x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 64.9 ms: 1.03x slower                                                   |
| comprehensions             | 29.0 us                                                               | 30.0 us: 1.03x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.23 us: 1.04x slower                                                   |
| json                       | 5.52 ms                                                               | 5.79 ms: 1.05x slower                                                   |
| sqlglot_parse              | 1.65 ms                                                               | 1.75 ms: 1.06x slower                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                                   |
| mdp                        | 3.35 sec                                                              | 3.60 sec: 1.07x slower                                                  |
| json_loads                 | 30.3 us                                                               | 32.6 us: 1.08x slower                                                   |
| sympy_str                  | 295 ms                                                                | 317 ms: 1.08x slower                                                    |
| chaos                      | 78.8 ms                                                               | 85.1 ms: 1.08x slower                                                   |
| thrift                     | 910 us                                                                | 985 us: 1.08x slower                                                    |
| sympy_expand               | 482 ms                                                                | 522 ms: 1.08x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.9 us: 1.08x slower                                                   |
| regex_dna                  | 239 ms                                                                | 261 ms: 1.09x slower                                                    |
| deltablue                  | 4.75 ms                                                               | 5.19 ms: 1.09x slower                                                   |
| pycparser                  | 1.25 sec                                                              | 1.37 sec: 1.10x slower                                                  |
| sqlglot_transpile          | 2.00 ms                                                               | 2.21 ms: 1.11x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.96 us: 1.11x slower                                                   |
| richards                   | 58.1 ms                                                               | 65.4 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 132 ms                                                                | 149 ms: 1.13x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.3 ms: 1.14x slower                                                   |
| sqlglot_optimize           | 63.4 ms                                                               | 72.4 ms: 1.14x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 74.8 ms: 1.15x slower                                                   |
| meteor_contest             | 115 ms                                                                | 132 ms: 1.15x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                               | 8.47 ms: 1.15x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.60 ms: 1.16x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 88.5 ms: 1.16x slower                                                   |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.96 ms: 1.17x slower                                                   |
| tomli_loads                | 2.62 sec                                                              | 3.08 sec: 1.18x slower                                                  |
| crypto_pyaes               | 86.5 ms                                                               | 102 ms: 1.18x slower                                                    |
| coverage                   | 84.1 ms                                                               | 99.1 ms: 1.18x slower                                                   |
| 2to3                       | 300 ms                                                                | 354 ms: 1.18x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.15 ms: 1.19x slower                                                   |
| django_template            | 41.8 ms                                                               | 49.9 ms: 1.19x slower                                                   |
| xml_etree_generate         | 104 ms                                                                | 125 ms: 1.20x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 449 us: 1.20x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 9.96 ms: 1.20x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 5.05 ms: 1.20x slower                                                   |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| go                         | 163 ms                                                                | 198 ms: 1.22x slower                                                    |
| regex_compile              | 137 ms                                                                | 167 ms: 1.22x slower                                                    |
| nbody                      | 113 ms                                                                | 138 ms: 1.23x slower                                                    |
| python_startup             | 10.2 ms                                                               | 12.5 ms: 1.23x slower                                                   |
| deepcopy                   | 435 us                                                                | 541 us: 1.24x slower                                                    |
| mako                       | 13.3 ms                                                               | 16.5 ms: 1.24x slower                                                   |
| deepcopy_reduce            | 3.89 us                                                               | 4.84 us: 1.24x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 77.7 ms: 1.25x slower                                                   |
| unpickle_pure_python       | 278 us                                                                | 349 us: 1.25x slower                                                    |
| nqueens                    | 102 ms                                                                | 130 ms: 1.27x slower                                                    |
| float                      | 89.6 ms                                                               | 114 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 7.98 ms: 1.27x slower                                                   |
| fannkuch                   | 451 ms                                                                | 575 ms: 1.28x slower                                                    |
| pprint_pformat             | 1.85 sec                                                              | 2.37 sec: 1.28x slower                                                  |
| pprint_safe_repr           | 903 ms                                                                | 1.16 sec: 1.29x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 2.43 ms: 1.30x slower                                                   |
| genshi_text                | 28.2 ms                                                               | 36.6 ms: 1.30x slower                                                   |
| scimark_fft                | 402 ms                                                                | 537 ms: 1.34x slower                                                    |
| scimark_sor                | 145 ms                                                                | 198 ms: 1.36x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 114 ms: 1.37x slower                                                    |
| async_generators           | 378 ms                                                                | 523 ms: 1.38x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 10.5 ms: 1.39x slower                                                   |
| pyflate                    | 516 ms                                                                | 726 ms: 1.41x slower                                                    |
| logging_silent             | 133 ns                                                                | 188 ns: 1.42x slower                                                    |
| spectral_norm              | 131 ms                                                                | 186 ms: 1.42x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 71.6 us: 1.46x slower                                                   |
| scimark_lu                 | 140 ms                                                                | 207 ms: 1.48x slower                                                    |
| telco                      | 7.80 ms                                                               | 166 ms: 21.21x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.11x slower                                                            |

Benchmark hidden because not significant (5): logging_format, pylint, bench_thread_pool, dask, pickle_dict
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.05x