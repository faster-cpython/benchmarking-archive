# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_trampolines
- machine: linux-aarch64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.01x slower
- HPT reliability: 97.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 351 ms: 1.17x slower                                                         |
| chameleon      | 8.29 ms                                                               | 9.40 ms: 1.13x slower                                                        |
| docutils       | 2.92 sec                                                              | 3.43 sec: 1.18x slower                                                       |
| html5lib       | 65.3 ms                                                               | 71.0 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 510 ms: 1.38x faster                                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 609 ms: 1.36x faster                                                         |
| async_tree_memoization     | 872 ms                                                                | 660 ms: 1.32x faster                                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                       |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.19 sec: 1.29x faster                                                       |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 775 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 807 ms: 1.18x faster                                                         |
| Geometric mean             | (ref)                                                                 | 1.29x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 106 ms: 1.06x faster                                                         |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                                         |
| float          | 89.6 ms                                                               | 88.5 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                 | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                        |
| regex_dna      | 239 ms                                                                | 254 ms: 1.06x slower                                                         |
| regex_effbot   | 4.25 ms                                                               | 4.91 ms: 1.15x slower                                                        |
| regex_compile  | 137 ms                                                                | 163 ms: 1.19x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|---------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps          | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                        |
| xml_etree_parse     | 209 ms                                                                | 188 ms: 1.11x faster                                                         |
| unpickle_list       | 6.86 us                                                               | 6.41 us: 1.07x faster                                                        |
| pickle_pure_python  | 374 us                                                                | 361 us: 1.04x faster                                                         |
| xml_etree_iterparse | 152 ms                                                                | 147 ms: 1.03x faster                                                         |
| tomli_loads         | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                                       |
| pickle_dict         | 37.6 us                                                               | 37.7 us: 1.00x slower                                                        |
| xml_etree_process   | 76.1 ms                                                               | 80.0 ms: 1.05x slower                                                        |
| json_loads          | 30.3 us                                                               | 31.9 us: 1.05x slower                                                        |
| pickle              | 12.8 us                                                               | 13.6 us: 1.06x slower                                                        |
| pickle_list         | 5.01 us                                                               | 5.34 us: 1.07x slower                                                        |
| xml_etree_generate  | 104 ms                                                                | 114 ms: 1.10x slower                                                         |
| unpickle            | 16.9 us                                                               | 19.6 us: 1.16x slower                                                        |
| Geometric mean      | (ref)                                                                 | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                                        |
| python_startup_no_site | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                                        |
| Geometric mean         | (ref)                                                                 | 1.45x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.8 ms: 1.04x faster                                                        |
| django_template | 41.8 ms                                                               | 50.6 ms: 1.21x slower                                                        |
| genshi_text     | 28.2 ms                                                               | 34.5 ms: 1.22x slower                                                        |
| genshi_xml      | 62.2 ms                                                               | 80.3 ms: 1.29x slower                                                        |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------|:---------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 211 us: 3.09x faster                                                         |
| generators                 | 64.2 ms                                                               | 38.2 ms: 1.68x faster                                                        |
| asyncio_tcp                | 920 ms                                                                | 621 ms: 1.48x faster                                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.24 sec: 1.42x faster                                                       |
| async_tree_none            | 701 ms                                                                | 510 ms: 1.38x faster                                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 609 ms: 1.36x faster                                                         |
| async_tree_memoization     | 872 ms                                                                | 660 ms: 1.32x faster                                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.32x faster                                                       |
| async_tree_none_tg         | 620 ms                                                                | 473 ms: 1.31x faster                                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.19 sec: 1.29x faster                                                       |
| comprehensions             | 29.0 us                                                               | 23.6 us: 1.23x faster                                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 775 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 807 ms: 1.18x faster                                                         |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                        |
| richards_super             | 70.2 ms                                                               | 60.2 ms: 1.17x faster                                                        |
| xml_etree_parse            | 209 ms                                                                | 188 ms: 1.11x faster                                                         |
| coroutines                 | 33.3 ms                                                               | 30.1 ms: 1.11x faster                                                        |
| raytrace                   | 351 ms                                                                | 317 ms: 1.11x faster                                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.51 ms: 1.09x faster                                                        |
| richards                   | 58.1 ms                                                               | 53.3 ms: 1.09x faster                                                        |
| pathlib                    | 24.8 ms                                                               | 22.9 ms: 1.08x faster                                                        |
| unpickle_list              | 6.86 us                                                               | 6.41 us: 1.07x faster                                                        |
| nbody                      | 113 ms                                                                | 106 ms: 1.06x faster                                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.89 ms: 1.06x faster                                                        |
| mako                       | 13.3 ms                                                               | 12.8 ms: 1.04x faster                                                        |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                                         |
| pickle_pure_python         | 374 us                                                                | 361 us: 1.04x faster                                                         |
| xml_etree_iterparse        | 152 ms                                                                | 147 ms: 1.03x faster                                                         |
| deltablue                  | 4.75 ms                                                               | 4.62 ms: 1.03x faster                                                        |
| tomli_loads                | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                                       |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                        |
| float                      | 89.6 ms                                                               | 88.5 ms: 1.01x faster                                                        |
| logging_format             | 8.22 us                                                               | 8.19 us: 1.00x faster                                                        |
| pickle_dict                | 37.6 us                                                               | 37.7 us: 1.00x slower                                                        |
| asyncio_websockets         | 656 ms                                                                | 660 ms: 1.01x slower                                                         |
| logging_silent             | 133 ns                                                                | 133 ns: 1.01x slower                                                         |
| fannkuch                   | 451 ms                                                                | 456 ms: 1.01x slower                                                         |
| crypto_pyaes               | 86.5 ms                                                               | 88.1 ms: 1.02x slower                                                        |
| scimark_monte_carlo        | 83.2 ms                                                               | 85.1 ms: 1.02x slower                                                        |
| mdp                        | 3.35 sec                                                              | 3.43 sec: 1.02x slower                                                       |
| json                       | 5.52 ms                                                               | 5.68 ms: 1.03x slower                                                        |
| deepcopy_memo              | 49.0 us                                                               | 50.9 us: 1.04x slower                                                        |
| meteor_contest             | 115 ms                                                                | 120 ms: 1.04x slower                                                         |
| pycparser                  | 1.25 sec                                                              | 1.30 sec: 1.04x slower                                                       |
| regex_v8                   | 29.1 ms                                                               | 30.3 ms: 1.04x slower                                                        |
| dask                       | 385 ms                                                                | 401 ms: 1.04x slower                                                         |
| sqlglot_normalize          | 132 ms                                                                | 139 ms: 1.05x slower                                                         |
| xml_etree_process          | 76.1 ms                                                               | 80.0 ms: 1.05x slower                                                        |
| json_loads                 | 30.3 us                                                               | 31.9 us: 1.05x slower                                                        |
| sympy_str                  | 295 ms                                                                | 310 ms: 1.05x slower                                                         |
| regex_dna                  | 239 ms                                                                | 254 ms: 1.06x slower                                                         |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.06x slower                                                        |
| spectral_norm              | 131 ms                                                                | 139 ms: 1.06x slower                                                         |
| deepcopy                   | 435 us                                                                | 463 us: 1.06x slower                                                         |
| bench_mp_pool              | 7.44 ms                                                               | 7.91 ms: 1.06x slower                                                        |
| sympy_sum                  | 168 ms                                                                | 179 ms: 1.06x slower                                                         |
| thrift                     | 910 us                                                                | 968 us: 1.06x slower                                                         |
| pickle_list                | 5.01 us                                                               | 5.34 us: 1.07x slower                                                        |
| deepcopy_reduce            | 3.89 us                                                               | 4.19 us: 1.08x slower                                                        |
| sqlite_synth               | 3.56 us                                                               | 3.84 us: 1.08x slower                                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 68.9 ms: 1.09x slower                                                        |
| chaos                      | 78.8 ms                                                               | 85.7 ms: 1.09x slower                                                        |
| html5lib                   | 65.3 ms                                                               | 71.0 ms: 1.09x slower                                                        |
| sympy_expand               | 482 ms                                                                | 527 ms: 1.09x slower                                                         |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.10x slower                                                         |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.90 ms: 1.10x slower                                                        |
| scimark_fft                | 402 ms                                                                | 449 ms: 1.12x slower                                                         |
| sympy_integrate            | 23.2 ms                                                               | 25.9 ms: 1.12x slower                                                        |
| dulwich_log                | 63.2 ms                                                               | 71.3 ms: 1.13x slower                                                        |
| chameleon                  | 8.29 ms                                                               | 9.40 ms: 1.13x slower                                                        |
| go                         | 163 ms                                                                | 185 ms: 1.14x slower                                                         |
| gc_traversal               | 4.33 ms                                                               | 4.96 ms: 1.15x slower                                                        |
| regex_effbot               | 4.25 ms                                                               | 4.91 ms: 1.15x slower                                                        |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                                        |
| pyflate                    | 516 ms                                                                | 600 ms: 1.16x slower                                                         |
| 2to3                       | 300 ms                                                                | 351 ms: 1.17x slower                                                         |
| nqueens                    | 102 ms                                                                | 120 ms: 1.17x slower                                                         |
| docutils                   | 2.92 sec                                                              | 3.43 sec: 1.18x slower                                                       |
| hexiom                     | 7.57 ms                                                               | 8.97 ms: 1.18x slower                                                        |
| coverage                   | 84.1 ms                                                               | 100 ms: 1.19x slower                                                         |
| regex_compile              | 137 ms                                                                | 163 ms: 1.19x slower                                                         |
| django_template            | 41.8 ms                                                               | 50.6 ms: 1.21x slower                                                        |
| genshi_text                | 28.2 ms                                                               | 34.5 ms: 1.22x slower                                                        |
| create_gc_cycles           | 1.87 ms                                                               | 2.30 ms: 1.23x slower                                                        |
| telco                      | 7.80 ms                                                               | 9.69 ms: 1.24x slower                                                        |
| scimark_sor                | 145 ms                                                                | 184 ms: 1.27x slower                                                         |
| scimark_lu                 | 140 ms                                                                | 180 ms: 1.29x slower                                                         |
| genshi_xml                 | 62.2 ms                                                               | 80.3 ms: 1.29x slower                                                        |
| pprint_safe_repr           | 903 ms                                                                | 1.17 sec: 1.29x slower                                                       |
| pprint_pformat             | 1.85 sec                                                              | 2.42 sec: 1.31x slower                                                       |
| async_generators           | 378 ms                                                                | 506 ms: 1.34x slower                                                         |
| python_startup             | 10.2 ms                                                               | 14.7 ms: 1.44x slower                                                        |
| python_startup_no_site     | 7.35 ms                                                               | 10.7 ms: 1.45x slower                                                        |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): tornado_http, logging_simple, unpickle_pure_python, pylint
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 97.80% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x