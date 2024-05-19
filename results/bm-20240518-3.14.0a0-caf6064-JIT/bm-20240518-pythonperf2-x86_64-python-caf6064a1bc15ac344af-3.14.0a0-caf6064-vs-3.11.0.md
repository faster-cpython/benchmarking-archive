# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.02x faster
- HPT reliability: 98.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 306 ms: 1.07x slower                                                        |
| chameleon      | 7.92 ms                                                      | 8.00 ms: 1.01x slower                                                       |
| docutils       | 2.85 sec                                                     | 3.15 sec: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 374 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 344 ms: 1.38x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 468 ms: 1.34x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 874 ms: 1.34x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 453 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 890 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 621 ms: 1.21x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 82.6 ms: 1.13x faster                                                       |
| float          | 74.9 ms                                                      | 73.6 ms: 1.02x faster                                                       |
| pidigits       | 251 ms                                                       | 250 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 141 ms: 1.11x faster                                                        |
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.60 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| unpickle_pure_python | 238 us                                                       | 214 us: 1.11x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 99.6 ms: 1.07x faster                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                      |
| pickle_dict          | 32.3 us                                                      | 32.2 us: 1.00x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 321 us: 1.02x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 81.4 ms: 1.02x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                       |
| unpickle_list        | 4.60 us                                                      | 4.88 us: 1.06x slower                                                       |
| pickle               | 9.89 us                                                      | 10.9 us: 1.11x slower                                                       |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.12x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.68 us: 1.19x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.43 ms: 1.22x slower                                                       |
| python_startup         | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.11 ms: 1.21x faster                                                       |
| django_template | 39.3 ms                                                      | 43.4 ms: 1.11x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 29.3 ms: 1.15x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 68.7 ms: 1.20x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 186 us: 2.86x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 375 ms: 1.99x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                      |
| generators                 | 54.6 ms                                                      | 34.9 ms: 1.57x faster                                                       |
| comprehensions             | 25.1 us                                                      | 17.9 us: 1.40x faster                                                       |
| async_tree_none            | 518 ms                                                       | 374 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 344 ms: 1.38x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 468 ms: 1.34x faster                                                        |
| pylint                     | 514 ms                                                       | 383 ms: 1.34x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 874 ms: 1.34x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 453 ms: 1.32x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.3 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 890 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 621 ms: 1.21x faster                                                        |
| mako                       | 11.0 ms                                                      | 9.11 ms: 1.21x faster                                                       |
| richards_super             | 63.6 ms                                                      | 52.7 ms: 1.21x faster                                                       |
| fannkuch                   | 416 ms                                                       | 350 ms: 1.19x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 70.6 ms: 1.18x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 16.2 ms: 1.17x faster                                                       |
| spectral_norm              | 95.1 ms                                                      | 83.0 ms: 1.15x faster                                                       |
| chaos                      | 74.9 ms                                                      | 66.1 ms: 1.13x faster                                                       |
| nbody                      | 92.9 ms                                                      | 82.6 ms: 1.13x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 214 us: 1.11x faster                                                        |
| regex_compile              | 156 ms                                                       | 141 ms: 1.11x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 168 ms: 1.10x faster                                                        |
| raytrace                   | 309 ms                                                       | 284 ms: 1.09x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                        |
| richards                   | 49.7 ms                                                      | 46.0 ms: 1.08x faster                                                       |
| json                       | 5.58 ms                                                      | 5.18 ms: 1.08x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.76 us: 1.07x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                       | 99.6 ms: 1.07x faster                                                       |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.4 ms: 1.07x faster                                                       |
| sympy_str                  | 337 ms                                                       | 315 ms: 1.07x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.60 sec: 1.07x faster                                                      |
| tomli_loads                | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                      |
| sqlglot_parse              | 1.51 ms                                                      | 1.44 ms: 1.06x faster                                                       |
| nqueens                    | 103 ms                                                       | 97.4 ms: 1.05x faster                                                       |
| deltablue                  | 3.97 ms                                                      | 3.79 ms: 1.05x faster                                                       |
| hexiom                     | 6.98 ms                                                      | 6.68 ms: 1.04x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 963 us: 1.04x faster                                                        |
| sympy_expand               | 553 ms                                                       | 535 ms: 1.03x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.47 us: 1.03x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.85 ms: 1.03x faster                                                       |
| deepcopy_memo              | 37.5 us                                                      | 36.6 us: 1.03x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                      |
| thrift                     | 931 us                                                       | 910 us: 1.02x faster                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                                      |
| pprint_safe_repr           | 805 ms                                                       | 790 ms: 1.02x faster                                                        |
| float                      | 74.9 ms                                                      | 73.6 ms: 1.02x faster                                                       |
| pidigits                   | 251 ms                                                       | 250 ms: 1.00x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 32.2 us: 1.00x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 26.0 ms: 1.01x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 115 ms: 1.01x slower                                                        |
| chameleon                  | 7.92 ms                                                      | 8.00 ms: 1.01x slower                                                       |
| pickle_pure_python         | 316 us                                                       | 321 us: 1.02x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 81.4 ms: 1.02x slower                                                       |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.02x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 4.82 ms: 1.03x slower                                                       |
| scimark_fft                | 281 ms                                                       | 289 ms: 1.03x slower                                                        |
| go                         | 158 ms                                                       | 164 ms: 1.04x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                       |
| logging_silent             | 100 ns                                                       | 105 ns: 1.04x slower                                                        |
| pyflate                    | 449 ms                                                       | 470 ms: 1.05x slower                                                        |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.88 us: 1.06x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                       |
| 2to3                       | 287 ms                                                       | 306 ms: 1.07x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 130 ms: 1.07x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.45 ms: 1.07x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.60 ms: 1.08x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.67 us: 1.08x slower                                                       |
| deepcopy                   | 391 us                                                       | 424 us: 1.08x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 64.4 ms: 1.09x slower                                                       |
| django_template            | 39.3 ms                                                      | 43.4 ms: 1.11x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.15 sec: 1.11x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.11x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.81 us: 1.11x slower                                                       |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.12x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 29.3 ms: 1.15x slower                                                       |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.19x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.68 us: 1.19x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 68.7 ms: 1.20x slower                                                       |
| coverage                   | 66.1 ms                                                      | 80.6 ms: 1.22x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 9.43 ms: 1.22x slower                                                       |
| async_generators           | 322 ms                                                       | 396 ms: 1.23x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.96 ms: 1.25x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                       |
| flaskblogging              | 3.88 ms                                                      | 4.96 ms: 1.28x slower                                                       |
| telco                      | 6.81 ms                                                      | 174 ms: 25.50x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                                |

Benchmark hidden because not significant (6): asyncio_websockets, scimark_sparse_mat_mult, tornado_http, dulwich_log, dask, html5lib
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x