# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.07x faster
- HPT reliability: 99.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 288 ms: 1.01x slower                                                        |
| chameleon      | 7.92 ms                                                      | 7.50 ms: 1.06x faster                                                       |
| docutils       | 2.85 sec                                                     | 2.97 sec: 1.04x slower                                                      |
| html5lib       | 72.2 ms                                                      | 73.3 ms: 1.01x slower                                                       |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 435 ms: 1.38x faster                                                        |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 351 ms: 1.35x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 483 ms: 1.30x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 917 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 88.7 ms: 1.05x faster                                                       |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                        |
| float          | 74.9 ms                                                      | 79.9 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 144 ms: 1.08x faster                                                        |
| regex_v8       | 24.4 ms                                                      | 25.1 ms: 1.03x slower                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.46 ms: 1.03x slower                                                       |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                       |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| unpickle_pure_python | 238 us                                                       | 213 us: 1.12x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 31.5 us: 1.03x faster                                                       |
| unpickle_list        | 4.60 us                                                      | 4.73 us: 1.03x slower                                                       |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                       |
| xml_etree_generate   | 79.7 ms                                                      | 86.4 ms: 1.08x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 60.8 ms: 1.09x slower                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.48 sec: 1.10x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.39 us: 1.11x slower                                                       |
| unpickle             | 13.3 us                                                      | 15.5 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.83 ms: 1.14x slower                                                       |
| python_startup         | 10.7 ms                                                      | 13.1 ms: 1.22x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                       |
| django_template | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 58.6 ms: 1.03x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf2-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 173 us: 3.07x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 373 ms: 2.00x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                      |
| generators                 | 54.6 ms                                                      | 33.9 ms: 1.61x faster                                                       |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                                        |
| comprehensions             | 25.1 us                                                      | 17.0 us: 1.47x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 435 ms: 1.38x faster                                                        |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 351 ms: 1.35x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 483 ms: 1.30x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.9 ms: 1.27x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 917 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                       |
| chaos                      | 74.9 ms                                                      | 61.9 ms: 1.21x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                       |
| deltablue                  | 3.97 ms                                                      | 3.38 ms: 1.18x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 16.1 ms: 1.17x faster                                                       |
| scimark_lu                 | 114 ms                                                       | 97.3 ms: 1.17x faster                                                       |
| fannkuch                   | 416 ms                                                       | 357 ms: 1.17x faster                                                        |
| raytrace                   | 309 ms                                                       | 268 ms: 1.16x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 72.9 ms: 1.14x faster                                                       |
| sympy_str                  | 337 ms                                                       | 296 ms: 1.14x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 213 us: 1.12x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.49 sec: 1.11x faster                                                      |
| logging_simple             | 7.24 us                                                      | 6.52 us: 1.11x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 23.4 ms: 1.10x faster                                                       |
| nqueens                    | 103 ms                                                       | 93.4 ms: 1.10x faster                                                       |
| scimark_monte_carlo        | 69.8 ms                                                      | 63.6 ms: 1.10x faster                                                       |
| hexiom                     | 6.98 ms                                                      | 6.38 ms: 1.09x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 915 us: 1.09x faster                                                        |
| sympy_expand               | 553 ms                                                       | 507 ms: 1.09x faster                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.77 ms: 1.08x faster                                                       |
| regex_compile              | 156 ms                                                       | 144 ms: 1.08x faster                                                        |
| richards_super             | 63.6 ms                                                      | 58.9 ms: 1.08x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.15 us: 1.08x faster                                                       |
| json                       | 5.58 ms                                                      | 5.20 ms: 1.07x faster                                                       |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.50 ms: 1.06x faster                                                       |
| nbody                      | 92.9 ms                                                      | 88.7 ms: 1.05x faster                                                       |
| thrift                     | 931 us                                                       | 889 us: 1.05x faster                                                        |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                                        |
| meteor_contest             | 131 ms                                                       | 126 ms: 1.03x faster                                                        |
| dask                       | 410 ms                                                       | 397 ms: 1.03x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 31.5 us: 1.03x faster                                                       |
| logging_silent             | 100 ns                                                       | 98.3 ns: 1.02x faster                                                       |
| go                         | 158 ms                                                       | 156 ms: 1.01x faster                                                        |
| deepcopy                   | 391 us                                                       | 388 us: 1.01x faster                                                        |
| sqlglot_normalize          | 122 ms                                                       | 121 ms: 1.01x faster                                                        |
| 2to3                       | 287 ms                                                       | 288 ms: 1.01x slower                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.68 sec: 1.01x slower                                                      |
| sqlglot_optimize           | 59.0 ms                                                      | 59.5 ms: 1.01x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 73.3 ms: 1.01x slower                                                       |
| django_template            | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 58.6 ms: 1.03x slower                                                       |
| pprint_safe_repr           | 805 ms                                                       | 826 ms: 1.03x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.73 us: 1.03x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 25.1 ms: 1.03x slower                                                       |
| spectral_norm              | 95.1 ms                                                      | 97.9 ms: 1.03x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.50 us: 1.03x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.46 ms: 1.03x slower                                                       |
| deepcopy_memo              | 37.5 us                                                      | 39.1 us: 1.04x slower                                                       |
| docutils                   | 2.85 sec                                                     | 2.97 sec: 1.04x slower                                                      |
| richards                   | 49.7 ms                                                      | 51.9 ms: 1.04x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                       |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.27 ms: 1.05x slower                                                       |
| pyflate                    | 449 ms                                                       | 478 ms: 1.06x slower                                                        |
| float                      | 74.9 ms                                                      | 79.9 ms: 1.07x slower                                                       |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 86.4 ms: 1.08x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 60.8 ms: 1.09x slower                                                       |
| scimark_fft                | 281 ms                                                       | 306 ms: 1.09x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.48 sec: 1.10x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.39 us: 1.11x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.81 us: 1.12x slower                                                       |
| scimark_sor                | 110 ms                                                       | 124 ms: 1.13x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.71 ms: 1.14x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 8.83 ms: 1.14x slower                                                       |
| async_generators           | 322 ms                                                       | 367 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.5 us: 1.17x slower                                                       |
| flaskblogging              | 3.88 ms                                                      | 4.73 ms: 1.22x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.1 ms: 1.22x slower                                                       |
| telco                      | 6.81 ms                                                      | 8.33 ms: 1.22x slower                                                       |
| coverage                   | 66.1 ms                                                      | 81.2 ms: 1.23x slower                                                       |
| create_gc_cycles           | 1.58 ms                                                      | 2.01 ms: 1.28x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                |

Benchmark hidden because not significant (4): pickle_pure_python, asyncio_websockets, dulwich_log, bench_mp_pool
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.10% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x