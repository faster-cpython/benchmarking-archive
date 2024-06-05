# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: linux-x86_64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.07x faster
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.42 ms: 1.07x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.6 ms: 1.02x slower                                                        |
| tornado_http   | 124 ms                                                       | 118 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 372 ms: 1.39x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 430 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 346 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 582 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 615 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 89.2 ms: 1.04x faster                                                        |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 81.0 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 144 ms: 1.08x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                        |
| regex_dna      | 227 ms                                                       | 248 ms: 1.09x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.67 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.3 us: 1.19x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 211 us: 1.13x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 30.8 us: 1.05x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                         |
| unpickle_list        | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 60.4 ms: 1.08x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 86.8 ms: 1.09x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.41 us: 1.12x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.8 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.83 ms: 1.14x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                        |
| django_template | 39.3 ms                                                      | 38.1 ms: 1.03x faster                                                        |
| genshi_xml      | 57.1 ms                                                      | 56.3 ms: 1.01x faster                                                        |
| genshi_text     | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 174 us: 3.05x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 375 ms: 1.99x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                       |
| generators                 | 54.6 ms                                                      | 32.7 ms: 1.67x faster                                                        |
| pylint                     | 514 ms                                                       | 340 ms: 1.51x faster                                                         |
| comprehensions             | 25.1 us                                                      | 17.0 us: 1.48x faster                                                        |
| async_tree_none            | 518 ms                                                       | 372 ms: 1.39x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 430 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 346 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 582 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| chaos                      | 74.9 ms                                                      | 60.7 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 615 ms: 1.22x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 153 ms: 1.21x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.3 us: 1.19x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.37 ms: 1.18x faster                                                        |
| fannkuch                   | 416 ms                                                       | 358 ms: 1.16x faster                                                         |
| scimark_lu                 | 114 ms                                                       | 98.4 ms: 1.16x faster                                                        |
| nqueens                    | 103 ms                                                       | 88.9 ms: 1.15x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.31 us: 1.15x faster                                                        |
| sympy_str                  | 337 ms                                                       | 296 ms: 1.14x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 73.4 ms: 1.13x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 211 us: 1.13x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.46 sec: 1.12x faster                                                       |
| raytrace                   | 309 ms                                                       | 277 ms: 1.12x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 898 us: 1.11x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 23.3 ms: 1.11x faster                                                        |
| logging_format             | 7.71 us                                                      | 6.99 us: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 504 ms: 1.10x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.4 ms: 1.09x faster                                                        |
| regex_compile              | 156 ms                                                       | 144 ms: 1.08x faster                                                         |
| hexiom                     | 6.98 ms                                                      | 6.44 ms: 1.08x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.21 sec: 1.08x faster                                                       |
| scimark_monte_carlo        | 69.8 ms                                                      | 64.9 ms: 1.08x faster                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.42 ms: 1.07x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| richards_super             | 63.6 ms                                                      | 59.8 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.29 ms: 1.05x faster                                                        |
| tornado_http               | 124 ms                                                       | 118 ms: 1.05x faster                                                         |
| pickle_dict                | 32.3 us                                                      | 30.8 us: 1.05x faster                                                        |
| dask                       | 410 ms                                                       | 392 ms: 1.05x faster                                                         |
| nbody                      | 92.9 ms                                                      | 89.2 ms: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 897 us: 1.04x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                                         |
| logging_silent             | 100 ns                                                       | 96.8 ns: 1.04x faster                                                        |
| django_template            | 39.3 ms                                                      | 38.1 ms: 1.03x faster                                                        |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.03x faster                                                         |
| deepcopy                   | 391 us                                                       | 382 us: 1.02x faster                                                         |
| sqlglot_normalize          | 122 ms                                                       | 119 ms: 1.02x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                         |
| genshi_xml                 | 57.1 ms                                                      | 56.3 ms: 1.01x faster                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.42 us: 1.01x slower                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 59.7 ms: 1.01x slower                                                        |
| go                         | 158 ms                                                       | 160 ms: 1.01x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                                        |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 73.6 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 825 ms: 1.03x slower                                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.86 ms: 1.03x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 98.6 ms: 1.04x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.27 ms: 1.05x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                                       |
| pyflate                    | 449 ms                                                       | 478 ms: 1.06x slower                                                         |
| richards                   | 49.7 ms                                                      | 53.1 ms: 1.07x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.07x slower                                                        |
| float                      | 74.9 ms                                                      | 81.0 ms: 1.08x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 60.4 ms: 1.08x slower                                                        |
| scimark_sor                | 110 ms                                                       | 119 ms: 1.08x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.09x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.51 ms: 1.09x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 86.8 ms: 1.09x slower                                                        |
| regex_dna                  | 227 ms                                                       | 248 ms: 1.09x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.67 ms: 1.10x slower                                                        |
| scimark_fft                | 281 ms                                                       | 313 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.41 us: 1.12x slower                                                        |
| async_generators           | 322 ms                                                       | 363 ms: 1.13x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.85 us: 1.13x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.83 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.8 us: 1.19x slower                                                        |
| flaskblogging              | 3.88 ms                                                      | 4.68 ms: 1.21x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.41 ms: 1.24x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.01 ms: 1.27x slower                                                        |
| coverage                   | 66.1 ms                                                      | 85.3 ms: 1.29x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                 |

Benchmark hidden because not significant (5): asyncio_websockets, dulwich_log, pprint_pformat, deepcopy_memo, mypy2
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.57% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x