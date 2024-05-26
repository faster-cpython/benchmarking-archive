# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.06x faster
- HPT reliability: 99.68%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 305 ms: 1.06x slower                                                        |
| chameleon      | 7.92 ms                                                      | 7.68 ms: 1.03x faster                                                       |
| docutils       | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                      |
| html5lib       | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                        |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 348 ms: 1.36x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 470 ms: 1.34x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 903 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 585 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 624 ms: 1.21x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 81.6 ms: 1.14x faster                                                       |
| float          | 74.9 ms                                                      | 74.2 ms: 1.01x faster                                                       |
| pidigits       | 251 ms                                                       | 250 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 138 ms: 1.13x faster                                                        |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                       |
| regex_dna      | 227 ms                                                       | 243 ms: 1.07x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.67 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| unpickle_pure_python | 238 us                                                       | 222 us: 1.08x faster                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.12 sec: 1.06x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                       | 101 ms: 1.06x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 149 ms: 1.04x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 32.0 us: 1.01x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 318 us: 1.01x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 81.8 ms: 1.03x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                       |
| unpickle_list        | 4.60 us                                                      | 4.79 us: 1.04x slower                                                       |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.45 us: 1.13x slower                                                       |
| unpickle             | 13.3 us                                                      | 15.4 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.48 ms: 1.23x slower                                                       |
| python_startup         | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.14 ms: 1.20x faster                                                       |
| django_template | 39.3 ms                                                      | 41.4 ms: 1.05x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 64.8 ms: 1.13x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 185 us: 2.87x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 377 ms: 1.98x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                      |
| generators                 | 54.6 ms                                                      | 34.4 ms: 1.59x faster                                                       |
| comprehensions             | 25.1 us                                                      | 17.9 us: 1.40x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                        |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 348 ms: 1.36x faster                                                        |
| pylint                     | 514 ms                                                       | 380 ms: 1.35x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 470 ms: 1.34x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 903 ms: 1.30x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.5 ms: 1.29x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 585 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                       |
| fannkuch                   | 416 ms                                                       | 336 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 624 ms: 1.21x faster                                                        |
| richards_super             | 63.6 ms                                                      | 52.7 ms: 1.21x faster                                                       |
| mako                       | 11.0 ms                                                      | 9.14 ms: 1.20x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 70.2 ms: 1.19x faster                                                       |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 16.2 ms: 1.17x faster                                                       |
| chaos                      | 74.9 ms                                                      | 64.4 ms: 1.16x faster                                                       |
| nbody                      | 92.9 ms                                                      | 81.6 ms: 1.14x faster                                                       |
| regex_compile              | 156 ms                                                       | 138 ms: 1.13x faster                                                        |
| spectral_norm              | 95.1 ms                                                      | 84.3 ms: 1.13x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.45 us: 1.12x faster                                                       |
| sympy_sum                  | 186 ms                                                       | 166 ms: 1.12x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.01 us: 1.10x faster                                                       |
| raytrace                   | 309 ms                                                       | 284 ms: 1.09x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.57 sec: 1.08x faster                                                      |
| richards                   | 49.7 ms                                                      | 46.1 ms: 1.08x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 222 us: 1.08x faster                                                        |
| sympy_str                  | 337 ms                                                       | 314 ms: 1.07x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.73 ms: 1.07x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.06x faster                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.12 sec: 1.06x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                       | 101 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.30 ms: 1.05x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                       |
| nqueens                    | 103 ms                                                       | 98.4 ms: 1.04x faster                                                       |
| hexiom                     | 6.98 ms                                                      | 6.70 ms: 1.04x faster                                                       |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 3.91 ms: 1.04x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 961 us: 1.04x faster                                                        |
| sympy_expand               | 553 ms                                                       | 533 ms: 1.04x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 149 ms: 1.04x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.68 ms: 1.03x faster                                                       |
| thrift                     | 931 us                                                       | 904 us: 1.03x faster                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 68.0 ms: 1.03x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                      |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.02x faster                                                        |
| float                      | 74.9 ms                                                      | 74.2 ms: 1.01x faster                                                       |
| pickle_dict                | 32.3 us                                                      | 32.0 us: 1.01x faster                                                       |
| pidigits                   | 251 ms                                                       | 250 ms: 1.00x faster                                                        |
| pickle_pure_python         | 316 us                                                       | 318 us: 1.01x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 37.8 us: 1.01x slower                                                       |
| go                         | 158 ms                                                       | 161 ms: 1.02x slower                                                        |
| scimark_fft                | 281 ms                                                       | 288 ms: 1.03x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 81.8 ms: 1.03x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                       |
| pyflate                    | 449 ms                                                       | 463 ms: 1.03x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                       |
| unpickle_list              | 4.60 us                                                      | 4.79 us: 1.04x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 119 ms: 1.04x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 128 ms: 1.05x slower                                                        |
| django_template            | 39.3 ms                                                      | 41.4 ms: 1.05x slower                                                       |
| 2to3                       | 287 ms                                                       | 305 ms: 1.06x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                       |
| logging_silent             | 100 ns                                                       | 107 ns: 1.06x slower                                                        |
| regex_dna                  | 227 ms                                                       | 243 ms: 1.07x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.1 ms: 1.07x slower                                                       |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                       |
| deepcopy                   | 391 us                                                       | 427 us: 1.09x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.76 us: 1.09x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                      |
| regex_effbot               | 3.34 ms                                                      | 3.67 ms: 1.10x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.74 us: 1.10x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.45 us: 1.13x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 64.8 ms: 1.13x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                       |
| unpickle                   | 13.3 us                                                      | 15.4 us: 1.16x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.89 ms: 1.18x slower                                                       |
| async_generators           | 322 ms                                                       | 380 ms: 1.18x slower                                                        |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.19x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.17 ms: 1.20x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 9.48 ms: 1.23x slower                                                       |
| create_gc_cycles           | 1.58 ms                                                      | 1.98 ms: 1.26x slower                                                       |
| flaskblogging              | 3.88 ms                                                      | 4.96 ms: 1.28x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                       |
| coverage                   | 66.1 ms                                                      | 85.2 ms: 1.29x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                |

Benchmark hidden because not significant (8): dask, dulwich_log, pprint_pformat, pprint_safe_repr, tornado_http, asyncio_websockets, sympy_integrate, bench_mp_pool
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.68% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x