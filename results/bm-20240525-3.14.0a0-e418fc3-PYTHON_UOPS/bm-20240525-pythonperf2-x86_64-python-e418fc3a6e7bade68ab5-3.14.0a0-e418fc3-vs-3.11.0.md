# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 343 ms: 1.20x slower                                                        |
| chameleon      | 7.92 ms                                                      | 8.74 ms: 1.10x slower                                                       |
| docutils       | 2.85 sec                                                     | 3.45 sec: 1.21x slower                                                      |
| html5lib       | 72.2 ms                                                      | 87.5 ms: 1.21x slower                                                       |
| tornado_http   | 124 ms                                                       | 130 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.15x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 396 ms: 1.31x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 459 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 363 ms: 1.31x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 496 ms: 1.27x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 935 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 603 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 932 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 645 ms: 1.17x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 254 ms: 1.01x slower                                                        |
| float          | 74.9 ms                                                      | 97.3 ms: 1.30x slower                                                       |
| nbody          | 92.9 ms                                                      | 124 ms: 1.33x slower                                                        |
| Geometric mean | (ref)                                                        | 1.20x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.34 ms                                                      | 3.49 ms: 1.04x slower                                                       |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.4 ms: 1.08x slower                                                       |
| regex_compile  | 156 ms                                                       | 215 ms: 1.38x slower                                                        |
| Geometric mean | (ref)                                                        | 1.13x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.3 ms: 1.17x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.9 us: 1.16x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.07x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 30.8 us: 1.05x faster                                                       |
| unpickle_list        | 4.60 us                                                      | 4.70 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 113 ms: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                       |
| unpickle             | 13.3 us                                                      | 15.6 us: 1.17x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.65 us: 1.18x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 68.8 ms: 1.23x slower                                                       |
| xml_etree_generate   | 79.7 ms                                                      | 98.3 ms: 1.23x slower                                                       |
| unpickle_pure_python | 238 us                                                       | 311 us: 1.30x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.95 sec: 1.31x slower                                                      |
| pickle_pure_python   | 316 us                                                       | 437 us: 1.38x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.93 ms: 1.15x slower                                                       |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 45.9 ms: 1.17x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 67.9 ms: 1.19x slower                                                       |
| mako            | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 33.4 ms: 1.31x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 204 us: 2.61x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 386 ms: 1.93x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                      |
| generators                 | 54.6 ms                                                      | 33.9 ms: 1.61x faster                                                       |
| async_tree_none            | 518 ms                                                       | 396 ms: 1.31x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 459 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 363 ms: 1.31x faster                                                        |
| pylint                     | 514 ms                                                       | 396 ms: 1.30x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 496 ms: 1.27x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 935 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 603 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 932 ms: 1.24x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 22.9 ms: 1.21x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 11.3 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 645 ms: 1.17x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.9 us: 1.16x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 17.2 ms: 1.10x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.07x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 30.8 us: 1.05x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.94 us: 1.04x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.48 us: 1.03x faster                                                       |
| json                       | 5.58 ms                                                      | 5.46 ms: 1.02x faster                                                       |
| pidigits                   | 251 ms                                                       | 254 ms: 1.01x slower                                                        |
| mdp                        | 2.77 sec                                                     | 2.81 sec: 1.01x slower                                                      |
| unpickle_list              | 4.60 us                                                      | 4.70 us: 1.02x slower                                                       |
| sympy_sum                  | 186 ms                                                       | 190 ms: 1.02x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.02 ms: 1.02x slower                                                       |
| dask                       | 410 ms                                                       | 422 ms: 1.03x slower                                                        |
| richards_super             | 63.6 ms                                                      | 65.9 ms: 1.04x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.49 ms: 1.04x slower                                                       |
| bench_mp_pool              | 4.70 ms                                                      | 4.90 ms: 1.04x slower                                                       |
| raytrace                   | 309 ms                                                       | 323 ms: 1.04x slower                                                        |
| tornado_http               | 124 ms                                                       | 130 ms: 1.05x slower                                                        |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 113 ms: 1.06x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                       |
| chaos                      | 74.9 ms                                                      | 80.9 ms: 1.08x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 26.4 ms: 1.08x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.51 ms: 1.09x slower                                                       |
| comprehensions             | 25.1 us                                                      | 27.4 us: 1.09x slower                                                       |
| sympy_integrate            | 25.8 ms                                                      | 28.2 ms: 1.09x slower                                                       |
| meteor_contest             | 131 ms                                                       | 144 ms: 1.10x slower                                                        |
| chameleon                  | 7.92 ms                                                      | 8.74 ms: 1.10x slower                                                       |
| sympy_str                  | 337 ms                                                       | 372 ms: 1.11x slower                                                        |
| pycparser                  | 1.31 sec                                                     | 1.45 sec: 1.11x slower                                                      |
| crypto_pyaes               | 83.3 ms                                                      | 93.4 ms: 1.12x slower                                                       |
| fannkuch                   | 416 ms                                                       | 473 ms: 1.14x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.73 ms: 1.14x slower                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 2.18 ms: 1.14x slower                                                       |
| deltablue                  | 3.97 ms                                                      | 4.53 ms: 1.14x slower                                                       |
| sympy_expand               | 553 ms                                                       | 636 ms: 1.15x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.90 us: 1.15x slower                                                       |
| nqueens                    | 103 ms                                                       | 118 ms: 1.15x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 140 ms: 1.15x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.93 ms: 1.15x slower                                                       |
| dulwich_log                | 67.4 ms                                                      | 78.0 ms: 1.16x slower                                                       |
| django_template            | 39.3 ms                                                      | 45.9 ms: 1.17x slower                                                       |
| unpickle                   | 13.3 us                                                      | 15.6 us: 1.17x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.65 us: 1.18x slower                                                       |
| richards                   | 49.7 ms                                                      | 58.9 ms: 1.19x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 67.9 ms: 1.19x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 70.6 ms: 1.20x slower                                                       |
| 2to3                       | 287 ms                                                       | 343 ms: 1.20x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 4.08 us: 1.20x slower                                                       |
| deepcopy                   | 391 us                                                       | 473 us: 1.21x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 87.5 ms: 1.21x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.45 sec: 1.21x slower                                                      |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 68.8 ms: 1.23x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 98.3 ms: 1.23x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 142 ms: 1.24x slower                                                        |
| coverage                   | 66.1 ms                                                      | 82.4 ms: 1.25x slower                                                       |
| pprint_pformat             | 1.67 sec                                                     | 2.08 sec: 1.25x slower                                                      |
| async_generators           | 322 ms                                                       | 404 ms: 1.26x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 1.02 sec: 1.26x slower                                                      |
| flaskblogging              | 3.88 ms                                                      | 4.92 ms: 1.27x slower                                                       |
| mako                       | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                       |
| go                         | 158 ms                                                       | 202 ms: 1.28x slower                                                        |
| float                      | 74.9 ms                                                      | 97.3 ms: 1.30x slower                                                       |
| create_gc_cycles           | 1.58 ms                                                      | 2.05 ms: 1.30x slower                                                       |
| unpickle_pure_python       | 238 us                                                       | 311 us: 1.30x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.95 sec: 1.31x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 33.4 ms: 1.31x slower                                                       |
| nbody                      | 92.9 ms                                                      | 124 ms: 1.33x slower                                                        |
| telco                      | 6.81 ms                                                      | 9.20 ms: 1.35x slower                                                       |
| regex_compile              | 156 ms                                                       | 215 ms: 1.38x slower                                                        |
| pickle_pure_python         | 316 us                                                       | 437 us: 1.38x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 97.8 ms: 1.40x slower                                                       |
| pyflate                    | 449 ms                                                       | 651 ms: 1.45x slower                                                        |
| scimark_sor                | 110 ms                                                       | 159 ms: 1.45x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 10.4 ms: 1.50x slower                                                       |
| scimark_fft                | 281 ms                                                       | 428 ms: 1.53x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 57.8 us: 1.54x slower                                                       |
| spectral_norm              | 95.1 ms                                                      | 148 ms: 1.55x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.49 ms: 1.60x slower                                                       |
| logging_silent             | 100 ns                                                       | 165 ns: 1.64x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                                |

Benchmark hidden because not significant (2): thrift, asyncio_websockets
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.05x