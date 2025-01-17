# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: linux-x86_64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 343 ms: 1.20x slower                                                        |
| chameleon      | 7.92 ms                                                      | 8.61 ms: 1.09x slower                                                       |
| docutils       | 2.85 sec                                                     | 3.46 sec: 1.22x slower                                                      |
| html5lib       | 72.2 ms                                                      | 84.5 ms: 1.17x slower                                                       |
| tornado_http   | 124 ms                                                       | 129 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                        | 1.14x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                        |
| async_tree_none            | 518 ms                                                       | 389 ms: 1.33x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 458 ms: 1.31x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 898 ms: 1.30x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 491 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 907 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 607 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 642 ms: 1.17x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 254 ms: 1.01x slower                                                        |
| float          | 74.9 ms                                                      | 95.7 ms: 1.28x slower                                                       |
| nbody          | 92.9 ms                                                      | 123 ms: 1.32x slower                                                        |
| Geometric mean | (ref)                                                        | 1.20x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.34 ms                                                      | 3.46 ms: 1.04x slower                                                       |
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                       |
| regex_compile  | 156 ms                                                       | 214 ms: 1.37x slower                                                        |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.17x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.07x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 30.7 us: 1.05x faster                                                       |
| unpickle_list        | 4.60 us                                                      | 4.68 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 113 ms: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                                       |
| unpickle             | 13.3 us                                                      | 15.4 us: 1.16x slower                                                       |
| xml_etree_generate   | 79.7 ms                                                      | 96.4 ms: 1.21x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 67.8 ms: 1.21x slower                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.88 sec: 1.28x slower                                                      |
| unpickle_pure_python | 238 us                                                       | 308 us: 1.29x slower                                                        |
| pickle_pure_python   | 316 us                                                       | 440 us: 1.39x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.90 ms: 1.15x slower                                                       |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 45.8 ms: 1.16x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 69.9 ms: 1.23x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 32.7 ms: 1.28x slower                                                       |
| mako            | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.25x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf2-x86_64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 200 us: 2.65x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 387 ms: 1.93x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                      |
| generators                 | 54.6 ms                                                      | 34.6 ms: 1.58x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                        |
| async_tree_none            | 518 ms                                                       | 389 ms: 1.33x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 458 ms: 1.31x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 898 ms: 1.30x faster                                                        |
| pylint                     | 514 ms                                                       | 396 ms: 1.30x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 491 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 907 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 607 ms: 1.24x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 22.9 ms: 1.21x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                       |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.17x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 642 ms: 1.17x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.1 ms: 1.11x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.70 us: 1.08x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.07x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 30.7 us: 1.05x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.36 us: 1.05x faster                                                       |
| json                       | 5.58 ms                                                      | 5.53 ms: 1.01x faster                                                       |
| mdp                        | 2.77 sec                                                     | 2.78 sec: 1.00x slower                                                      |
| pidigits                   | 251 ms                                                       | 254 ms: 1.01x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.68 us: 1.02x slower                                                       |
| sympy_sum                  | 186 ms                                                       | 189 ms: 1.02x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.03 ms: 1.03x slower                                                       |
| dask                       | 410 ms                                                       | 423 ms: 1.03x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.46 ms: 1.04x slower                                                       |
| tornado_http               | 124 ms                                                       | 129 ms: 1.04x slower                                                        |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                        |
| richards_super             | 63.6 ms                                                      | 66.9 ms: 1.05x slower                                                       |
| xml_etree_iterparse        | 107 ms                                                       | 113 ms: 1.06x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                                       |
| bench_mp_pool              | 4.70 ms                                                      | 5.02 ms: 1.07x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                       |
| chaos                      | 74.9 ms                                                      | 80.5 ms: 1.07x slower                                                       |
| raytrace                   | 309 ms                                                       | 333 ms: 1.08x slower                                                        |
| chameleon                  | 7.92 ms                                                      | 8.61 ms: 1.09x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.51 ms: 1.09x slower                                                       |
| sympy_integrate            | 25.8 ms                                                      | 28.3 ms: 1.10x slower                                                       |
| sympy_str                  | 337 ms                                                       | 370 ms: 1.10x slower                                                        |
| comprehensions             | 25.1 us                                                      | 27.6 us: 1.10x slower                                                       |
| pycparser                  | 1.31 sec                                                     | 1.46 sec: 1.11x slower                                                      |
| crypto_pyaes               | 83.3 ms                                                      | 93.0 ms: 1.12x slower                                                       |
| sympy_expand               | 553 ms                                                       | 624 ms: 1.13x slower                                                        |
| meteor_contest             | 131 ms                                                       | 148 ms: 1.14x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                                       |
| deltablue                  | 3.97 ms                                                      | 4.56 ms: 1.15x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 8.90 ms: 1.15x slower                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 2.20 ms: 1.15x slower                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.75 ms: 1.15x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.91 us: 1.16x slower                                                       |
| nqueens                    | 103 ms                                                       | 119 ms: 1.16x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.4 us: 1.16x slower                                                       |
| fannkuch                   | 416 ms                                                       | 483 ms: 1.16x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 78.3 ms: 1.16x slower                                                       |
| django_template            | 39.3 ms                                                      | 45.8 ms: 1.16x slower                                                       |
| sqlglot_normalize          | 122 ms                                                       | 142 ms: 1.17x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 84.5 ms: 1.17x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 4.03 us: 1.19x slower                                                       |
| richards                   | 49.7 ms                                                      | 59.3 ms: 1.19x slower                                                       |
| 2to3                       | 287 ms                                                       | 343 ms: 1.20x slower                                                        |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 71.0 ms: 1.20x slower                                                       |
| deepcopy                   | 391 us                                                       | 473 us: 1.21x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 96.4 ms: 1.21x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 138 ms: 1.21x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 67.8 ms: 1.21x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.46 sec: 1.22x slower                                                      |
| coverage                   | 66.1 ms                                                      | 80.7 ms: 1.22x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 69.9 ms: 1.23x slower                                                       |
| pprint_pformat             | 1.67 sec                                                     | 2.09 sec: 1.25x slower                                                      |
| pprint_safe_repr           | 805 ms                                                       | 1.03 sec: 1.27x slower                                                      |
| flaskblogging              | 3.88 ms                                                      | 4.95 ms: 1.27x slower                                                       |
| async_generators           | 322 ms                                                       | 411 ms: 1.28x slower                                                        |
| float                      | 74.9 ms                                                      | 95.7 ms: 1.28x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.88 sec: 1.28x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 32.7 ms: 1.28x slower                                                       |
| go                         | 158 ms                                                       | 203 ms: 1.29x slower                                                        |
| unpickle_pure_python       | 238 us                                                       | 308 us: 1.29x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.07 ms: 1.31x slower                                                       |
| nbody                      | 92.9 ms                                                      | 123 ms: 1.32x slower                                                        |
| mako                       | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                       |
| regex_compile              | 156 ms                                                       | 214 ms: 1.37x slower                                                        |
| pickle_pure_python         | 316 us                                                       | 440 us: 1.39x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 98.8 ms: 1.42x slower                                                       |
| pyflate                    | 449 ms                                                       | 645 ms: 1.44x slower                                                        |
| scimark_sor                | 110 ms                                                       | 166 ms: 1.51x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 10.6 ms: 1.52x slower                                                       |
| scimark_fft                | 281 ms                                                       | 429 ms: 1.53x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 58.2 us: 1.55x slower                                                       |
| logging_silent             | 100 ns                                                       | 161 ns: 1.60x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 155 ms: 1.63x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.97 ms: 1.71x slower                                                       |
| telco                      | 6.81 ms                                                      | 182 ms: 26.73x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                                |

Benchmark hidden because not significant (2): thrift, asyncio_websockets
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.06x