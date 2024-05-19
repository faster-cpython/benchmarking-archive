# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.04x faster
- HPT reliability: 99.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 289 ms: 1.01x slower                                                        |
| chameleon      | 7.92 ms                                                      | 7.29 ms: 1.09x faster                                                       |
| docutils       | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                      |
| html5lib       | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                       |
| tornado_http   | 124 ms                                                       | 119 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 366 ms: 1.41x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 441 ms: 1.36x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 865 ms: 1.35x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 615 ms: 1.22x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 87.9 ms: 1.06x faster                                                       |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                        |
| float          | 74.9 ms                                                      | 80.0 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                        |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                       |
| regex_dna      | 227 ms                                                       | 246 ms: 1.08x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 222 us: 1.08x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 30.7 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                                        |
| pickle_pure_python   | 316 us                                                       | 313 us: 1.01x faster                                                        |
| unpickle_list        | 4.60 us                                                      | 4.77 us: 1.04x slower                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.35 sec: 1.04x slower                                                      |
| xml_etree_generate   | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                       |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 59.8 ms: 1.07x slower                                                       |
| unpickle             | 13.3 us                                                      | 14.7 us: 1.11x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.44 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.82 ms: 1.14x slower                                                       |
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                       |
| genshi_xml     | 57.1 ms                                                      | 55.9 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 177 us: 3.01x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                      |
| generators                 | 54.6 ms                                                      | 33.7 ms: 1.62x faster                                                       |
| pylint                     | 514 ms                                                       | 343 ms: 1.50x faster                                                        |
| comprehensions             | 25.1 us                                                      | 17.1 us: 1.46x faster                                                       |
| async_tree_none            | 518 ms                                                       | 366 ms: 1.41x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 441 ms: 1.36x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 865 ms: 1.35x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.31x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.3 ms: 1.30x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                        |
| chaos                      | 74.9 ms                                                      | 59.8 ms: 1.25x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 615 ms: 1.22x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 16.2 ms: 1.17x faster                                                       |
| fannkuch                   | 416 ms                                                       | 358 ms: 1.16x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.41 ms: 1.16x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 72.1 ms: 1.16x faster                                                       |
| scimark_lu                 | 114 ms                                                       | 99.2 ms: 1.15x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.37 us: 1.14x faster                                                       |
| sympy_str                  | 337 ms                                                       | 298 ms: 1.13x faster                                                        |
| raytrace                   | 309 ms                                                       | 276 ms: 1.12x faster                                                        |
| nqueens                    | 103 ms                                                       | 92.2 ms: 1.11x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 902 us: 1.11x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                      |
| logging_format             | 7.71 us                                                      | 6.97 us: 1.11x faster                                                       |
| hexiom                     | 6.98 ms                                                      | 6.33 ms: 1.10x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 23.5 ms: 1.10x faster                                                       |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                        |
| sympy_expand               | 553 ms                                                       | 507 ms: 1.09x faster                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 64.2 ms: 1.09x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.29 ms: 1.09x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 222 us: 1.08x faster                                                        |
| richards_super             | 63.6 ms                                                      | 59.2 ms: 1.08x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.80 ms: 1.06x faster                                                       |
| nbody                      | 92.9 ms                                                      | 87.9 ms: 1.06x faster                                                       |
| pickle_dict                | 32.3 us                                                      | 30.7 us: 1.05x faster                                                       |
| mako                       | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                       |
| tornado_http               | 124 ms                                                       | 119 ms: 1.05x faster                                                        |
| dask                       | 410 ms                                                       | 395 ms: 1.04x faster                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 4.53 ms: 1.04x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                      |
| json                       | 5.58 ms                                                      | 5.42 ms: 1.03x faster                                                       |
| thrift                     | 931 us                                                       | 904 us: 1.03x faster                                                        |
| logging_silent             | 100 ns                                                       | 97.6 ns: 1.03x faster                                                       |
| genshi_xml                 | 57.1 ms                                                      | 55.9 ms: 1.02x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                                        |
| deepcopy                   | 391 us                                                       | 384 us: 1.02x faster                                                        |
| pickle_pure_python         | 316 us                                                       | 313 us: 1.01x faster                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.66 sec: 1.01x faster                                                      |
| meteor_contest             | 131 ms                                                       | 130 ms: 1.00x faster                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 810 ms: 1.01x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 67.9 ms: 1.01x slower                                                       |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                        |
| 2to3                       | 287 ms                                                       | 289 ms: 1.01x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.12 ms: 1.01x slower                                                       |
| spectral_norm              | 95.1 ms                                                      | 96.4 ms: 1.01x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.44 us: 1.01x slower                                                       |
| deepcopy_memo              | 37.5 us                                                      | 38.2 us: 1.02x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 60.1 ms: 1.02x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                       |
| unpickle_list              | 4.60 us                                                      | 4.77 us: 1.04x slower                                                       |
| richards                   | 49.7 ms                                                      | 51.6 ms: 1.04x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.35 sec: 1.04x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                       |
| scimark_fft                | 281 ms                                                       | 295 ms: 1.05x slower                                                        |
| docutils                   | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.40 ms: 1.06x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                       |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                                       |
| float                      | 74.9 ms                                                      | 80.0 ms: 1.07x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 59.8 ms: 1.07x slower                                                       |
| pyflate                    | 449 ms                                                       | 483 ms: 1.07x slower                                                        |
| go                         | 158 ms                                                       | 170 ms: 1.08x slower                                                        |
| regex_dna                  | 227 ms                                                       | 246 ms: 1.08x slower                                                        |
| unpickle                   | 13.3 us                                                      | 14.7 us: 1.11x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.84 us: 1.13x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.44 us: 1.13x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 8.82 ms: 1.14x slower                                                       |
| async_generators           | 322 ms                                                       | 373 ms: 1.16x slower                                                        |
| coverage                   | 66.1 ms                                                      | 77.7 ms: 1.17x slower                                                       |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                       |
| flaskblogging              | 3.88 ms                                                      | 4.73 ms: 1.22x slower                                                       |
| scimark_sor                | 110 ms                                                       | 138 ms: 1.26x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.03 ms: 1.29x slower                                                       |
| telco                      | 6.81 ms                                                      | 170 ms: 24.94x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                |

Benchmark hidden because not significant (3): genshi_text, asyncio_websockets, django_template
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.18% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x