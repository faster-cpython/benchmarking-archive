# Results vs. 3.11.0

- fork: python
- ref: e83ce850f433fd8bbf8f
- machine: linux-x86_64
- commit hash: e83ce85
- commit date: 2024-06-05
- overall geometric mean: 1.06x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 305 ms: 1.06x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                      |
| html5lib       | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                        |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 893 ms: 1.31x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 482 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 918 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 629 ms: 1.20x faster                                                        |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 81.1 ms: 1.15x faster                                                       |
| float          | 74.9 ms                                                      | 73.2 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 137 ms: 1.13x faster                                                        |
| regex_dna      | 227 ms                                                       | 240 ms: 1.06x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                       |
| regex_v8       | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                       |
| json_loads           | 28.9 us                                                      | 25.1 us: 1.15x faster                                                       |
| unpickle_pure_python | 238 us                                                       | 216 us: 1.11x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 99.8 ms: 1.07x faster                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.11 sec: 1.07x faster                                                      |
| pickle_pure_python   | 316 us                                                       | 318 us: 1.01x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 81.1 ms: 1.02x slower                                                       |
| pickle_dict          | 32.3 us                                                      | 33.3 us: 1.03x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                                       |
| unpickle_list        | 4.60 us                                                      | 4.96 us: 1.08x slower                                                       |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                       |
| pickle_list          | 3.94 us                                                      | 4.59 us: 1.17x slower                                                       |
| unpickle             | 13.3 us                                                      | 15.5 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.46 ms: 1.22x slower                                                       |
| python_startup         | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                       |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.19 ms: 1.20x faster                                                       |
| django_template | 39.3 ms                                                      | 41.8 ms: 1.06x slower                                                       |
| genshi_text     | 25.5 ms                                                      | 29.5 ms: 1.16x slower                                                       |
| genshi_xml      | 57.1 ms                                                      | 66.8 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 184 us: 2.89x faster                                                        |
| asyncio_tcp                | 747 ms                                                       | 382 ms: 1.96x faster                                                        |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                      |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                       |
| comprehensions             | 25.1 us                                                      | 18.2 us: 1.38x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                        |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                        |
| pylint                     | 514 ms                                                       | 380 ms: 1.35x faster                                                        |
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 893 ms: 1.31x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 482 ms: 1.30x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.5 ms: 1.29x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 918 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                       |
| richards_super             | 63.6 ms                                                      | 51.8 ms: 1.23x faster                                                       |
| fannkuch                   | 416 ms                                                       | 344 ms: 1.21x faster                                                        |
| mako                       | 11.0 ms                                                      | 9.19 ms: 1.20x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 629 ms: 1.20x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 69.9 ms: 1.19x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 16.0 ms: 1.18x faster                                                       |
| json_loads                 | 28.9 us                                                      | 25.1 us: 1.15x faster                                                       |
| nbody                      | 92.9 ms                                                      | 81.1 ms: 1.15x faster                                                       |
| regex_compile              | 156 ms                                                       | 137 ms: 1.13x faster                                                        |
| richards                   | 49.7 ms                                                      | 44.2 ms: 1.12x faster                                                       |
| chaos                      | 74.9 ms                                                      | 66.8 ms: 1.12x faster                                                       |
| sympy_sum                  | 186 ms                                                       | 166 ms: 1.12x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 216 us: 1.11x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.58 us: 1.10x faster                                                       |
| spectral_norm              | 95.1 ms                                                      | 86.5 ms: 1.10x faster                                                       |
| mdp                        | 2.77 sec                                                     | 2.55 sec: 1.09x faster                                                      |
| sympy_str                  | 337 ms                                                       | 312 ms: 1.08x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.16 us: 1.08x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 99.8 ms: 1.07x faster                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.11 sec: 1.07x faster                                                      |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.06x faster                                                       |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.7 ms: 1.06x faster                                                       |
| raytrace                   | 309 ms                                                       | 292 ms: 1.06x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.75 ms: 1.06x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 951 us: 1.05x faster                                                        |
| json                       | 5.58 ms                                                      | 5.32 ms: 1.05x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.04x faster                                                       |
| sympy_expand               | 553 ms                                                       | 531 ms: 1.04x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.76 ms: 1.03x faster                                                       |
| dulwich_log                | 67.4 ms                                                      | 65.3 ms: 1.03x faster                                                       |
| nqueens                    | 103 ms                                                       | 99.7 ms: 1.03x faster                                                       |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 3.95 ms: 1.03x faster                                                       |
| float                      | 74.9 ms                                                      | 73.2 ms: 1.02x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                      |
| thrift                     | 931 us                                                       | 914 us: 1.02x faster                                                        |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                                        |
| dask                       | 410 ms                                                       | 405 ms: 1.01x faster                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.65 sec: 1.01x faster                                                      |
| sympy_integrate            | 25.8 ms                                                      | 25.6 ms: 1.01x faster                                                       |
| scimark_lu                 | 114 ms                                                       | 113 ms: 1.01x faster                                                        |
| pprint_safe_repr           | 805 ms                                                       | 799 ms: 1.01x faster                                                        |
| pickle_pure_python         | 316 us                                                       | 318 us: 1.01x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                       |
| scimark_fft                | 281 ms                                                       | 284 ms: 1.01x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 81.1 ms: 1.02x slower                                                       |
| go                         | 158 ms                                                       | 161 ms: 1.02x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 33.3 us: 1.03x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                                       |
| pyflate                    | 449 ms                                                       | 469 ms: 1.04x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 127 ms: 1.04x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 4.93 ms: 1.05x slower                                                       |
| deepcopy                   | 391 us                                                       | 411 us: 1.05x slower                                                        |
| regex_dna                  | 227 ms                                                       | 240 ms: 1.06x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.38 ms: 1.06x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                       |
| django_template            | 39.3 ms                                                      | 41.8 ms: 1.06x slower                                                       |
| 2to3                       | 287 ms                                                       | 305 ms: 1.06x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.62 us: 1.07x slower                                                       |
| logging_silent             | 100 ns                                                       | 107 ns: 1.07x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.3 ms: 1.07x slower                                                       |
| unpickle_list              | 4.60 us                                                      | 4.96 us: 1.08x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.8 us: 1.09x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.79 us: 1.11x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 29.5 ms: 1.16x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.59 us: 1.17x slower                                                       |
| unpickle                   | 13.3 us                                                      | 15.5 us: 1.17x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 66.8 ms: 1.17x slower                                                       |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.18x slower                                                        |
| coverage                   | 66.1 ms                                                      | 78.8 ms: 1.19x slower                                                       |
| telco                      | 6.81 ms                                                      | 8.27 ms: 1.21x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 9.46 ms: 1.22x slower                                                       |
| async_generators           | 322 ms                                                       | 399 ms: 1.24x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.96 ms: 1.25x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                |

Benchmark hidden because not significant (4): tornado_http, asyncio_websockets, deepcopy_memo, pidigits
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x